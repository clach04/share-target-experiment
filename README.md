# share-target-experiment

share target experiments / PWA - probably not working

Currently based on https://github.com/w3c/web-share-target/tree/main/demos
NOT working via ngrok.
w3c/web-share-target can work by serving w3c dir with demo python web server and ngrok.
NOTE NOTE to speed up install, try opening <a href="manifest.json">manifest.json</a> and <a href="sw.js">sw.js</a> manually (maybe required for ngrok with abuse protection?)


    echo Issue:
    echo        ngrok http 7878
    py -3 -m http.server 7878

  * http.server works for w3c demo
  * Caddy2 works for w3c demo
  * It does NOT work for w3c demo when using this wsgi debug server :-(

TODO try this demo with same URL pwa.html INSTEAD of submit URL.

See:

  * https://w3c.github.io/web-share/demos/
      * https://w3c.github.io/web-share/demos/share.html
      * https://w3c.github.io/web-share/demos/share-files.html

## Demo

### Windows

    set PORT=7878
    set ALWAYS_RETURN_404=false

    echo http://localhost:%PORT%
    echo http://localhost:%PORT%/pwa.html
    echo http://localhost:%PORT%/icons/icon-512.png

    py -3 debugserver2_wsgi_class.py
    python debugserver2_wsgi_class.py

### Linux / Unix

    export PORT=7878
    export ALWAYS_RETURN_404=false

    echo http://localhost:$PORT
    echo http://localhost:$PORT/pwa.html
    echo http://localhost:$PORT/icons/icon-512.png

    py -3 debugserver2_wsgi_class.py
    python debugserver2_wsgi_class.py

## Additional resources

### Documentation

  * https://web.dev/web-share-target/
  * https://w3c.github.io/web-share-target/ 
  * https://developer.mozilla.org/en-US/docs/Web/API/Web_Share_API
      * https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Tutorials/js13kGames/Installable_PWAs#requirements
      * https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Installing
      * https://addons.mozilla.org/en-US/firefox/addon/pwas-for-firefox/
  * https://dev.to/nicomartin/share-target-api-5263 https://support.google.com/chrome/answer/9658361?hl=en&co=GENIE.Platform%3DAndroid
  * https://github.com/GoogleChrome/samples/blob/gh-pages/web-share/README.md#web-share-demo 
  * https://web.dev/articles/web-share - talks about:
      * web-share (to local apps) from within a browser
      * web-share-target for sharing to a custom PWA/Server (i.e. share from a native app to web/PWA)

### Samples

  * https://github.com/GoogleChrome/samples/blob/gh-pages/web-share/README.md#web-share-demo 

  * file upload https://github.com/GoogleChromeLabs/squoosh  
  *  URL https://ytaud.io/
      * https://github.com/nico-martin/yt-audio
      * https://github.com/nico-martin/yt-audio-source

