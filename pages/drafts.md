---
layout: default
title: Drafts
permalink: /drafts/

hidden_in:
  - production
robots: noindex
---

<div class="home">

  <h1 class="page-heading">Draft Posts</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      {% if post.draft %}
        <li>
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>

          {{ post.excerpt }}
        </li>
      {% endif %}
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
