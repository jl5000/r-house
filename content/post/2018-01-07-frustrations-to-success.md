---
title: "If at first you don't succeed..."
date: "2018-01-07"
author: "Jamie Lendrum"
tags: [r, rstudio, flickr, data science, git, github, netlify]
---

After having some time to ponder the issues I was having in my last post, I'm pleased to say that all three are resolved, or at least partially to my immediate satisfaction.

First off, I managed to get Netlify to automatically build my website for me, thanks to the helpful advice of their online support team. It turns out I was making a very silly error of trying to run a build command including the version, e.g. `hugo_0.31` AND creating a `HUGO_VERSION` environment variable. Turns out I just needed a simple `hugo` command when using the environment variable, and everything worked out fine. As an added bonus, I spontaneously decided to change my blog's theme, despite the high risk of it all going horribly wrong, and it worked like a charm. I had a few issues with old urls not working, but that was easily resolved. I really like it.

My attempts to use the Flickr API from R have also moved on somewhat. I've discovered that my code to access photosets actually works, but only for photosets that are public. Since all mine are private it was just giving me an empty list. To access my photosets I'll need to provide authentication to the API, and I've stumbled upon a [GitHub repo](https://github.com/jimhester/flickrr) which looks to contain code that I can use using the `httr` package.

Lastly, I discovered a great ebook [Happy Git and GitHub for the useR](http://happygitwithr.com/) by Jenny Bryan which has highlighted to me where I was going wrong with linking RStudio, Git, and GitHub and has a lot of good exaplanation. It now doesn't seem so daunting, notwithstanding the warning that *Git will crush you again with merge conflicts*!  
