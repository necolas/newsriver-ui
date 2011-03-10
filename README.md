#  NewsRiver UI

## Changelog:

### v.0.5.0 : 9 March 2011

#### General
* Added a favicon and apple-touch-icon.
* Added _json-example.js; only used for localhost debugging.
* Switched to Google CDN jQuery (with local fallback).
* Switched to local jQuery Templates plugin.

#### index.html
* Removed HTML5 elements and shim; IE cannot style HTML5 elements generated from the jQuery templates.
* Added X-UA-Compatible to force latest IE rendering engine and enable Chrome Frame.
* Changed meta viewport to `width=device-width, initial-scale=1.0`.
* Default JSON url, JSON callback, and social sharing settings can be overriden in `River.settings` in the document head.
* Added ARIA landmark roles.
* Default text now indicates that JavaScript is required.
* Added RSS image to footer.
* Updated footer's fine-print.

##### jQuery template
* Stream item titles are now hyperlinks only if there is an `item.permalink` or `item.link`.
* Each stream item's `id` is added to its container element. Used to check if new items exist in the stream.
* Conditional display of Twitter and Facebook sharing links.
* All stream items are contained within `<div id="stream-items">`.
* Notification of updates to the feed are shown in `<div id="stream-notice">`.

#### default.css
* Removed individual article borders to reduce visual clutter.
* Added a marker to indicate which item was previously the most recent, prior to stream update. Only visible in expanded view.

#### custom.js
* Complete rewrite of the scripts (including use of namespacing).
* Loading message only present if JavaScript is enabled.
* Regular checks for updates to the JSON feed.
* Displays the number of new items available.
* Repopulates the stream when the notice is clicked.
* Changed the way the datetime format used on blocks of updates. Time comes last, no longer displays seconds.

## Summary:

This is a client-side, river of news UI. It is created to display a JSONP file that is generated using Dave Winer's [River2](http://newsriver.org/river2.html) software.

### River resources

* [River of News (Google Group)](http://groups.google.com/group/river-of-news)
* [How to: River2 is a River of News](http://newsriver.org/river2.html)
* [How to: EC2 for Poets](http://ec2.scripting.com/)
* [OPML Editor](http://editor.opml.org/)

## License:

MIT/GPL license