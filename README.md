# InAppWebViewPkg

Made this because we needed to take the InAppWebViews package... make an entire app with the webview inside... and then load it on a web server to see if it works.

this is because the index.html page needs some manupilation.
so the regular in Chrome execution from Android Studio doesnt compile with that change
so after you run a flutter build web.. you then edit the index.html @ build/web folder... and then load the entire thing as a site.
YOu cant run an index.html by clicking on it on the computers folder cause it needs a web servers environment.
the glitch projects site address is https://roomy-flint-neem.glitch.me/
proj @glitch roomy-flint-neem

comes from inappwebview_pkg in flutter


later... i used a page from https://candle-far-amaranthus.glitch.me to display in this InAppWebView which worked perfectly too.

But when trying to display only a part of the above site it failed because of the Cors/SameOriginPolicy

SO next.. I loaded 2 images in the assets folder of this GitRepo. loaded them in pg2.html... then pulled this pg2.html into the 
InAppWebView with Js.evaluate(). And I was able to avoid the Cors/SameOriginPolicy error!
the Js.evaluate sets display to none on the ids of the imgs or divs... whichever you dont need.. and that disappears
