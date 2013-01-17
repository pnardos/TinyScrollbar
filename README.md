## Tiny Scrollbar

Fork of **Tiny Scrollbar** &mdash; a lightweight jQuery plugin. Styled minimalistic scrollbar, with update animation and HTML generation if container hasn't. Originally created by [Maarten Baijs](http://www.baijs.nl/), v1.81.

### Features

* iPhone, iPad, Android support!
* New in 1.8. You can now drag the content on mobile devices!
* Can scroll vertical or horizontal.
* Supports scrolling by wheel, thumb, track or touch.
* It has a update function so it can handle content changes.
* Size of the scrollbar and thumb can be set to auto or a fixed number.
* Easy customizable.
* Supports normal scrolling and mobile style invert scrolling.
* Lightweight: it's only 200 lines of code. Mimified size is above 4KB.

### Modifications

Changes by [Annexare Studio](http://annexare.com/):

* HTML markup generation, so can be used with any block without special structure, all wrappers will be created automatically.
* CSS classes prefixes.
* Default theme, close to OS X styles (to be updated yet).
* Update scrolling animation, if used.
* jQuery UI class "ui-corner-all" is added, but border radius can be easily overriden.

### Usage

```html
	<div class="scrollbar">This block will have a scrollbar. Should have more content actually.</div>
```

```js
	$(document).ready(function(){
		// define scrollbars
		$(".scrollbar").tinyscrollbar({
			prefix: "",
			updateTime: 200
		});
		// update block when changed
		// accepts 1 param:
		// - 'top' (if none) or 'bottom';
		// - 'relative' sets the position of the scrollbar relative to the old content when new content is passed in;
		// - integer, to move to a certain location in the content.
		$(".scrollbar").tinyscrollbar_update();
	});
```

```css
	.scrollbar { clear: both; margin: 0;}
	.scrollbar .viewport { overflow: hidden; position: relative;}
	.scrollbar .overview { list-style: none; position: absolute; left: 0; top: 0;}
	.scrollbar .thumb { background-color: rgba(85,85,85,.8);}
	.scrollbar .bar { position: relative; float: right; width: 8px;}
	.scrollbar .track { background-color: rgba(34,34,34,.5); height: 100%; width: 8px; position: relative; padding: 0;}
	.scrollbar .track:hover,
	.scrollbar .active .track { background-color: rgba(34,34,34,.7);}
	.scrollbar .track:hover .thumb,
	.scrollbar .active .thumb { background-color: rgba(153,153,153,.9);}
	.scrollbar .thumb { height: 20px; width: 8px; cursor: pointer; overflow: hidden; position: absolute; top: 0;}
	.scrollbar .thumb:hover { background-color: rgba(153,153,153,.9);}
	.scrollbar .thumb .end { overflow: hidden; height: 0; width: 8px;}
	.scrollbar .disable { display: none;}
	.noSelect { user-select: none; -o-user-select: none; -moz-user-select: none; -khtml-user-select: none; -webkit-user-select: none;}
```
