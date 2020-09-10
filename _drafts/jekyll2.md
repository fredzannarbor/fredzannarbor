---
title: Smart Resumes with Jekyll 1 of 2
---

# Building a Multipurpose Resume with Jekyll Collections (part 2 of 2)

In the previous installment we created a nested for loop that iterates over our employers and accomplishments and assembles a smart resume based on the match between the resume goal and the accomplishment.  In this essay we will add some necessary features such as improved control over sorting and the addition of an Education section.

We want the employers in our resume to be sorted chronologically from newest to oldest. but by default Jekyll sorts documents in a collection by its last modification date, so we need to use Liquid's sort filter to make a copy of the employers collection.

![chair](/assets/images/2020-09-10-00-45-04.png)