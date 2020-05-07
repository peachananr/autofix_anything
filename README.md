#Auto Fix Anything by Pete R.
This little plugin will let you automatically fix position of any container on your website with one JS call
Created by [Pete R.](http://www.thepetedesign.com), Founder of [BucketListly](http://www.bucketlistly.com)


## Demo
[View demo](http://peachananr.github.io/autofix_anything/Demo/autofix_demo.html)

## Compatibility
Modern browsers such as Chrome, Firefox, and Safari, on desktop have been tested.

## Basic Usage
With this plugin you can dynamically fix a container within the viewport with one JS call. The plugin will detect when to fix/unfix the position automatically.

To add this to your website, simply include the latest jQuery library together with `jquery.autofix_anything.js` and `autofix_anything.css` into your document's `<head>` and call the function as follows:

  
````javascript
$(".sidebar").autofix_anything({
  customOffset: false, // You can define custom offset for when you want the container to be fixed. This option takes the number of pixels from the top of the page. The default value is false which the plugin will automatically fix the container when the it is in the viewport
  manual: false, // Toggle this to true if you wish to manually fix containers with the public method. Default value is false
  onlyInContainer: true // Set this to false if you don't want the fixed container to limit itself to the parent's container.
});
````

Although, the HTML and CSS structures below are not mandatory, following it will help the plugin perform better out of the box

````html
<div class="wrapper">
  ..
  <div class="sidebar">..</div>
  ..
</div>
````

````css
.wrapper {
  position: relative;
}
````

## Public Method
You can also fix your containers programmatically as well:

### $.fn.manualfix()

This method will let you toggle the fix state of the container. The method will detect whether to fix or not to fix based on the current state. 

Note: Make sure the `manual` option of the main function call is toggled to true.

````javascript
$(".sidebar").autofix_anything({
  manual: true
});
````
and call this function anywhere you like to toggle it.

````js
$(".sidebar").manualfix()
````

If you want to see more of my plugins, visit [The Pete Design](http://www.thepetedesign.com/#design), or follow me on [Twitter](http://www.twitter.com/peachananr) and [Github](http://www.github.com/peachananr).

## Other Resources
- [Tutorial](http://www.onextrapixel.com/2013/11/18/fix-any-div-container-into-view-port-with-autofix_anything-js/)
