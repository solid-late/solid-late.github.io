## HCZ Material theme

This is a simple personal material theme, best suited for personal authors, programmars, bloggers. 

### Demo
* [https://codeasashu.github.io/hcz-jekyll-blog](https://codeasashu.github.io/hcz-jekyll-blog/)

#### Feature

* Sitemap and XML Feed
* Site Search 
* Projects and tags
* Paginations in homepage
* Posts under category
* Related Posts
* Highlight pre
* Next & Previous Post
* Disqus comment

#### Screenshot

![Screenshot Home Page](https://raw.githubusercontent.com/ashutosh2k12/jekyllthemes/master/thumbnails/hcz-material.png  "Screenshot Home Page")


## How to

Short explenation how to work with the website.

### How to create a blog post

1. Create a new file in the folder *_posts* with the filename format **YYYY-MM-DD-short-description.md**. 
2. Use the following snippet at the beginning of the file:
```
---
layout: post
title:  "Insert your post title here"
date:   YYYY-MM-DD
category: [categroy1, category2]
---
```

3. Use markdown language to write your entry. A cheatsheet can be found [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### How to create/change/delete a category

1. Create a new file in the folder *category* with the filename format **category-name.md**.
2. Use the following snippet in the file:

```
---
layout: posts_by_category
categories: $category-name
title: $Title of the category
permalink: /category/$category-name
---
```