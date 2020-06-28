---
layout: default
title: Contributing to a Project
parent: Engineering Practices
nav_order: 2
---

# Contributing to a Project

So you ~~were forced~~ want to contribute to one of Forus Labs' open-source or proprietary projects. This guide details
the steps to contribute to a project. The contents of each step may be different for some projects but should still
roughly follow what is outlined in this article. 

## Issuing an Issue

Before taking further action, an issue needs to be created in the appropriate GitHub repository. If you are a developer
at Forus Labs, consider discussing the issue with other developers internally before creating an issue on GitHub. This
will ensure that the issue raised is relevant and _actually_ an issue. To expedite the process, follow an issue template
provided in the repository.

A submitted issue will be triage accordingly once it has been discussed. Although it is highly subjective due to the 
specifics of each project, a triage issue will, in general, be labelled with the following:

- Depending on the nature of the issue, either `bug`, `enhancement` or `new feature`
- `component: x` - where `x` is an affected component
- `priority: y` - where `y` is the priority of the issue

In addition, a triage issue may be assigned to a version milestone.

After submitting an issue, you can either choose to submit a pull request to resolve the issue yourself or wait for 
someone else to (hopefully) do so.

## Submitting a Pull Request

When submitting a pull request, do include a description of what the pull request does, and if possible, how it does so. 
The description should also mention any issues linked to the pull request. 

## How a Pull Request is Reviewed

All submitted pull requests will be reviewed before they are accepted. Precedence is given to pull requests with higher
priority.

Describing the nuances of reviewing the code in a pull request is out of the scope of this article. It warrants its own 
article due to how lengthy the topic is. Please see [code reeeviews](code_reviews) for more information.

## Post Pull Request Review

After reviewing a pull request, either of the following will happen. In the best case scenario, the pull request is
accepted. Yay! However, in most cases, there will be issues in the pull request that you will be requested to fix. 
After fixing the issues, the pull request will be reviewed again and vice versa. On some occasions, we may choose to 
decline a pull request.

If a pull request is accepted, the feature branch that contains the pull request is squashed and merged. After which, it
is deleted.


