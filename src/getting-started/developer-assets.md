---
title: "Developer assets"
date: 2022-02-01 00:00:03Z
--- 

The easiest way to get started is to use the jsdelvr CDN to include the gov.cy developer assets in your code, as shown in the [page template](../page-template/#starter-template) and the examples below. 

Alternatively you can download the [gov.cy starter kit]({{site.distDownload}}), unzip it and include it in your project. 

The following file structure is included in the starter kit:
```html
.
+-- css
|   +-- govcy.uds.css
+-- img
|   +-- ...
+-- JS
|   +-- govcy.uds.js
|   +-- locales
|       +-- govcy.datepicker.el.js
|       +-- govcy.datepicker.en.js
+-- manifest.json
```

All HTML code examples in this website utilizes the classes, styling and behavior defined in this CSS and JS files of our developer assets. 

## CSS
To add the gov.cy styles using our developer assets, add the CSS either using the CDN or using the downloaded starter kit.

### CDN
To use the gov.cy CSS with jsdelivr CDN, include the following code in your `<head>`.

```html
<!-- CSS -->
{{ site.cssCDN }}
```
### Downloaded starter kit
To add the gov.cy CSS using the downloaded starter kit, use the pre-built `css/govcy.uds.min.css` file, by including the following code in your `<head>`.

```html
<!-- CSS -->
<link href="css/govcy.uds.min.css" rel="stylesheet" >
```

**NOTE:** if the paths or filenames of your files are different in you project, please adjust the code accordingly.

## JavaScript
Many of our components require the use of JavaScript to function. To enable them, you can use the gov.cy JS either using the CDN or using the downloaded starter kit to reference the javascript file.

### CDN
To use the gov.cy CSS with jsdelivr CDN, include the following code right before the closing `</body>` tag.

```html
<!-- scripts -->
{{ site.jsCDN }}
```

### Downloaded starter kit
To add the gov.cy javascript using the downloaded starter kit, use the pre-built `js/govcy.uds.js` file, by including the following code right before the closing `</body>` tag.

```html
<!-- scripts -->
<script src="js/govcy.uds.min.js" type="text/javascript"></script>
```

**NOTE:** if the paths or filenames of your files are different in you project, please adjust the code accordingly.

## Images

You will need to reference images for icons and logos. All images required by the [page template's `head` section](../page-template/#head) and [manifest.json](../page-template/#theme%2C-app-manifest-and-apple-touch-icon) are included in the starter kid under the `/img` folder.

## Next step

To implement [styles](../../styles/), [components](../../components/) and [patterns](../../patterns/) using the developer assets, make sure to use the [starter template](../page-template/#starter-template) and the code included in each documentation page through this website.

To get stated in creating a page, take a look at out [create a page](../../guides/create_a_page/) guide. 
