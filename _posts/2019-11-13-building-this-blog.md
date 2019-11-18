---
layout: post
title:  "Building this blog"
date:   2019-11-13 16:08:27
comments: true
categories: web configurations
---

### Jekyll
This blog is built using the static site generator Jekyll and the base theme Minima. Read more on my thoughts about static site generators [here]({% post_url 2019-11-12-thoughts-on-static-site-generators %}).

### robots.txt
robots.txt is a file that is placed in the root folder of any website to give instruction to any robot (i.e web crawler) that visits.

For this website I chose to allow the Google robot to visit any pages on the website, but to dissallow all other robots.

```
User-agent: Google
Disallow:

User-agent: *
Disallow: / 
```

### humans.txt
humans.txt is a file that also is placed in the root of any website and presents information about the website to any human visitor, for example the team that contributed in the building of the website.

This is what this website's humans.txt looks like:
```
/* TEAM */
Role: Developer
Name: Liz Dahlström
Site: https://lizdahlstrom.github.io
Location: Gothenburg, Sweden

/ * SITE */
Language: English
Standards: HTML5, CSS3
Components: Jekyll, Sass
Software: VSCode, Docker
```

### Open Graph
Open Graph is a protocol that is widely use to present any web page as a "graph object" when linked in social media. It is as easy as providing meta data and Open Graph properties in the head section of a web page.

On this website I have implemented Open Graph by making a Jekyll template that is included in the head of every page.

Any page that is linked on social media will be presented with title, type, url and image.

### Disqus
In order to enable comments on the blog I have used the commenting platform [Disqus](https://disqus.com/).