# resources-template

A static HTML page that is a shortcut to the most common downloads and requirements of the college (unprotected).  Adapted for public usage.

Used to help students install software.  Appears with tiles and a search menu.


# Creating Icons

All icons must be jpg format.  All icons must be 228 x 228 pixels.  All icons must go in `img/icon/`.


# Adding New Tiles

There are two types of tiles that can be added.  Either one that goes directly to a website (type 1) or opens a pop up window.

## Type 1 - Direct

1. Copy the below template and change the fields in the below list.
- `href=""` - The URL that your tile redirects to.
- `src=""` - The location and name of your image.  Put into the `img/icon` folder.  
- `<h2>` - The name that appears on the tile.  Keep it short.
- `<p>` - The description of the tile.  Keep it short.
- `<p>` - The label to apply to your tile.

**Example (Google Chrome Tile)**
```html
<li><a target="_blank" href="https://www.google.com/chrome/">
    <img src="img/icon/chrome.jpg" class="ui-li-thumb">
    <h2>Google Chrome</h2>
    <p>Google Chrome Browser</p>
    <p class="ui-li-aside">External</p>
</a></li>
```

2. Insert it in the section of index.htm that is commented for tiles.

That's it!

## Type 2 - Pop Up

Copy the below template and change the fields in the below list:
- `href=""` - The Name that you give your popup box in step 3.
- `src=""` - The location and name of your image.  Put into the `img/icon` folder.  
- `<h2>` - The name that appears on the tile.  Keep it short.
- `<p>` - The description of the tile.  Keep it short.
- `<p>` - The label to apply to your tile.


**Example (SSL Cert Tile)**
```html
<li><a href="#sslcert-popup" data-rel="popup" data-position-to="window" data-transition="pop">
    <img src="img/icon/sslcert.jpg" class="ui-li-thumb">
    <h2>SSL Certificate</h2>
    <p> SSL Certificate for Internet </p>
    <p class="ui-li-aside">Internet</p>
</a></li>
```

2. Insert it in the section of index.htm that is commented for tiles.

3. Copy the below template and update the following fields:
- comment - you may want to update the comment `<!-- COMMENT -->`
- `id=""` - The name of the popup you used in step 1.
- `<h1>` - The title you want on your pop up box.
- `<h3>` - The description or instruction you want on your popup box.
- `<a href=""` - You can have as many buttons as you like, the example has three buttons.  Each button needs the URL updated, img src"" and description.
- `<p>` - (Optional) Description after all the buttons

**Example (SSL Cert Pop Up)**
```html
<!-- SSL CERTIFICATE -->
<div data-role="popup" id="sslcert-popup" data-overlay-theme="b" data-theme="b" data-dismissible="true">
    <div data-role="header" data-theme="a">
    <h1>Software Version</h1>
    </div>
    <div role="main" class="ui-content">
        <h3 class="ui-title">Please select your operating system from below.</h3>
        <a href="http://resources.maristns.catholic.edu.au/download/ssl/windows-installSSLCertificate2018.exe" class="ui-btn ui-corner-all ui-shadow ui-btn-inline ui-btn-b" target="_blank"><img src="img/windows.svg" width="50"> <br /> Windows </a>
        <a href="http://resources.maristns.catholic.edu.au/download/ssl/macos-installSSLCertificate2018.pkg" class="ui-btn ui-corner-all ui-shadow ui-btn-inline ui-btn-b" target="_blank"><img src="img/mac.png" width="50"> <br /> Mac OSX </a>
        <a href="http://resources.maristns.catholic.edu.au/download/ssl/ZscalerSHA256.crt" class="ui-btn ui-corner-all ui-shadow ui-btn-inline ui-btn-b" target="_blank"><img src="img/icon/cert.png" width="50"> <br /> Cert File </a>
        <p> Updated: 01/01/2020 </p>
    </div>
</div>
```

4. Insert the above modified code into the index.htm file that is commented for popups.

5. That's it!