# element-css-path

Javascript library and jQuery plugin for determining the CSS path of an HTML DOM element.

## Usage with jQuery (jquery.element-css-path.js)

```javascript
$(element).elementCssPath(options);
```

Example:

```html
<head>
	<script src="jquery.min.js"></script>
	<script src="jquery.element-css-path.min.js"></script>
</head>
<body>
	<div id="wrapper">
		<div id="content">
			<div id="sidebar">
				get the path of this!
			</div>
		</div>
	</div>
</body>
```

```javascript
$("#sidebar").elementCssPath();
// returns: html body div#wrapper div#content div#sidebar
```

## Usage alone (element-css-path.js)

```javascript
ElementCssPath(element, options);
```

Example:

```html
<head>
	<script src="element-css-path.min.js"></script>
</head>
<body>
	<div id="wrapper">
		<div id="content">
			<div id="sidebar">
				get the path of this!
			</div>
		</div>
	</div>
</body>
```

```javascript
ElementCssPath(document.getElementById("sidebar"));
// returns: html body div#wrapper div#content div#sidebar
```

## Options
Customize the functionality with the following options:

### `unique` (default: `false`)
A boolean, if true, path contains a unique route to the element using the pseudo selector :nth-child.

### `directDescendant` (default: `false`)
A boolean, if true, path contains the direct descendant operator (>) for all the elements.

### `startWithClosestID` (default: `false`)
A boolean, if true, path begins with the first element with an ID up the ancestor tree. E.g. `html body div#wrapper div#nav ul li a` would be shortened to `div#nav ul li a`.


## Browser Support

* IE 5.5+
* Chrome
* Firefox
* Safari
* Opera

## License

Distributed under the MIT license.

