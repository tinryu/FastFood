[jQuery gallery elevatezoom](http://www.elevateweb.co.uk/image-zoom/)
================================

Demo gallery elevatezoom (zoom+fancybox)


## Getting Started

Include jQuery and the plugin on a page. Include your images and initialise the plugin.

```html
<!--LIB-->
<script src='jquery-1.11.0.min.js'></script>
<script src='jquery.elevateZoom-3.0.8.min.js'></script>
<link href="fancybox/jquery.fancybox.css" rel="stylesheet" type="text/css" />
<script src='fancybox/jquery.mousewheel-3.0.6.pack.js' type='text/javascript'></script>		
<script src='fancybox/jquery.fancybox.js' type='text/javascript'></script>
<!--LIB-->
<div class="man0img">
	<img id="zoom_01" src='images/small/image1.png' data-zoom-image="images/large/image1.jpg"/>
</div>
<div id="slide-detail-carousel-1">
	<a class="item" href="#" data-image="images/small/image1.png" data-zoom-image="images/large/image1.jpg">
	<img id="zoom_01" src="images/thumb/image1.jpg" />
	</a>

	<a class="item" href="#" data-image="images/small/image2.png" data-zoom-image="images/large/image2.jpg">
	<img id="zoom_01" src="images/thumb/image2.jpg" />
	</a>

	<a class="item" href="#" data-image="images/small/image3.png" data-zoom-image="images/large/image3.jpg">
	<img id="zoom_01" src="images/thumb/image3.jpg" />
	</a>

	<a class="item" href="#" data-image="images/small/image4.png" data-zoom-image="images/large/image4.jpg">
	<img id="zoom_01" src="images/thumb/image4.jpg" />
	</a>

</div>
javascript
<script>
    $(document).ready(function () {
			$('.fancybox').fancybox();

			$("#zoom_01").elevateZoom({
				gallery:'slide-detail-carousel-1', 
				cursor: 'pointer', 
				galleryActiveClass: 'active', 
				imageCrossfade: true,
				loadingIcon: 'http://www.elevateweb.co.uk/spinner.gif'
			}); 
			//pass the images to Fancybox
			$("#zoom_01").bind("click", function(e) {  
			  var ez =   $('#zoom_01').data('elevateZoom');	
				$.fancybox(ez.getGalleryList());
			  return false;
			});
		});
</script>
Css Plus
<style type="text/css">
	#slide-detail-carousel-1 img{
		border:2px solid white;
	}
	.active img{
		border:2px solid #333 !important;
	}
</style>
```

For more information on how to setup and customise, [check the examples](http://www.elevateweb.co.uk/image-zoom/examples).

## License
Copyright (c) 2012 Andrew Eades
Dual licensed under the GPL and MIT licenses.
