# vsreddit
Visual Studio Reddit, A Reddit skin for GreaseMonkey

# how to install
- Install tampermonkey / greasemonkey
- Add a new script
- include the below script in tampermonkey
```javascript
// ==UserScript==
// @name         VSReddit
// @namespace    https://rukiaxi.github.io/vsreddit/
// @version      0.1
// @description  Make reddit look like VSCode
// @author       Sem Wong
// @match        https://*.reddit.com/*
// @grant        none
// @require https://code.jquery.com/jquery-2.1.4.min.js
// ==/UserScript==

(function() {
    'use strict';
    var link = document.createElement('LINK');
    link.rel = 'stylesheet';
    link.href = 'https:/rukiaxi.github.io/vsreddit/vsreddit.css';
    link.type = 'text/css';
    document.body.insertBefore(link, null);
})();
```

> Note, we're currently working on getting a tampermonkey script available on our github page
> Please use the above script until we created the tampermonkey script