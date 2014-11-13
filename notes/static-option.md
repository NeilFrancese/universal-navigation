## Option #2: Simple iFrame Universal Navigation & Footer

##### Using Internet Explorer? Be sure you are not running in "_Compatibility Mode_" when testing:
> Press the `F12 Key`, and click "Internet Explorer X Compatibilty Mode" and change to latest non-compatibility mode from the dropdown

> **Defaulting to compatibility mode is a byproduct of IE's "intranet" settings**. While testing internally, you will experience this issue, even on closing and re-opening a browser window. **_EXTERNAL USERS WILL NOT EXPERIENCE THIS ISSUE_**. Please don't file issues about Compatibility mode unless you can replicate outside of NY networks. Thanks.

___!!! Place this code at the very top of your site, outside of any container divs, and as close to the opening \<body\> tag as possible. The header should expand to 100% of the screen width, even if your current site has a fixed width. !!!___


```html
<iframe id="nygov-universal-navigation-frame" class="nygov-universal-container" width="100%" height="86px" src="//static-assets.ny.gov/load_global_menu/ajax?iframe=true" data-updated="2014-11-07 08:30" frameborder="0" style="border:none; overflow:hidden; width:100%; height:86px;" scrolling="no">
            Your browser does not support iFrames
</iframe>
<!-- Google Tag Manager -->
    <noscript><iframe src="//www.googletagmanager.com/ns.html?id=GTM-T4FP6H" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
    <script type="text/javascript">(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0];var j=d.createElement(s);var dl=l!='dataLayer'?'&l='+l:'';j.src='//www.googletagmanager.com/gtm.js?id='+i+dl;j.type='text/javascript';j.async=true;f.parentNode.insertBefore(j,f);})(window,document,'script','dataLayer','GTM-T4FP6H');</script>
<!-- End Google Tag Manager -->
```

### Footer Embed Code (pair with static banner)

 ___!!! Place this code at the very bottom of your site, outside of any container divs, as close to and before the closing \<body\> tag. The footer should expand to 100% of the screen, even if your current site has a fixed width. !!!___

```html
<iframe id="nygov-universal-footer-frame" class="nygov-universal-container" width="100%" height="200px" src="//static-assets.ny.gov/load_global_footer/ajax?iframe=true" data-updated="2014-11-07 08:30" frameborder="0" style="border:none; overflow:hidden; width:100%; height:200px;" scrolling="no">
            Your browser does not support iFrames
</iframe>
```

### Hiding the uNav when printing

The content inside the static uNav is automatically hidden when printed, however the `<iframe>` will leave a noticeable blank area on a print page. To hide this blank area add the following CSS to your site. (This is ONLY needed for the static uNav.)

```css
@media print {
    .nygov-universal-container {
        display: none;
    }     
}
```

## Available Settings

### Open links in new windows or tabs

Append `&target=blank` to the URL in the `<iframe src>`.

**Banner:**

```html
src="//static-assets.ny.gov/load_global_menu/ajax?iframe=true&target=blank"
```

**Footer:**

```html
src="//static-assets.ny.gov/load_global_footer/ajax?iframe=true&target=blank"
```
