---
layout: default
title: "MoMI From Home"
---

{% for post in site.posts %}

  <div class="card card-bordered bg-{{ post.color }} clr-{{ post.color }} mb-3">
    <div class="card-body bg-white text-dark">
      <div class="row align-items-center">
        <div class="col-lg-4">
          <img src="{{ post.img_src }}" class="card-img" alt=" {{ post.title }}">
        </div>
        <div class="col-lg-8 py-2">
          <h5 class="card-title">{{ post.title }}</h5>
          <h6 class="card-subtitle mb-2 text-muted">{{ post.date | date: "%B %-d, %Y"  }}</h6>
          <p>{{ post.content }}</p>
          <div class="card-footer text-muted">
          <b>Category:</b> <i>{{ post.category }}</i><br>
          {% if post.tags.size > 0 %}
            <b>Tag{% if post.tags.size > 1 %}s{% endif %}</b>:
            <i>{{ post.tags | sort | join: ", " }}</i>
          {% endif %}
          </div>
        </div>
      </div>
    </div>
  </div>

{% endfor %}
