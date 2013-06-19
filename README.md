Preload.js 1.0.0
=====

A light Javascript library made to preload images and display a progress bar


Documentation
=====


Abstract
------

Preload.js is a Javascript library that was made to simplify images preload and to automatically manage a loading progress bar.

The main idea is that you can choose the files to be preloaded, and the scripts does it all.
The page content is hidden, the progress bar is displayed until all the images are loaded. Then you are shown the page back.


Installation and configuration
------

- Download the Preload.js file and paste it in your "js" directory
- Download the preload.css file and paste it in your "css" directory
- In the HEAD of the HTML document, include a link to the CSS:

```html
<link rel="stylesheet" type="text/css" href="css/preload.css" />
```

- WARNING: the content of your web document must be all included in a
	
```html
<div id="wrapper">...</div>
```

- At the bottom of the BODY, include a link to the JS :

```html
<script type="text/javascript" src="js/Preload.js"></script>
```

- Just after, create a <SCRIPT> tag and paste the following:

```html
// List the resources to be loaded here:
var elements = [
	/* Customize the files list: */
	'img/bg-content-01.jpg',
	'img/bg-content-02.jpg',
	'img/bg-content-03.jpg',
	'img/bg-content-04.jpg',
	'img/bg-content-05.jpg'
];

// Preload instance: 
var preload = new Preload();

// Preload initialization with the elements to be loaded and a callback method: 
preload.init( 'wrapper', elements, function() {
	// This is the callback method called after the preload finishes, and after the #wrapper content is displayed again 
	// You can customize here: 
	alert('Resources loaded!');
});
```

- Then if you want to customize the look of the progress bar, feel free to modify the preload.css content.

Changelog
=====

1.0.0 (2013-06-18)
-----

* Initial project


Contributors
=====

* [Rémy Vuong, repo owner, main contributor](https://github.com/rvuong)
