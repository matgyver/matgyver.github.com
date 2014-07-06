---
layout: page
title: Welcome to RFGeeks 
tagline: I do RF and I'm a geek, enough said
---
{% include JB/setup %}

## Welcome to RFGeeks.com

Welcome to the new website for RFGeeks.com!

What is RFGeeks.com?  It is a website that will talk about electronics, computers, gaming, amateur radio, high altitude balloons, UASs, robotics and more.  It is basically a reflection of my interests or things I am involved in, the projects I do, the classes I teach and the research I do.  In addition, some personal projects of mine will be posted here as well.

So I hope you enjoy the new site.  I have recently moved the site to GitHub using GitHub Pages and Jekyll.  This is still a work in progress and I am slowly getting files, images, and information transferred over.  In the mean time if you need something from the old site you can find it [still at Google Sites](http://sites.google.con/site/rfgeeks)
    
## Navigating the site

The menu at the top will help you navigate the site.  Archive will take you a listing of past blog posts.  Tags will list tags that I will use for posts as well and can help you find a post or page that may be of a certain topic or interest.  Pages will list all pages on the site.  And finally Categories will list any categories defined and the relevant pages.

Below is also a list of blog posts.

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Projects
A vast majority of my projects are now hosted on GitHub.  So the best thing to do is to go to my [GitHub page](http://github.com/matgyver).  Eventually I plan to make GitHub pages for each project and then I will link those from this site.  In the meantime, a list of my projects is also below.

{{site.github.public_repositories}}

