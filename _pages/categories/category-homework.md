---
title: "Homework"
layout: archive
permalink: /categories/homework/
author_profile: true
sidebar_main: true
---


{% assign posts = site.categories.homework %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}