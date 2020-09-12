---
title: Home Page
layout: default
---

## Publish Using My Algorithmic Publishing Systems

1.  ZerothDraft takes your social media archives, analyzes and clusters them  into chapters, and creates a book draft that you can publish via my company, Nimble Books, or others.
2.  AltBrains Workshop enables you to create, consume, contribute to, and share persistent topic trackers.
3.  PageKicker is a command-line tool for creating topical e-books from permissioned content.
4.  Nimble Books LLC is an innovative, idiosyncratic independent publisher with more than 250 books in print on topics including politics, international relations, strategy, military and naval history, religion, law, and popular culture.

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