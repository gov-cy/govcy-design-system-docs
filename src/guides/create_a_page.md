---
title: "How to create a page using the gov.cy Unified Design System"
date: 2022-02-01 00:01:01Z
description: "A step by step guide for developers on how to create a simple question page using DSF’s reusable components."
image: v3_custom_page.png
---
In this guide we will be looking at a step by step guide for developers on how to create a simple [question page](../../patterns/question_pages) using the [developer assets](../../getting-started/developer-assets/). 

You can use our pre-built [css and javascript](../../getting-started/developer-assets/) to create an HTML page with the necessary [head](../../getting-started/page-template/#head) and [body](../../getting-started/page-template/#body) sections and use one of the predefined [layouts](../../styles/layout/). All you need to do is copy the code below and follow the instructions: 

## 1. Download all the developer assets
First things first, you will need to [download all the static files form the starter kit](../../getting-started/developer-assets/) needed from our design system:

In the examples used in this guide, we will only be using the images from the downloaded file under the `/img` sub-folder. We will be using CDN for the css and JavaScript.

## 2. Create a web app manifest file
The [web app manifest](../../getting-started/page-template/#theme%2C-app-manifest-and-apple-touch-icon) provides information about your service such as its name, icons, background and theme colour, in a JSON text file.

Create a `manifest.json` text file and add the following content.
```json
{
    "short_name": "Sample service",
    "name": "Sample service - gov.cy",
    "icons": [
        {
            "src": "img/icons-128.png",
            "type": "image/png",
            "sizes": "128x128"
        },
        {
            "src": "img/icons-192.png",
            "type": "image/png",
            "sizes": "192x192"
        },
        {
            "src": "img/icons-512.png",
            "type": "image/png",
            "sizes": "512x512"
        }
    ],
    "start_url": ".",
    "background_color": "#31576F",
    "display": "browser",
    "scope": "/",
    "theme_color": "#31576F"
}
```
In a real service make sure to replace the following with your service details:

- `short_name`: “Sample service”,
- `name`: “Sample service - gov.cy”

## 3. Create an html file
Create an html file using the [page template](../../getting-started/page-template/).

In our example we have created a file named `index.html`. At this point the file’s content looks like this:
```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Social -->
    <meta property="og:description" content="This is an example of a sample question page for a gov.cy service ">
    <meta property="og:title" content="Where do you live? - Sample service - gov.cy">
    <meta property="og:url" content="https://SERVICE_URL">
    <meta property="og:type" content="website">
    <meta property="og:image" content="img/icons-512.png">
    <meta property="og:site_name" content="GOV.CY">
 
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://SERVICE_URL">
    <meta property="twitter:title" content="Where do you live? - Sample service - gov.cy">
    <meta property="twitter:description" content="This is an example of a sample question page for a gov.cy service ">
    <meta property="twitter:image" content="img/icons-512.png">
 
    <!-- Theme -->
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#31576F">
    <link rel="icon" type="image/png" sizes="48x48" href="img/favicon-48x48.png">
    <link rel="icon" type="image/png" sizes="32x32" href="img/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="img/favicon-16x16.png">
 
    <link rel="apple-touch-icon-precomposed" sizes="144x144" href="img/apple-touch-icon-144x144-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="120x120" href="img/apple-touch-icon-120x120-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="114x114" href="img/apple-touch-icon-114x114-precomposed.png">
    <link rel="apple-touch-icon-precomposed" sizes="72x72" href="img/apple-touch-icon-72x72-precomposed.png">
    <link rel="apple-touch-icon-precomposed" href="img/apple-touch-icon-57x57-precomposed.png">
 
    <!-- CSS -->
    {{ site.cssCDN }}
   
    <title>Where do you live? - Sample service - gov.cy</title>
    <meta name="description" content="This is an example of a sample question page for a gov.cy service ">
 
 
  </head>
  <body>
    <a href="#mainContainer" class="govcy-skip-link">Skip to main content</a>
    <!--bodyStart-->
    <section  class="govcy-container-fluid" id="bodyStartContainer"> </section>
    <!--Header-->
    <header class="govcy-header govcy-d-print-none" id="headerContainer"> </header>
    <!--beforeMain-->
    <section class="govcy-container" id="beforeMainContainer"> </section>
    <!--main-->
    <main class="govcy-container" id="mainContainer"> </main>
    <!-- Footer -->
    <footer class="govcy-footer govcy-d-print-none" id="footerContainer"> </footer>
    <!--bodyEnd-->
    <section  class="govcy-container-fluid" id="bodyEndContainer"> </section>
    <!-- scripts -->
    {{ site.jsCDN }}
  </body>
</html>
```
In a real service make sure to replace the following with your service details:

- Update the language of the document depending on the language of the page
	- `<html lang="en">`
- Update the content of the following tags with your **service URL start page**
    - `<meta property="og:url" content="https://SERVICE_URL">`
    - `<meta property="twitter:url" content="https://SERVICE_URL">`
- Update the content of the following tags with your **page title**
    - `<meta property="og:title" content="Where do you live? - Sample service - gov.cy">`
    - `<meta property="twitter:title" content="Where do you live? - Sample service - gov.cy">`
    - `<title>Where do you live? - Sample service - gov.cy</title>`
- Update content the content of the following tags with your **service description**
    - `<meta property="og:description" content="This is an example of a sample question page for a gov.cy service ">`
    - `<meta property="twitter:description" content="This is an example of a sample question page for a gov.cy service ">`
    - `<meta name="description" content="This is an example of a sample question page for a gov.cy service ">`

Visually, the page looks like this right now:
![Representation of our page with nothing on it](../../img/v3_page_with_nothing.png){style="aspect-ratio: auto;"}

## 4. Add the desired layout

You can now replace the `<main>` section with the [desired layout](../../styles/layout/) in your html file. 

This is what the `<main>` section looks like at this point:

```html
 <!--main-->
    <main class="govcy-container" id="mainContainer">
        <div class="govcy-row">
            <article class="govcy-col-8">Main</article>
        </div>
    </main>
```

Visually our page right now looks like this:
![Representation of our page with layout on it](../../img/v3_page_with_layout.png){style="aspect-ratio: auto;"}

It still is not much to look at but be patient, we are getting there.

## 5. Add components and patterns
We can now add our design elements and include content in our page. First we will start with the basics, that is all the components most gov.cy pages should have.
### Header
Replace the code to inside the header section of the body for a [header component](../../components/header/)

This is what the header section looks like now:

```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                </div>
                <ul class="govcy-menu-items govcy-ms-auto">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn">Menu</a></span></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <nav class="govcy-mainmenu" aria-label="Main Menu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="English language" lang="en" aria-current="true">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
In a real service make sure to replace the service name and add functionality to change language.
### Back link
Add code inside the `before main` section (`<section id="beforeMainContainer">`) of the body for a [back link](../../components/back_link/).

This is what the before main section looks like now:
```html
<!--beforeMain-->
<section class="govcy-container" id="beforeMainContainer">
    <a class="govcy-back-link" href="#">Back</a>
</section>
```
In a real service make sure to add functionality to your back link.
### Footer
Add code inside the footer section of the body for a [footer component](../../components/footer/)

This is what the footer section looks like now:
```html
<!-- Footer -->
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                    <a href="https://europa.eu/" title="Go to EU Website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/FundedbyEU_NextGeneration_H53-EN.png" alt="Funded by the EU Next Generation EU"></a>
                    <a href="http://www.cyprus-tomorrow.gov.cy/" title="Go to Cyprus to tomorrow website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/CYpros to aurio logo eng_H53_EN.png" alt="Cyprus tomorrow, recovery and resilience plan"></a>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
```
In a real service make sure to add real urls for all the links inside the footer.
### Question page pattern
Proceed and use the [question page pattern](../../patterns/question_pages/) and add content in the `<main>` section to complete the page. We use the question page pattern when we are asking the user a question in the service.

This is what the main section looks like now:
```html
<!--main-->
<main class="govcy-container" id="mainContainer">
	<div class="govcy-row">
		<article class="govcy-col-8">
			<form action="" class="govcy-form" novalidate="">
				<fieldset class="govcy-fieldset">
					<legend class="govcy-legend ">
						<h1>Where do you live?</h1>
					</legend>
					<div class="govcy-form-control">
						<div class="govcy-radio">
							<input class="govcy-radio-input" type="radio" name="radiosGroup" id="option1">
							<label class="govcy-label" for="option1">Cyprus</label>
						</div>
						<div class="govcy-radio">
							<input class="govcy-radio-input" type="radio" name="radiosGroup" id="option2">
							<label class="govcy-label" for="option2">Abroad</label>
						</div>
					</div>
				</fieldset>
				<button type="submit" class="govcy-btn-primary">Continue</button>
			</form>
		</article>
	</div>
</main>
```

Notice that to create this question, we have used the following elements from the design system:

- a [single question radio component](../../components/radio/#single-question-page)
- a [primary button component](../../components/button/#primary-button)

Finally our page visually looks like this now:

![Representation of our page with everything on it](../../img/v3_page_with_all.png){style="aspect-ratio: auto;"}
[See the page in a new tab](../../htmls/simple_quesrtion/){rel="noreferrer noopener" target="_blank"}

In a real service make sure to add functionality in the Continue button.

So there you have it. All the steps and code you need to start building pages for gov.cy.