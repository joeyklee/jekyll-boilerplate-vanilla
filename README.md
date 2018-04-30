# README

Super minimal Jekyll boilerplate mostly derived from the super nice documentation from Tania Rascia's ["Make a Static Website with Jekyll"](https://www.taniarascia.com/make-a-static-website-with-jekyll/)

## Hopes and dreams

To use this template for quick static web projects with minimal needs

## Setup

see: https://jekyllrb.com/docs/quickstart/

```bash
# Install Bundler through RubyGems
gem install bundler

# Add Jekyll to your Gemfile and install its dependencies
bundle add jekyll && bundle install

# Create a new Jekyll site at ./myblog
jekyll new myblog

# Change into your new directory
cd myblog

# Build the site on the preview server
bundle exec jekyll serve

# Now browse to http://localhost:4000
```

## Files & Directories:

Very brief overview of things so we don't forget:


### _config.yml
This is where you set all your configurations that are accessibel throughout your project

Dont forget:

* to set the `baseurl` and `url` // notice our `baseurl` is `""` to default to the index
* the `include:["_pages"]` sets the `_pages` folder as the place where all your magic is happening

### _sass/
Our `_sass/` is where all our sass partials go. they are read into our `main.scss` living in the `css` folder which then gets compiled for use as `main.css`

### _site/
This is where all our stuff gets compiled to. Don't change anythign in here or else it will get overwritten.

### _pages/
Notice all of our pages are living in their own unique directory: 

* about
    - about.md
* blog
    - `_posts`
        + blog1.md
        + blog2.md
        + blog3.md
    - index.html // this takes care of the post list
* contact
    - contact.md

Remember:

* make sure to specify the `layout` and the `permalink`

```
---
layout: page
title: Contact
permalink: /contact/
---
```

* Each post also has a frontmatter

```
---
layout: post
title:  "activity data"
date:   2018-04-10 16:16:01 -0600
categories: data
permalink: /blog/activity-data
---
```


### _layouts/

The layouts contain our general layouts used throughout the page. 

Notice:

* home.html is our landing page
* default.html is our default structure. It takes the `includes/head.html`,  `includes/header.html`, and  `includes/footer.html` and mashes any of the `{{content}}` is is fed into it. 
* That way we can keep our nav bar etc in the same place

### _includes

The includes are just partial bits of markup that we use across our page.

#### _data

Our data folder is where we store data that can be accessed across our page. I <3 the data folder.
 

