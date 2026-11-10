---
layout: default
title: About
hero: large
---

<section class="intro">
  <h1 class="display">{{ site.title }}</h1>
  <p class="lede">I'm an astronomer studying how young stars and their planet-forming disks are shaped by the material around them, using ALMA observations of gas and dust.</p>
</section>

<!-- Edit everything below. Plain Markdown works here. -->

I'm a [your position] at [your institution]. My research focuses on protoplanetary disk dynamics, infalling streamers, and the molecular line and dust tracers that let us see them.

Much of my recent work centers on GW Ori, a young triple star system surrounded by a large disk, where I use CO observations to trace material falling in from the surrounding cloud.

Outside of research, I [a sentence about outreach, interests, or anything else you'd like visitors to know].

<ul class="link-list link-list--intro">{% for link in site.links %}<li><a href="{{ link.url }}">{{ link.label }}</a></li>{% endfor %}</ul>
