---
layout: defaults
title: Home
---

  <script type="module">
    import PhotoSwipeLightbox from 'assets/js/photoswipe-lightbox.esm.js';
    const lightbox = new PhotoSwipeLightbox({
      gallery: '#my-gallery',
      children: 'a',
      pswpModule: () => import('assets/js/photoswipe-lightbox.esm.min.js')
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