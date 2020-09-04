# Writing a Smart Multipurpose Resume with Jekyll Collections

Do you struggle with figuring out how best to summarize your diverse (and, perhaps, lengthy...) experience into a handful or two of machine-learning-friendly bullet points?
Are you applying to several different types of jobs, perhaps seeking to make a career change?
Are you an inveterate tinkerer who likes to play around with technology?
If so, consider using Jekyll Collections to make a "Smart" Multipurpose Resume.

Jekyll is a popular free command-line program for Windows, Linux, or Mac that generates static web pages from your plain text or markdown documents. Crucially, it is used by GitHub's Pages platform, which provides an option for free web hosting; or you can upload the pages to your own server.

Jekyll includes a neat concept called "Collections" of related documents.  In this example, I show how to use Jekyll Collections to create different views of your experience through whatever prism is most important at the moment.

As I figured out how to achieve my goals, I leaned heavily on [the core Jekyll documentation for Collections](https://jekyllrb.com/docs/collections/), which is is quite good and includes [a step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/09-collections/).

My concept requires that I add two Collections to my site's default: Accomplishments and Employers. Then I will use Jekyll's Liquid template language to filter bullets in and out depending on situation.

The procedure is as follows.

1.  Create directories _accomplishments and _employers in your Jekyll site root.  The underscores are required in the directory names.

2.  Modify _config.yml by inserting the following anywhere:

```
accomplishments:
  output: true
  permalink: /:collection/:name

employers:
  output: true
  permalink: /:collection/:name

```
No underscores here!

This makes Jekyll aware of the collections.

3.  Each document in _achievements describes one of your noteworthy achievements. You should use the [now-standard X-Y-Z form](https://www.inc.com/bill-murphy-jr/google-recruiters-say-these-5-resume-tips-including-x-y-z-formula-will-improve-your-odds-of-getting-hired-at-google.html) of "Accomplished [X] as measured by [Y], by doing [Z]."

Here is an example of one that I did for a recent position.  I called this document "software-review.md".

```
---
job_title: Product Manager, Acme Widgets
from_date: May 2017
to_date: August 2019
resume_goal: product_mgr
keywords: strategy, money
employer: Acme
---
Reduced company spending by approximately $300,000 (25%) and reduced business risk to my product by review of company-wide utilization of key software dependency that resulted in renegotiated contract with better terms.


```
4.  Each document in _employers describes one of your past employers.  Here is the document for Acme:

---
layout: default
title: Acme
from_date: May 2017
to_date: August 2019
---
Product Manager, Acme Widgets May 2017 - August 2019

5.  Note that we need to have a field that enables us to match accomplishments with the employers that own them.  In employers it is "title" and in _accomplishments it is "employer".  

6. Now we create the "smart" part of the "smart resume."  We need some logic to pick out only the accomplishments that are relevant to the goal of the resume.  Jekyll uses the Liquid templating language which can do simple conditional logic and control operations inside HTML pages.  We create a page called "resume_by_goal.html" that will serve as the template for our smart resumes.

To create a resume that emphasizes accomplishments relative to our goal, we are going to loop over the collection of employers, then look at each accomplishment belonging to that employer and determine whether it is relevant to our goal.  We accomplish this with nested for loops.

The outer for loop iterates over our site's collection of employers.

```
---
layout: default
title: Resumes by Goal
---
<p><strong>Goal: a position as a developer relations advocate</strong></p>

{% for employer in site.employers %}

{{ employer.content }}

{{ INNER FOR LOOP WILL GO HERE }}

{% endfor %}

```

This loop alone creates output like the following:



The inner for loop iterates over the accomplishments.



<ul>

{% for accomplishment in site.accomplishments %}

{% if accomplishment.resume_goal == "developer_relations" and employer.title == accomplishment.employer %}

{{ accomplishment.content }}

{% endif %}
{% endfor %}
</ul>