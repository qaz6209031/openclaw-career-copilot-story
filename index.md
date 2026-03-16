---
layout: default
title: Kai's OpenClaw Stories
---

# OpenClaw stories

This repo is set up as a single GitHub Pages site for publishing article pages that can be imported into Medium drafts.

<div class="story-list">
{% assign sorted_stories = site.stories | sort: 'title' %}
{% for story in sorted_stories reversed %}
  <a class="story-card" href="{{ site.baseurl }}{{ story.url }}">
    <div class="eyebrow">Story</div>
    <h2 style="margin: 8px 0 6px;">{{ story.title }}</h2>
    {% if story.description %}<p class="muted" style="margin:0;">{{ story.description }}</p>{% else %}<p class="muted" style="margin:0;">Open public page</p>{% endif %}
  </a>
{% endfor %}
</div>

<p class="footer-note">Each story gets a stable public URL under <code>/stories/&lt;slug&gt;/</code>, which makes it easy to feed into Medium's Import story flow.</p>
