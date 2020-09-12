---
title: Dashboard
layout: default
---
Username: fzimmerman

- [Zeroth Draft](#zeroth-draft)
- [AltBrains](#altbrains)
- [Nimble Books](#nimble-books)

## Zeroth Draft 

Platform| User Id | Status
---------|----------|---------
Facebook | FredZimmerman1 | Processing
LinkedIn | wfzimmerman | Processing
Twitter  | fredzannarbor | Processing

## AltBrains

{% assign twitter_url = "https://twitter.com/search?q=" %}

Name| Resource | Status
---------|----------|---------
{% for altbrain in site.altbrains -%} [{{ altbrain.title }}]({{ altbrain.url }}) | {% if altbrain.twitter_search_string != "" %}Twitter search: <a href="{{ twitter_url | append: altbrain.twitter_search_string }}">{{ twitter_url | append: altbrain.twitter_search_string }}</a>{%- else -%}
{%- endif -%} | foo
{% endfor %}


## Nimble Books


{% assign authorbooks = site.books_in_print |  where_exp: "item", "item.Author contains 'Zimmerman'" %}


Title | ISBN | Status
------|-------|------
{% for book in authorbooks %}{% if book.Author contains "Zimmerman" %}<a href="{{ book.url | relative_url }}">{{ book.title }}</a> | {{ book.ISBN }} | Available {%- else -%}ouch{%- endif -%} |
{% endfor %}