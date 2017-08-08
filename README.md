# vsreddit
Visual Studio Reddit, A Reddit skin for GreaseMonkey

# how to install
- Install tampermonkey / greasemonkey
- Add a new script
- include the below script in tampermonkey
```javascript
// ==UserScript==
// @name         VSReddit
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  VSReddit Theme
// @author       You
// @match        https://*.reddit.com/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    $("head").append("<link rel='stylesheet' type='text/css' href='https://rukiaxi.github.io/vsreddit/vsreddit.css' />");
    $("head").append("<script src='https://cdnjs.cloudflare.com/ajax/libs/turbolinks/5.0.3/turbolinks.js' data-turbolinks-eval='false'></script>");
    $("li:has(a[href*='/ads/'])").hide();
    $("#srList").append($("#openRESPrefs"));
    
    document.addEventListener("turbolinks:load", function() {
        $("li:has(a[href*='/ads/'])").hide();
        $("#srList").append($("#openRESPrefs"));
    });
})();
```

> Note, we're currently working on getting a tampermonkey script available on our github page
> Please use the above script until we created the tampermonkey script