---
title: My custom title
---
    <link rel="stylesheet" href="node_modules/photoswipe/dist/photoswipe.css">
    <style>
      .thumbnail200 {
        width:200px;
        height:200px;
      }
    </style>
  </head>
  <body>
	<script type="module">
import PhotoSwipeLightbox from '../node_modules/photoswipe/dist/photoswipe-lightbox.esm.js';
const lightbox = new PhotoSwipeLightbox({
  gallery: '#my-gallery',
  children: 'a',
  pswpModule: () => import('../node_modules/photoswipe/dist/photoswipe.esm.js')
});
lightbox.init();
</script>

{% for counter in (0..9) %}
  <!-- the stuff to be done followed by an increase in the 'counter' variable -->
    {{ counter }}
{% endfor %}


# array = [1,2,3,4,5,6]
{% for item in array limit:2 offset:2 %}
  {{ item }}
{% endfor %}
# results in 3,4 


<div class="pswp-gallery" id="my-gallery">
    <a href="img/Offroadents - 1.PNG" 
      data-pswp-width="1024" 
      data-pswp-height="1024" 
      target="_blank">
      <img src="img/Offroadents - 1.PNG" class="thumbnail200" alt="" />
    </a>

    <a href="img/Offroadents - 1.PNG" 
      data-pswp-width="1024" 
      data-pswp-height="1024" 
      target="_blank">
      <img src="img/Offroadents - 1.PNG" class="thumbnail200" alt="" />
    </a>
  </div>

  

  </body>
</html>
