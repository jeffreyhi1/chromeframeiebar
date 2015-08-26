Based directly on IE6Update.com plugin, ActiveBar2 and ideas from http://www.sliceratwork.com/integrate-google-chrome-frame-in-ie
Modified it to work with Chrome Frame. Just slap the code in head, using IE conditional tags (greedy like that):
```
<!--[if IE]>
    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/chrome-frame/1/CFInstall.min.js"></script>
    <script type="text/javascript" src="jquery-1.4.2.min.js"></script>
    <script type="text/javascript" src="chromeframe.js" charset="utf-8"></script>
    <script>
      $.chromeframebar({});
    </script>
<![endif]-->
```
Uses jQuery 1.4.2. Uses the MSI version of the installer (isn't an scary EXE for dumb users). Set 'use\_msi': false to download the exe version.

When the user decides to close it, he/she won't be bothered again, because it uses a cookie that expires on browser close. Will ask again when he/she closes the browser and visit the site again, or until he/she installs the chrome frame plugin! Unless you specify 'force':true to it, and will annoy the user until he/she installs the plugin.

---


# Screenshots #

## Bar showing when Chrome isn't available ##
![http://chromeframeiebar.googlecode.com/files/chromebar.jpg](http://chromeframeiebar.googlecode.com/files/chromebar.jpg)

## On mouse over ##
![http://chromeframeiebar.googlecode.com/files/chromebarhover.jpg](http://chromeframeiebar.googlecode.com/files/chromebarhover.jpg)

## After clicking it ##
![http://chromeframeiebar.googlecode.com/files/chromebarafterclick.jpg](http://chromeframeiebar.googlecode.com/files/chromebarafterclick.jpg)