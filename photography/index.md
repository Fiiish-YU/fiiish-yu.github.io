---
layout: default
title: 摄影杂谈
description: 摄影作品和拍摄时的点滴
permalink: /photography/
---

这里记录镜头里的风景，也记录按下快门时的心情。

<div class="photo-wall">
  {% assign moments = site.photography | sort: "date" | reverse %}
  {% if moments.size > 0 %}
    {% for moment in moments %}
      {% assign image_count = moment.images | size %}
      <article class="photo-moment">
        <header class="photo-moment__header">
          <h2 class="photo-moment__title">{{ moment.title | escape }}</h2>
          <time class="photo-moment__date" datetime="{{ moment.date | date_to_xmlschema }}">
            {{ moment.date | date: "%Y年%m月%d日" }}
          </time>
        </header>
        {% if moment.caption %}
          <p class="photo-moment__caption">{{ moment.caption | escape }}</p>
        {% endif %}
        {% if image_count > 0 %}
          <div class="photo-grid photo-grid--{{ image_count | at_most: 12 }}">
            {% for image in moment.images limit:12 %}
              <a class="photo-grid__item" href="{{ image.src | relative_url }}">
                <img src="{{ image.src | relative_url }}" alt="{{ image.alt | default: moment.title | escape }}" loading="lazy">
              </a>
            {% endfor %}
          </div>
        {% endif %}
      </article>
    {% endfor %}
  {% else %}
    <p class="photo-wall__empty">还没有摄影动态，期待第一张照片。</p>
  {% endif %}
</div>
