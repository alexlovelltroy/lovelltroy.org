+++
# Date this page was created.
date = "2018-04-15"

# Project title.
title = "Generate DNS and DHCP for your home network"

# Project summary to display on homepage.
summary = "Create internal dhcp/dns configurations for OpenBSD-based routers"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "scaled/presidencia.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["programming", "devops", "OpenBSD", "nsd", "unbound", "tftpd"]

# Optional external URL for project (replaces project detail page).
# external_link = "https://github.com/alexlovelltroy/gendomains/"

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/header-presidencia.jpg"
caption = "My caption :smile:"

+++

I run my home network behind an OpenBSD router for historical reasons.  I keep the initial configuration for it in (Packer and Ansible)[http://github.com/alexlovelltroy/openbsd-router], and try to treat it as an appliance rather than a computer I play with.  Some time ago, I wrote a quick python script to generate a purely internal domain structure.  That means a dhcpd.conf file and a corresponding domain zonefile and reverse DNS zone file for nsd.  Both of those need to be intercepted by the unbound configuration file for internal resolution.

 