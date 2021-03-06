
# Food Oasis

This is a website with a map of food sources in Los Angeles, and list of resources about food deserts and health. You can view the site here…
https://foodoasis.la

## How to make changes

The website is published with [GitHub Pages](https://pages.github.com), and the files are generated with [Jekyll](http://jekyllrb.com).

As you make changes and commit/push them to GitHub, the [staging website](https://staging.foodoasis.la) will automatically update.

## How to develop locally

If you want to see a preview of your changes while you work, you can [run a Jekyll server](https://jekyllrb.com) on your local machine. [Installing Ruby and Jekyll](https://jekyllrb.com/docs/installation/) is a good place to start.

Since it takes a while to generate the whole site, you may want to run Jekyll in “incremenetal” mode, like this…

```jekyll serve --incremental```

## A summary of the project files

### Files for Jekyll
```
_config.yml
_data/*
_drafts/*
_includes/*
_layouts/*

```

### Files for Node.js
```
_node/*
```

### Files [generated by Node.js](#how-to-update-the-location-data), for Jekyll
```
_community-garden/*
_farmers-market/*
_food-pantry/*
```

### Files for GitHub
```
README.md
LICENSE
CNAME
```

### Assets
```
assets/css
assets/images
assets/js
```

### Pages
```
index.html
organizations.md
resources.md
about.md
team.md
faqs.md
news.html
404.md
```

### Pages translated into Spanish
```
es/*
```

### Lists of locations
```
locations/*
community-garden/*
farmers-market/*
food-pantry/*
```

## How to update the location data

The locations listed on the website are generated by Jekyll from markdown files in these folders…
```
_community-garden/*
_farmers-market/*
_food-pantry/*

community-garden/*
farmers-market/*
food-pantry/*

locations/*
```

The markdown files themselves are generated by [Node.js](https://nodejs.org) from the data files in the `_data` folder.

To re-generate the files, first install Node.js. And then run these three commands from your project folder…

1) Change to the `_node` directory…
```
cd _node
```

2) Install Node.js dependencies for this project…
```
npm install
```

3) Ask Node.js to run the generation script
```
node generate-locations.js
```

Note that this will overwrite the existing markdown files, but it won’t remove any of them. You may wish to manually remove these folders before running `generate-locations.js`, so there won’t be any old files left inside them…
```
_community-garden/*
_farmers-market/*
_food-pantry/*

community-garden/*
farmers-market/*
food-pantry/*

locations/*
