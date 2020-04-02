---
layout: default
title: Una lista de podcasts independientes en español para escuchar en casa durante la contingencia sanitaria.
---

<section>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <h1>{{ site.title }}</h1>
        <h2>{{ page.title }}</h2>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container">
    <div class="row">
      {% for podcast in site.data.podcasts.list %}

      <div class="col-lg-6 mb-5 pb-5">
        <div class="row">
          <div class="col-4">
            <img src="/img/{{ podcast.image }}" alt="{{ podcast.name }}" class="img-fluid shadow">
          </div>
          <div class="col-8">
            <h3>{{ podcast.name }}</h3>
            <p>{{ podcast.description }}</p>
            <p class="mb-0 links">
              {% unless podcast.apple == nil %}
              <a href="{{ podcast.apple }}"><span>Apple</span></a>
              {% endunless %}
              {% unless podcast.google == nil %}
              <a href="{{ podcast.google }}"><span>Google</span></a>
              {% endunless %}
              {% unless podcast.spotify == nil %}
              <a href="{{ podcast.spotify }}"><span>Spotify</span></a>
              {% endunless %}
            </p>
          </div>
        </div>
      </div>

      {% endfor %}

    </div>
  </div>
</section>

<div class="container-fluid bg-dark text-white">
  <section>
    <div class="container">
      hello
    </div>
  </section>
</div>