---
layout: default
title: How to Review Code
parent: Code Reeeviews
nav_order: 1
---

The purpose of code reviews is to maintain and improve the quality of the codebase with each change. Nevertheless, a
balance should be sought between upholding the standard of the codebase and allowing progress on a pull request. 

## The Purpose of Code Reviews

It is _not_ the goal of a code review to demand absolute perfection in a pull request. That would only cause developers 
to be discouraged from making changes and dread code reviews. Rather, it is to ensure that the pull request is of a 
satisfactory standard. That being said, it is the responsibility of the reviewer to ensure that the pull request meets
the standards before being merged.

Only in cases of absolute emergencies can a pull request be merged without meeting the satisfactory standards.

The most important principle is for a reviewer is to be objective. Opinions and personal preferences are secondary to
technical truths and data. On the matter of style preferences, the corresponding style guide for the language should be
followed.

## Things to Look for in a Code Review

Before a code review, the pull request should have been successfully built on the CI. The review should not proceed if the 
build fails. Look for supporting tests, i.e. unit tests in the pull request or browse through the generated Codecov
report. In the report, the complexity and lines of code covered for the changes should be approximately ~90%. This is to
give leeway for code branches that cannot be reached in tests.

The most important thing to cover is overarching design. Do the changes integrate well with the existing codebase?
Is it consistent with the rest of the codebase? Does it belong inside the application or a library? Is there anything that
can be better designed? Did the author choose good names for everything? Closely linked to design is functionality. Are 
there any edge cases that the current change does not cover? Do the changes have the intended effect?

Other than data files, generated code or project files, every single line of code should be examined. If it is too hard
or takes too long to go through the changes, it is a sign the pull request is either too complex or long. Do let the
author know so that the issue can be resolved. Do not be afraid to ask the author to explain something if you do not
understand it. It is faster and clearer to seek clarification from the author rather than slowly struggle through the
code.

## Speed of Code Reviews

The speed of code reviews directly equate to development velocity. Code reviews should be completed soon after a pull
request submission. However, if you are in the middle of a focused task such as writing code, you should not interrupt
the task to do a code review. Instead, wait for the nearest break point, to switch tasks. The author should be requested
to split the pull request into several smaller pull requests if the pull request so large that you do not think that you 
have the time to review it.

## Handling Disagreements

Disagreements between the pull request author and reviewer are bound to happen. Always keep in mind that all criticism is
levelled at the pull request. Nothing personal kid, just business. Nevertheless, it goes without saying to keep all 
disagreements and discussions civil. 

Reviewers sometimes believe that the author will be ~~butthurt~~ upset if a reviewer insists on an improvement. Sometimes
the author do become upset, but it is usually brief, and they become thankful later that you helped them to improve their
code. Reviewers should not hesitate to insist on improvements to avoid upsetting the author. 

One of the biggest lies (other than the cake) is the promise made by the author to clean up the code after a pull request
is approved. The author promises to clean up the code after this pull request, thus it should be approved now. Often, the
clean-up does not happen and soon becomes lost or forgotten. It is usually best to insist that the author clean up the
code before the current pull request is approved.