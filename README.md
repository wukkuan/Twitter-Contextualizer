Twitter Contextualizer
============================

Twitter Contextualizer keeps your context on the
[twitter.com](https://twitter.com) when loading new tweets. By default, Twitter
simply loads the new tweets and doesn't scroll the page or make any indication
as to where you were. This script attempts to fix that issue by scrolling the
page such that the last read tweet is at the bottom, and marking it.


Usage
-----

### Greasemonkey / Chrome Extension
This plugin can be installed via [Userscripts.org](https://userscripts.org/) by visiting the script's [page](http://userscripts.org/scripts/show/147403).

### Bookmarklet
This script can be used as a bookmarklet as well, but keep in mind you'll have to click it each time you load the [twitter.com](https://twitter.com). Just copy and paste the following code into a bookmark's URL.

    javascript:(function(){var e=$(".stream-container"),t=$(".tweet:first").parent(),n=!1;$("body").ajaxComplete(function(e,r,i){if(n&&i.url.indexOf("/i/resolve.json")!==-1){n=!1;var s=$(t).offset().top,o=$(t).height(),u=s+o,a=$(window).height(),f=u-a;$("html, body").animate({scrollTop:f},500)}}),e.delegate(".new-tweets-bar:parent","click",function(e){t=$(".tweet:first").parent(),t.css({backgroundColor:"lightgrey"}),n=!0})})();

    
Issues
------

If you have any issues, feel free to contact me directly and I'll work to help you through it.

Email/Jabber - williamblasko@gmail.com  
Twitter - [@wukkuan](https://twitter.com/wukkuan)


License
-------
All of Twitter Contextualizer is licensed under the MIT license.

Copyright (c) 2012 William Blasko <williamblasko@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
