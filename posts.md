---
layout: page
title: Posts
permalink: /posts/
---

<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        {% if post.img-src %}
          <img src="{{ post.img-src }}" alt="">
        {% endif %}
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <!--{% for category in post.categories %}-->
        <!--<span>{{ category }}</span>-->
        <!--{% endfor %}-->
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe"><span class="icon-ajmn-star"></span>Subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
