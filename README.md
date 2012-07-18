# Web Performance Lab
An exercise in website performance optimization using best practices.

## Rule 1: Make Fewer HTTP Requests
* Combined CSS stylesheets into ubi_stylesheet_07112012.css

	This change combined all the CSS files under the resources folder
	into one stylesheet. This was done to reduce the number of requests
	required to gather all the style information. These resources were all
	hosted at the same location so could easily be concatenated.

* Combined JS files under the resources folder into ubi_scripts_07112012.js
  > All the javascript files held under the resources folder were
combined. Although the JQuery library was included, since it had been
downloaded, adding it into the shared file made sense.

* Combined promo images from the CDN into one sprite
  > Though these images may change with some frequency, stitching them
together is fast and easy, so the performance benefit is worthwhile.
The sprite used the reduced size of the images (original sizes were
100X larger than necessary) than what was originally being used by the
site, yielding a significant bandwidth savings as well.

* Change CSS and HTML to use new sprite
  > The names chosen for the ids were specific to this promo, but it
could be generalized (promo1, promo2, etc) so that only the sprite
would have to be changed. These changes may have actually made it
easier to update the images, since it is now only two lines that would
need to change (CSS background url and adding the new sprite image) as
opposed to changing all three anchor tags in the HTML in addition to
adding the three individual images.

* Combined search field images (search field and btn_on and btn_off)
and changed HTML and CSS to use it
  > Since these three images are always used together, it makes
perfect sense to combine them together.