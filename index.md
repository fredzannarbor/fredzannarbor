---
title: Home Page
layout: default
---


mobile: +1.734-545-5369 | fredzannarbor at gmail doht com | Ann Arbor, Michigan, USA

## My Companies

- [Nimble Books LLC](nimble/about_nimble.html)
- AltBrains Workshop LLC

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Pages

[Nimble Books in Print](books.html)

