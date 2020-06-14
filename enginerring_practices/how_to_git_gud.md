---
layout: default
title: How to Git Gud
parent: Engineering Practices
nav_order: 2
---

# How to Git Gud

In this time and age, any self-respecting company or open-source project uses some form of source version control to
manage changes to the source code. Here at Forus Labs, we use Git for our projects and GitHub to host our Git repositories.

## Main Branches

Our Git repositories will always hold three permanent branches. `master`, `staging` and `stable`.

The main branch should be considered as `master`. This branch will always contain the latest changes for the next release.
Developers will be branching and merging bug fixes, enhancements and new features from `master`. This branch will not
contain comments used by tools to generate documentation, e.g. dartdoc and Javadoc comments. 

We do not allow those comments in master as those tend to become stale _really_ quickly given the rapid pace of development.
Having no comments is better than comments that are outdated and/or misleading. Furthermore, those comments tend to
clutter the source file. Nobody wants to work with a 500 line source file that contains 400 lines of comments.


Changes are merged from `master` into `staging`. This branch will always contain the latest changes that have been
documented. Developers will branch from `master` and merge the documented changes into `staging`.


Consider `stable` to be always represent the latest code deployed in production. Developers will not interact with this
branch on a day to day basis. Once considered ready for release, `staging` is merged into `stable`.


## Supporting Branches

Supporting branches are used to aid parallel development between team members. Unlike main branches, supporting branches
always have a limited lifetime. In most cases, a supporting branch is deleted after it is merged into a main branch.

There are three different types of supporting branches:
* Feature branches
* Fix branches
* Documentation branches

Feature branches contain enhancements and new features that are currently being worked on. A feature branch should be 
created from `master` and subsequently merged back into `master` once work on the feature is complete. Its name should 
start with `feature/` followed by a short description joined by hyphens, e.g. a feature branch that adds laser beams will
be `feature/laser-beams`.

Fix branches contain fixes for bugs present in `master`. They should be created from and merged to the master branch.
A fix branch should start with `fix/` followed by a short description joined by hyphens, e.g. `fix/missing-item`.

Lastly, a documentation branch contains documentation for bug fixes, enhancements and new features. It should be created
from `master` and merged into `staging`. A documentation branch should start with `documentation/` followed by the
description of the feature or fix branch that it documents, e.g. a documentation branch that documents the changes in
`feature/fancy-feature` will be `documentation/fancy-feature`.
