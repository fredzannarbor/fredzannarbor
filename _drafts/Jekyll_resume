# Writing a Smart Multipurpose Resume with Jekyll Collections

Do you struggle with figuring out how best to summarize your diverse (and, perhaps, lengthy...) experience into a handful or two of machine-learning-friendly bullet points?
Are you applying to several different types of jobs, perhaps seeking to make a career change?
Are you an inveterate tinkerer who likes to play around with technology?
If so, consider using Jekyll Collections to make a "Smart" Multipurpose Resume.

Jekyll is a popular free command-line program for Windows, Linux, or Mac that generates static web pages from your plain text or markdown documents. Crucially, it is used by GitHub's Pages platform, which provides an option for free web hosting; or you can upload the pages to your own server.

Jekyll includes a neat concept called "Collections" of related documents.  In this example, I show how to use Jekyll Collections to create different views of your experience through whatever prism is most important at the moment.

As I figured out how to achieve my goals, I leaned heavily on [the core Jekyll documentation for Collections](https://jekyllrb.com/docs/collections/), which is is quite good and includes [a step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/09-collections/).

My concept requires that I add two Collections to my site's default: Achievements and Employers. Then I will use Jekyll's Liquid template language to filter bullets in and out depending on situation.

The procedure is as follows.

1.  Create directories _achievements and _employers in your Jekyll site root.  The underscores are required in the directory names.

2.  Modify _config.yml by inserting the following anywhere:

```
achievements:
  output: true
  permalink: /:collection/:name

employers:
  output: true
  permalink: /:collection/:name

```
No underscores here!

This makes Jekyll aware of the collections.

3.  Each document in _achievements describes one of your noteworthy achievements. You should use the [now-standard X-Y-Z form](https://www.inc.com/bill-murphy-jr/google-recruiters-say-these-5-resume-tips-including-x-y-z-formula-will-improve-your-odds-of-getting-hired-at-google.html) of "Accomplished [X] as measured by [Y], by doing [Z]."

4.  Each document in _employers describes one of your employers in the one-line format 

5.  A metadata field that is common to each document type enables matching.
