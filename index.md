---
title: Offroadents
---

<html>

<head>
  <meta charset="utf-8">
  <title>{{ page.title }}</title>
  <link rel="stylesheet" href="node_modules/photoswipe/dist/photoswipe.css">
  <style>
    .thumbnail200 {
      width: 200px;
      height: 200px;
    }
  </style>

  <script type="module">
    import PhotoSwipeLightbox from './node_modules/photoswipe/dist/photoswipe-lightbox.esm.js';
    const lightbox = new PhotoSwipeLightbox({
      gallery: '#my-gallery',
      children: 'a',
      pswpModule: () => import('./node_modules/photoswipe/dist/photoswipe.esm.js')
    });
    lightbox.init();
  </script>

  {% for counter in (1..35) %}

  <div class="pswp-gallery" id="my-gallery">
    <a href="assets/images/Offroadents - {{ counter }}.PNG" data-pswp-width="1024" data-pswp-height="1024"
      target="_blank">
      <img src="assets/images/Offroadents - {{ counter }}.PNG" class="thumbnail200" alt="" />
    </a>

  </div>
  {% endfor %}
