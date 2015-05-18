---
layout: post
title: "css design"
description: "classes vs IDs"
category: technical
tags: [technical, phase 0]
---
{% include JB/setup %}

Apologies in advance if this comes across as a little incoherent, but this is coming after a hard week of HTML and CSS.

Classes and IDs may seem very interchangeable, given they're both even more specific attributes to add to tags in order to specify style. They tell the stylesheet to look for a specific name for the tag, so that, for example, you can two div tags with very different style attributes, so long as they both belong to different IDs or classes.

The chief difference is that an ID should only be used once on the page, while a class can be reused multiple times on the same web page. This isn't just a matter of practices and custom, but it actually matters for the HTML validation.

The reason for this is that IDs are assigned Hash values (named after hash marks, not the computer science term). Hash values are an in-page navigational aid, like assigning a heading to the section. It lets you link to later down the page, or link to a specific section of a page when setting up the addresses.

Other than this navigational aid, a class and ID are treated exactly the same by CSS, and they don't require any other formatting.