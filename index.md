---
title: Home Page
layout: default
---

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Pages

- [Nimble Books in Print ({{ site.books_in_print.size }}) ](books.html) 
- [AltBrains ({{ site.altbrains.size }})](altbrains.html) topic trackers

## About Me

### My Companies

- [Nimble Books LLC](nimble/about_nimble.html)
- AltBrains Workshop LLC

### Resumes
- [Resume](resumes/product_manager_goal.html) / [full CV](resumes/cv-full.html)

### Coordinates
- {% include coordinates.html %}