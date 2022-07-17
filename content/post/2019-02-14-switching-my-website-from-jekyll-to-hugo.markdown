---
date: "2019-02-14T00:00:00Z"
tags:
- website
- jekyll
- hugo
title: Switching my website from Jekyll to Hugo
---

I’ve switched from my old (and janky) Jekyll + Polymer setup to Hugo, a similar
static content management system written in Go. I’ve needed to do this for a 
very long time but I procrastinated due to a lack of interest, time, and 
energy. In this post I’ll go over why I’ve switched, including an overview of
how I was previously generating my website with Jekyll.

<!--more-->

## The old: Jekyll + Polymer

I used Jekyll for a very long time. Over the years I went through a few 
different template designs, even creating several of my own that I never 
ultimately published. I was always trying to find a balance between client-side 
functionality and compatibility. I wanted a “modern” website with contemporary
creature comforts (like a responsive, mobile-friendly frontend) that would also
work with basic web browsers.

Sometime last year I settled on 
[a cool combination of two different templates](https://github.com/brandonsilver/jekyll-polymer/tree/customized):
one using the Polymer front-end library with oodles of Material Design elements,
and another very basic one of my own creation for users with JavaScript disabled.
Building my website entailed running a gulp script, which in turn first built the
Polymer-using version of my website (the default one), and then built the basic
version. Sounds great, right? I finally had the best of both worlds. All of the
benefits of modernity with full backwards compatibility.

As it turned out, Polymer didn’t age well. And the build tooling required to build
my Polymer template didn’t age well either. Add to that the complexity of said
build tooling and its inability to fully optimize the final product and you get a
mildly frustrated developer looking for alternatives.


## The new: Hugo

Switching to Hugo has given me the opportunity I needed to simplify my website.
It’s now back to being a single command away from being built. It’s also much
faster to build than with the previous Jekyll and Polymer setup. The theme I’m
using is [Mainroad](https://themes.gohugo.io/mainroad/) with some
[light modifications](https://github.com/brandonsilver/hugo-blog/commit/c0709344daae20f7000381f0bfae6826b35b3dfb#diff-8d234111c5efab4aa56cbd903e43a781).