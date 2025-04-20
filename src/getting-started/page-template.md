---
title: "Page Template"
date: 2022-02-01 00:00:04Z
--- 

## Starter Template
Use the following HTML template for your gov.cy pages.

```html
<!doctype html>
<html lang="el">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Social -->
    <meta property="og:description" content="Description of what the service does">
    <meta property="og:title" content="Page title - Service title - gov.cy">
    <meta property="og:url" content="https://SERVICE_URL">
    <meta property="og:type" content="website">
    <meta property="og:image" content="/img/icons-512.png">
    <meta property="og:site_name" content="gov.cy">
 
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://SERVICE_URL">
    <meta property="twitter:title" content="Page title - Service title - gov.cy">
    <meta property="twitter:description" content="Description of what the service does">
    <meta property="twitter:image" content="/img/icons-512.png">
 
    <!-- Theme --> 
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#31576F">
    <link rel="icon" type="image/png" sizes="48x48" href="/img/favicon-48x48.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/img/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/img/favicon-16x16.png">
 
    <link rel="apple-touch-icon-precomposed" sizes="144x144" href="/img/apple-touch-icon-144x144-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="120x120" href="/img/apple-touch-icon-120x120-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="114x114" href="/img/apple-touch-icon-114x114-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="72x72" href="/img/apple-touch-icon-72x72-precomposed.png">
    <link rel="apple-touch-icon-precomposed" href="/img/apple-touch-icon-57x57-precomposed.png">
 
    <!-- CSS -->
    {{ site.cssCDN }}
    
    <title>Page title - Service Name - gov.cy</title>
    <meta name="description" content="Description of what the service does">
 
 
  </head>
  <body>
    <!--bodyStart-->
    <section class="govcy-container-fluid" id="bodyStartContainer">
         <a href="#mainContainer" class="govcy-skip-link">Skip to main content</a>
        ...
    </section>

    <!--Header-->
    <header class="govcy-header govcy-d-print-none" id="headerContainer">
        ...
    </header>

    <!--beforeMain-->
    <section class="govcy-container" id="beforeMainContainer">
        ...
    </section>

    <!--main-->
    <main class="govcy-container" id="mainContainer">
        ...
    </main>

    <!-- Footer -->
    <footer class="govcy-footer govcy-d-print-none" id="footerContainer">
        ...
    </footer>

    <!--bodyEnd-->
    <section  class="govcy-container-fluid" id="bodyEndContainer">
        ...
    </section>    
    {{ site.jsCDN }}
  </body>
</html>
```
The code above includes the [head](#head) and all the sections described in the [body](#body) section and uses the appropriate gov.cy CSS classes to accommodate [spacing](../../styles/vertical_spacing/), [header](../../components/header/) and [footer](../../components/footer/) components.
## Head
### Important Globals
The starter template employs the following important global styles and settings that you’ll need to be aware of when using it.
#### HTML5 doctype and lang

Use the HTML5 doctype

```html
<!doctype html>
<html lang="el">
  ...
</html>
```
The language of the document or a page element must be identified using the lang attribute as follows `<html lang="en">`. This is a very important accessibility requirement as it instructs the screen readers which language to use.  

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Change the lang attribute according to the language used in the document
            <ul class="govcy-ml-4">
                <li>If the language of the page is in Greek, you must have <code>&lt;html lang="el""&gt;</code>. </li>
                <li>If the language of the page is in English, you must have <code>&lt;html lang="en""&gt;</code></li>
                <li>If the language of the page is in Turkish, you must have <code>&lt;html lang="tr""&gt;</code></li>
            </ul>
		</p>
    </div>
</div>

#### Responsive meta tag
To ensure proper rendering and touch zooming for all devices, add the responsive viewport meta tag to your `<head>`
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```
### Other Head Tags
#### title, description
Use the following tags inside the `<head>` tag.
```html
<title>Page title - Service Name - gov.cy</title>
<meta name="description" content="Description of what the service does">
```
Page titles should be unique and informative so that users know which page they are on. Change the content of the above tags, depending if you are implementing a content page or a service :

<div class="govcy-table-responsive">

| tags | Content pages | Services |
| ---- | ---- | ---- |
| **title** | Use the following naming convention <br> `Page name - Site Name - gov.cy` <br><br>For example:<br> `About - Department of Information Technology Services - gov.cy` | Use the following naming convention <br> `Page title - Service Name - gov.cy` <br><br>For example:<br> `Address we can use to write to you - Update my personal details - gov.cy` |
| **description** | Description of what the site is about | Description of what the service does |

{.govcy-table}
</div>

For the gov.cy portal websites use the following naming conventions:
- For sub-site home page: `Site Name - gov.cy` For example: 
`Department of Information Technology Services - gov.cy`
- For other sub-site pages: `Page name - Site Name - gov.cy`. For example: `About - Department of Information Technology Services - gov.cy`

#### social tags
Use the following meta tags inside the `<head>` tag.

```html
<meta property="og:description" content="Description of what the service does"> 
<meta property="og:title" content="Page title - Service title - gov.cy">
<meta property="og:url" content="https://SERVICE_URL">
<meta property="og:type" content="website">
<meta property="og:image" content="/img/icons-512.png">
<meta property="og:site_name" content="gov.cy">
 
<meta property="twitter:card" content="summary_large_image">
<meta property="twitter:url" content="https://SERVICE_URL">
<meta property="twitter:title" content="Page title - Service title - gov.cy">
<meta property="twitter:description" content="Description of what the service does">
<meta property="twitter:image" content="/img/icons-512.png">
```
  
Change the content of the above tags as follows:

- `og:title`, `twitter:title`: Use the same naming convention as explained above for the `<title>`
- `og:description`, `twitter:description`: Description of what the service does. In most cases should be the same as with `<meta name="description" content="...">`
- `og:url`, `twitter:url`: The URL of the stating page of the service
- `og:image`, `twitter:image`: The URL of the icon. The icon should be 512 x 512 px. Use the `icons-512.png` [image from our developer assets](../developer-assets/#images).
- `og:type`: Should be `website`
- `og:site_name`: Should be `gov.cy`
- `twitter:card`: Should be `summary_large_image`
#### theme, app manifest and apple-touch-icon

Use the following tags inside the `<head>` tag.
```html
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#31576F">
<link rel="icon" type="image/png" sizes="48x48" href="/img/favicon-48x48.png">
<link rel="icon" type="image/png" sizes="32x32" href="/img/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/img/favicon-16x16.png">
<link rel="apple-touch-icon-precomposed" sizes="144x144" href="/img/apple-touch-icon-144x144-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="120x120" href="/img/apple-touch-icon-120x120-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="114x114" href="/img/apple-touch-icon-114x114-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="72x72" href="/img/apple-touch-icon-72x72-precomposed.png">
<link rel="apple-touch-icon-precomposed" href="/img/apple-touch-icon-57x57-precomposed.png">
```
All images referenced in the `head` section and `manifest.json` are included in the [starter kid](../developer-assets/) under the `/img` folder.

The code above implies the existence of a `manifest.json` file. Use the following template for the manifest file.
```json
{
    "short_name": "Service title",
    "name": "Service title - gov.cy",
    "icons": [
        {
            "src": "/img/icons-128.png",
            "type": "image/png",
            "sizes": "128x128"
        },
        {
            "src": "/img/icons-192.png",
            "type": "image/png",
            "sizes": "192x192"
        },
        {
            "src": "/img/icons-512.png",
            "type": "image/png",
            "sizes": "512x512"
        }
    ],
    "start_url": "/LOCATION_OF_START_PAGE",
    "background_color": "#31576F",
    "display": "browser",
    "scope": "/",
    "theme_color": "#31576F"
}
```

**NOTE**: if the location or filenames of your images are different, please adjust the code appropriately.

## Body

### Max-width
Max-width defines the maximum width of the content of a page.

Note that some sections such as `Body start` and `Body end` use a fluid design for background colour and styling, but content such as text, links and icons are restricted within the max-width limit.

The default maximum width is `1200px`.
### Responsive breakpoint
Breakpoint is the width that determines how your responsive layout behaves across devices. The default breakpoint is `≥768px`.
### Sections
All pages must use the following structure inside the `<body>` tag.

<div class="govcy-table-responsive">

| Section Name | HTML Tag                                                                           | Description                                                                                                                                                                      |
| ------------ | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Body start**   | `<section class="govcy-container-fluid" id="bodyStartContainer"> </section>`       | To be used to render the content before the `<header>` such as [skip link](#skip-to-main-content) and [cookie consent](../../components/cookie_banner/) (Skip link must always be first). Width must be fluid, same as the viewport. |
| **Header**       | `<header class="govcy-header  govcy-d-print-none" id="headerContainer"> </header>` | To be used as the [page header](../../components/header/). Width must be fluid, same as the viewport. Use the `govcy-d-print-none` class to hide the header on print.                                    |
| **Before main**  | `<section class="govcy-container" id="beforeMainContainer"> </section>`            | To be used to render the content before the `<main>` (i.e. [back link](../../components/back_link/), [breadcrumbs](../../components/breadcrumbs/) and [phase banner](../../components/phase_banner/) only ) . This section must comply with the [max-width](#max-width) reference above and be placed in the center of the viewport with `text-align` set to `start`. |
| **Main**         | `<main class="govcy-container" id="mainContainer"> </main>`                        | To be used to render the service/website content (i.e. [question page](../../patterns/question_pages/). This section can have one of the layouts described in the [layouts](../../styles/layout/) page. This section must comply with the [max-width](#max-width) reference above and be placed in the center of the viewport with `text-align` set to `start`. |
| **Footer**       | `<footer class="govcy-footer  govcy-d-print-none" id="footerContainer"> </footer>` | To be used as the page [footer](../../components/footer/). Use the `govcy-d-print-none` class to hide the footer on print.                                                                               |
| **Body end**     | `<section class="govcy-container-fluid" id="bodyEndContainer"> </section>`         | To be used to render the content after the `<footer>`. Width must be fluid, same as the viewport.                                                                                |

{.govcy-table}
</div>

![Visual example marking the different sections of a gov.cy page](../../img/v3_sections_of_page.png){style="aspect-ratio: auto;"}
### Element Placement Order
Depending on the website or service, you might need to implement more than one design elements withing a section. Use the following order in each section:

1. **Body start section** 
    1. [Skip to main content](#skip-to-main-content)
    2. [Cookies banner](../../components/cookie_banner/)
2. **Header section**
    1. [Header](../../components/header/) component
3. **Before main section** 
    1. [Breadcrumbs](../../components/breadcrumbs/) or [Back link](../../components/back_link/) component
    2. [Phase banner](../../components/phase_banner/) component
4. **Main section** 
    1. [Error summary](../../components/error_summary/) component, in the case of errors.
    2. [Progress indicator](../../components/progress_indicator/) component, in case it is used.
    3. [Header 1 `<h1>`](../../styles/typography/#headings). If your using an input component and you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header accordingly. 
    4. Other [components](../../components/), [patterns](../../patterns/) or [typography](../../styles/typography/)
5. **Footer section**
    1. [Footer](../../components/footer/) component

{class="govcy-br-1 govcy-br-standard govcy-py-4"}

See below an sample page with most design elements present in the correct order.

[Open in new tab](../../samples/template-order-of-things-all/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/template-order-of-things-all/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>

### Skip to main content
Always include the skip link right after the opening `<body>` in the "Body start" section (bodyStartContainer).

```html
<a href="#mainContainer" class="govcy-skip-link">Skip to main content</a>
```

Make sure that the target element of the anchor is the **main section** container and that it includes the [error summary](../../components/error_summary/)  if applicable, the `h1` and the main content of the page. However, if you’re using a component that must be read before the user can skip to the main content (such as a cookie banner) , place the skip link immediately after the component.

The skip link component is visually hidden until a keyboard press activates it. The link should give the users the option to bypass the top-level navigation links and jump to the main content (`mainContainer`) of the page.

Use the following content:
- In English: `Skip to main content`
- In Greek: `Μεταφορά στο κεντρικό περιεχόμενο`

### Main section
The main section is where the content of each page is placed. If you are building a service, this is where you will place your components and patterns.

Remember that services should work independently and in isolation from other services, and that the `main` section should help users focus on their goal. Include only elements that are necessary for the user to complete the task at hand. 

For more information about the `<main>` section content, see the [layouts](../../styles/layout/) page.

## Sample pages
Here are some sample pages using the gov.cy page template. 

**Content pages**:
- [Page with title and paragraph (opens in new tab)](../../samples/templare-heading-title/){rel="noreferrer noopener" target="_blank"}
- [Page with title, different headings and paragraphs (opens in new tab)](../../samples/templare-heading-title-more/){rel="noreferrer noopener" target="_blank"}
- [Page with back link (opens in new tab)](../../samples/template-heading-back/){rel="noreferrer noopener" target="_blank"}
- [Page with breadcrumbs (opens in new tab)](../../samples/template-heading-breadcrumbs/){rel="noreferrer noopener" target="_blank"}
- [Page with phase banner (opens in new tab)](../../samples/template-heading-phase-banner/){rel="noreferrer noopener" target="_blank"}

**Service pages**:
- [Page with a question (opens in new tab)](../../samples/template-heading-input/){rel="noreferrer noopener" target="_blank"}
- [Page with an error (opens in new tab)](../../samples/template-heading-error-summary/){rel="noreferrer noopener" target="_blank"}
- [Page asking for address (opens in new tab)](../../samples/template-address/){rel="noreferrer noopener" target="_blank"}
- [Page with radios question (opens in new tab)](../../samples/template-radios/){rel="noreferrer noopener" target="_blank"}

## Accessibility
Make sure:
- you include the [skip link](#skip-to-main-content) in your page
- you use the correct [lang attribute](#html5-doctype-and-lang) in your page
- the [page titles are unique](#title%2C-description)