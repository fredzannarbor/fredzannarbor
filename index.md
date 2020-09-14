---
title: Home Page
layout: default
---

## Algorithmic Publishing Systems

1.  ZerothDraft takes your social media archives, analyzes and clusters them  into chapters, and creates a book draft that you can publish via my company, Nimble Books, or others.  [Get started now.](zerothdraft/getting_archives.html)
2.  AltBrains Workshop enables you to create, consume, contribute to, and share persistent topic trackers.
3.  PageKicker is [an open source command-line tool](https://github.com/fredzannarbor/pagekicker-community) for creating topical e-books from permissioned content. Test & contribute: `git clone https://github.com/fredzannarbor/pagekicker-community.git`
4.  Nimble Books LLC is an innovative, idiosyncratic independent publisher with more than 200 [books in print](books.html) on topics including politics, international relations, strategy, military and naval history, religion, law, and popular culture.  Submit a proposal!

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

### My Resumes
- [for product management](resumes/product_manager_goal.html)
- [for product management emphasizing voice, AI, & science](resumes/voice_product_management_resume.html)
- [for developer relations](resumes/developer_rx_resume.html)
- [full CV](resumes/cv-full.html) (all positions, all publications)
- [how to create smart resumes in Jekyll](_posts/2020-09-07-Jekyll-smart-resume.md)

### My Coordinates
- {% include coordinates.html %}