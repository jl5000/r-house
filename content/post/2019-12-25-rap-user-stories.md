---
title: "What's in a package?"
date: "2019-12-25"
author: "Jamie Lendrum"
tags: [r, agile, user stories, packages, rap, reproducibility]
---

Happy Christmas!

The holiday season has got me thinking about how discovering a new R package is like receiving a Christmas gift...you're not quite sure what's inside, but you're hoping it'll enrich your programming or analysis life in some way!

In this short blog post I'll be exploring a method to do this, of peeling back the wrapping paper so to speak, and getting straight to the point of the package in a succinct way.

The inspiration for this post has been in the development of a concept known as [Reproducible Analytical Pipelines](https://ukgovdatascience.github.io/rap-website/) (RAP) in UK Government. This is "a methodology for automating the bulk of steps involved in creating a statistical report". The RAP community promotes the use of programming languages, version control, automated testing, peer review, and other tools and methods.  

There are many R packages out there that can assist in RAPs, and the challenge is communicating what these packages do to those unfamiliar with the motivation behind RAP - let alone those who are relatively new to R.

In addition, every now and then, I see a new package on Twitter and it sounds like a really clever package, but I'm left wondering exactly why it's useful and how it'll improve my user experience. There are two absolutely magical R packages out there which are absolutely core to an advanced RAP, but communicating their worth to new users can be quite difficult. These are [drake](https://docs.ropensci.org/drake/) and [holepunch](https://karthik.github.io/holepunch/). It took me a while to wrap my own head around them.

To the authors' credit, they have taken the time to educate potential users through social media, user guides, vignettes, and videos, and in this post I'm proposing another method in which the 'so what' of these packages can be communicated; User Stories.

I've been familiar with User Stories for a couple of years now, and I think they're one of the more useful things to come out of agile methodologies. I'm certainly no expert, but I've found them to be great tools for getting to the nub of a problem. Within a user story, you identify the user, the function, and the benefit to the user. Whilst sounding quite simple, it can be a challenge getting these right for a number of reasons, for example; exposing implicit assumptions, and pitching them at an appropriate level.

With regards to the latter, they have a lot in common with the systems-thinking technique of 'laddering'. With laddering, you keep asking 'why?' to move up the ladder, and you ask 'how?' to move down the ladder. Asking 'why else?' and 'how else?' moves you sideways. Laddering is a useful skill for exploring purpose and potential options. It's important that you pitch your user stories on the appropriate rung of the ladder. This rung determines how many user stories you end up with.

In my experience, we've composed them using a standard structure: "As a {type of user}, I want to {do something}, So that {benefits are realised}". If we're going to apply this to a package, the first question is whether the {do something} is pitched at the overall package level or at the individual function level. For the sake of brevity, I'm going to pitch it at the package level, with the aim of bringing out individual aspects of functionality at the {benefits are realised} level.

Below I've produced a user story for each package above from the perspective of the analyst. One could easily construct others from the perspective of users trying to reproduce the results (e.g. a Technical Reviewer).

<br>

 Package | As a... | I want to... | So that...   
----------|-------------|-----------|------------
drake | Analyst | Orchestrate my complex analysis pipeline in an intelligent and efficient way | I can separate my workflow logic from my code logic.<br>I can save time by only re-running what I need to when something changes.<br>I can visualise my analysis pipeline.
holepunch | Analyst | Make my analysis environment available to anyone with minimal effort | They can easily reproduce my results and step through my approach

<br>
This could be a really good way for RAP champions to educate R beginners as to why certain packages are so useful, and indeed for package developers to communicate the purpose and benefits of their packages. 

It would be remiss of me to not mention that there are many potential ways of communicating and illustrating the value of packages. With respect to the packages above, there is a really good GitHub repository by Matt Dray which [illustrates drake by using a binder environment using the holepunch package](https://github.com/matt-dray/drake-egg-rap). Just click on the 'launch binder' button to view the analysis environment in the browser.