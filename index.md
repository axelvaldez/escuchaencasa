---
layout: default
title: Una lista de podcasts independientes en español para escuchar en casa durante la contingencia sanitaria.
---

<section>
  <div class="container">
    <div class="row align-items-center">
      <div class="col-12 col-lg-7">
        <h1 class="text-primary display-3 font-weight-bold">{{ site.title }}</h1>
        <h2 class="font-weight-normal">{{ page.title }}</h2>
      </div>
      <div class="col-lg-5">
        <img src="/img/header-illustration.png" alt="" class="img-fluid">
      </div>
    </div>
  </div>
</section>

<section class="bg-light-primary">
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

<div class="container-fluid bg-primary text-white">
  <section class="py-5">
    <div class="container">
      <div class="row justify-content-center text-center">
        <div class="col-lg-6">
          <h4>¡Comparte tu podcast!</h4>
          <p>Envíanos cualquier podcast que quieras ver en esta lista. Si cumple con los criterios, lo agregaremos en
            cuanto nos sea posible.</p>
          <p>
            <button type="button" class="btn btn-outline-light mr-2" data-toggle="modal" data-target="#criterios">
              Criterios
            </button>
            <button type="button" class="btn btn-light" data-toggle="modal" data-target="#podcastform">
              Compartir Podcast
            </button>
          </p>
        </div>
      </div>
    </div>
  </section>
</div>

<section class="py-5">
  <div class="container">
    <div class="row justify-content-center text-center">
      <div class="col-lg-6">
        <p>Hecho con ♥ por <a href="https://axelvaldez.mx/">Axel Valdez</a>.</p>
      </div>
    </div>
  </div>
</section>

{% include criterios.html %}
{% include form.html %}