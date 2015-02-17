# Share Buttons

**IN DEVELOPMENT**: I will post news of release on [my Twitter](http://twitter.com/sunnyismoi) and [my blog](http://sunnyis.me/blog/).

Social share buttons provided by Twitter, Facebook, and others allow you to easily add social sharing to your web page with a quick copy-and-paste. However, they add overhead and will increase load time. Chances are, all you want are good-looking buttons that allow your users to share a URL to their feeds. Here's where the Share Buttons project comes in.

Share Buttons allows you to implement simple sharing functionality through HTML, CSS, and JS that you can host on your site. You can view the demo and documentation below.

## Demo

You can view and interact with the [demo on CodePen](http://codepen.io/sunnysingh/pen/OPxbgq).

## Install

Available through [Bower](http://bower.io/):

```
bower install share-buttons
```

## Documentation

### CSS

Include `share-buttons.css` file in the `build` folder (or @import if using Less):

```html
<!-- Inlude in <head> tag -->
<link rel="stylesheet" href="build/css/share-buttons.css" />
```

The `share-buttons.css` file includes social icons, which come from the `fonts` folder. You can use the `share-buttons-no-icons.css` file if you are using your own icons or want text-only buttons.

### JS

If you want the sharing URL to open in a popup window/dialog, you can include the `share-buttons.js` file. This is pure JavaScript that does not rely on any framework, but may not work in older browsers. You can include the `share-buttons.jquery.js` file if you're using jQuery.

```html
<!-- Include before </body> closing tag -->
<script src="build/js/share-buttons.js"></script>
```

### Markup

The least amount of markup required for a button:

```html
<a class="share-btn share-btn-{SHARE_SERVICE}"
   href="{SHARE_URL}"
   title="Share">
	<span class="share-btn-icon"></span>
	<span class="share-btn-text">Share</span>
</a>
```

As you can see, it's simply an anchor tag with the `href` attribute linking to the share URL of the service.

The `.share-btn-{SHARE_SERVICE}` class is used to show the proper icon and `{SHARE_URL}` is the sharing URL for the service.
You can find the list of services along with their share URLs below:

* Twitter (share-btn-twitter): `https://twitter.com/share?text=Share Buttons Demo&url=`
* Facebook (share-btn-facebook): `https://www.facebook.com/sharer/sharer.php?u=`
* Google+ (share-btn-googleplus): `https://plus.google.com/share?url=`
* Reddit (share-btn-reddit): `http://www.reddit.com/submit?url=`
* Tumblr (share-btn-tumblr): `http://www.tumblr.com/share/link?url=`
* LinkedIn (share-btn-linkedin): `https://www.linkedin.com/shareArticle?mini=true&url=`
* Pinterest (share-btn-pinterest): `https://www.pinterest.com/pin/create/button/?url=`
* Delicious (share-btn-delicious): `https://delicious.com/save?v=5&noui&jump=close&url=`

Your page's URL typically goes after the `?url=` part, and must be encoded.

#### Button classes

You can change the way the buttons look with classes. Just add one or more of the following classes to the `a` tag:

* `share-btn-sm` or `share-btn-lg` for different sizes.
* `share-btn-branded` for a colorized button.
* `share-btn-inverse` for a dark-scheme.

If you want to make a button that only shows the icon (no text), make sure to use the following markup for the text span:
```html
<span class="share-btn-text-sr">Share</span>
```

This way, the buttons stay accessible to screen reader users.