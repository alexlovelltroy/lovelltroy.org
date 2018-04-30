+++
# Date this page was created.
date = "2018-03-20"

# Project title.
title = "Mnemonic-as-a-service"

# Project summary to display on homepage.
summary = "Instead of Hello World, I use a mnemonic wordlist to play around with new languages."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "scaled/presidencia.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["programming", "devops"]

# Optional external URL for project (replaces project detail page).
external_link = "https://github.com/alexlovelltroy/mnemonic-gin/"

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/header-presidencia.jpg"
caption = "My caption :smile:"

+++
# Mnemonic as a Service

>There are only two hard things in Computer Science: cache invalidation and naming things.
>
>-- Phil Karlton

Since I originally started playing with this wordlist, it has become my ```hello world``` example for dealing with new languages and frameworks.  I have examples in [flask](https://github.com/alexlovelltroy/mnemonic-as-a-service), [django](https://github.com/alexlovelltroy/django_mnemonic), nodejs, and lambda, that have all been behind menmonic-as-a-service.com at one time or another.  My latest attempts use several implementation patterns in golang.

The nice folks at [mnx.io](http://mnx.io/) wrote a fun [blog post](http://mnx.io/blog/a-proper-server-naming-scheme/) about server naming schemes.

One of the pearls of wisdom is the recommendation to use Oren Tirosh’s [mnemonic encoding project](http://web.archive.org/web/20090918202746/http://tothink.com/mnemonic/wordlist.html) as a wordlist.

GENIUS!


# Enter Golang, Docker and Kubernetes

Enough time has passed that I needed to play with a few more ideas.  The first is golang, so that's the language I've used here.  The second is Docker which is a natural fit for running Go binaries with repeatable environment variables.  It's certianly not necessary, but fun to learn.  I also have been working with kubernetes a lot recently and found the pod/service/deployment concept interesting enough to experiment there too.  Check out the Makefile for some GKE sugar that allowed me to do most of the development of this repo while on an airplane over the Pacific.  (No local docker builds on satellite internet)

# Rainbow Deploys

I'm not sold on this pattern yet, but found it compelling ehough to play with once I read about it. [Brandon Dimcheff's Blog](http://brandon.dimcheff.com/2018/02/rainbow-deploys-with-kubernetes/) explains the idea well.  I even cribbed some of his Makefile to get started.
