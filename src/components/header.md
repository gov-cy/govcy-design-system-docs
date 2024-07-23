---
"title" : "Header"
date: 2022-02-01 00:01:01Z
description: "Use the gov.cy header to shows users that they are on gov.cy and which service they are using."
---
The gov.cy header shows users that they are on gov.cy and which service they are using.

## When to use this component
You must use the gov.cy header at the top of every page hosted on one the gov.cy domain.

## When not to use this component
You must not use the gov.cy header if your service is not being hosted on the gov.cy domain.

## How it works
The header component should only exist in the [header section](../../getting-started/page-template/#sections). The component uses JavaScript. To use it with the gov.cy [developer assets](../../getting-started/developer-assets), make sure to include the main JavaScript file in your page.

You can only have one gov.cy header on each page. Be consistent, have the same header in the pages of your service.  

Users can navigate within the header links also by using the keyboard.

See below the different variants of the header component. Make sure to change the links `href` according to your implementation. The gov.cy logo link should lead to `https://gov.cy`. 

Use the `govcy-d-print-none` to hide the header on print media. 

Use the `active` class and `aria-current="true"` to indicate the current page in menu `<a>` elements.

### Default header
Use the default header for services and websites that consist of only a single page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                </div>
                <ul class="govcy-menu-items govcy-ms-auto">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
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
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```

### Header with a site or service name
Use the header with a site/service name if your service or website is more than 5 pages long - this can help users understand which service or site they are viewing.

Depending on your case, you may add link your service name, with the service's home or start page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name"><a href="#">Design System</a></span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name"><a href="#">Design System</a></span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```

### Header with a long name
If the service name is too long, then the section breaks.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Deputy Ministry of Research, Innovation and Digital Policy</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Deputy Ministry of Research, Innovation and Digital Policy</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Header without a language menu 
If a site/service is only available in one language, use a header without a language menu.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none" id="headerContainer">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Design system</span>
                </div>
            </div>
        </div>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none" id="headerContainer">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Design system</span>
                </div>
            </div>
        </div>
    </div>
</header>
```

### Header with search bar
For longer sites and services with lots of content, make sure to add a search bar. The search bar is placed next to the language dropdown.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="../../" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn">Menu</a></span></li>
                    <li class="govcy-global-search">
                        <span><a href="#" class="govcy-menu-item" aria-label="Search, expands search text box when clicked" aria-haspopup="true"><i class="govcy-search-icon"></i></a></span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <div class="govcy-header-search-area">
            <div class="govcy-container">
                <form action="" class="govcy-form" novalidate="">
                    <div class="govcy-form-control">
                        <label class="govcy-label" for="search">Search gov.cy</label>
                        <input id="search" type="text" class="govcy-text-input" enterkeyhint="search">
                        <button type="submit" class="govcy-btn-primary govcy-btn-search" aria-label="Search" aria-expanded="true">Search</button>
                    </div>
                </form>
            </div>
        </div>
        <nav class="govcy-mainmenu" aria-label="Main Menu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="../../" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn">Menu</a></span></li>
                    <li class="govcy-global-search">
                        <span><a href="#" class="govcy-menu-item" aria-label="Search, expands search text box when clicked" aria-haspopup="true"><i class="govcy-search-icon"></i></a></span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <div class="govcy-header-search-area">
            <div class="govcy-container">
                <form action="" class="govcy-form" novalidate="">
                    <div class="govcy-form-control">
                        <label class="govcy-label" for="search">Search gov.cy</label>
                        <input id="search" type="text" class="govcy-text-input" enterkeyhint="search">
                        <button type="submit" class="govcy-btn-primary govcy-btn-search" aria-label="Search" aria-expanded="true">Search</button>
                    </div>
                </form>
            </div>
        </div>
        <nav class="govcy-mainmenu" aria-label="Main Menu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Header with sign in option
Use a header with login in services or websites that require the user to login.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li><a href="#"><i class="govcy-signin-icon"></i> Sign In</a></li>
                    <li><span> / </span></li>
                    <li><a href="#">Register</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li><a href="#"><i class="govcy-signin-icon"></i> Sign In</a></li>
                    <li><span> / </span></li>
                    <li><a href="#">Register</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```

#### Header with user name and sign out
Use a header with the user name and sign out on services or websites that require the user to login, when the user is logged in.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li>Firstname Lastname</li>
                    <li><span>|</span></li>
                    <li><a href="#">Sign Out</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only" hidden=""><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn" aria-expanded="false">Menu</a></span></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <nav class="govcy-mainmenu" aria-label="Main Menu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα"  lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li>Firstname Lastname</li>
                    <li><span>|</span></li>
                    <li><a href="#">Sign Out</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only" hidden=""><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn" aria-expanded="false">Menu</a></span></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <nav class="govcy-mainmenu" aria-label="Main Menu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα"  lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Header with contact
Use this header if you wish to link a contact page at the header.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα"  lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα"  lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Contact">
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Header with navigation
Use the header with navigation if you need to include basic navigation.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 1</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 2</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 3</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 4</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 1</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 2</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 3</a></li>
                    <li><a href="#" class="govcy-menu-item">Page 4</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Navigation with a dropdown
If a main page includes different sub-pages, you can add drop down to the desired pages.

It’s important to note that menu pages that have a govcy-dropdown that are not linkable and their purpose it to open the govcy-dropdown, should have `href="#"`. For the example below element “Page 1” which is a govcy-dropdown is not a link.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```

Some subpages might have their own subpages, this is how its achieved

As mentioned above, menu pages that have a govcy-dropdown that are not linkable and their purpose it to open the govcy-dropdown, should have `href="#"`. For the example below element “subpage 2” is not a link.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li class="govcy-dropdown govcy-dropdown-right">
                                <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Subpage 2<i></i></a>
                                <ul class="govcy-right-menu govcy-expandable">
                                    <li><a href="#" class="govcy-menu-item">Item 1</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 2</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 3</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 4</a></li>
                                </ul>
                            </li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
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
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li class="govcy-dropdown govcy-dropdown-right">
                                <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Subpage 2<i></i></a>
                                <ul class="govcy-right-menu govcy-expandable">
                                    <li><a href="#" class="govcy-menu-item">Item 1</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 2</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 3</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 4</a></li>
                                </ul>
                            </li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Header using all the options
A header including all the options is a rare occurrence, however this is how it will look.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li><a href="#"><i class="govcy-signin-icon"></i> Sign In</a></li>
                    <li><span> / </span></li>
                    <li><a href="#">Register</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn">Menu</a></span></li>
                    <li class="govcy-global-search">
                        <span><a href="#" class="govcy-menu-item" aria-label="Search, expands search text box when clicked" aria-haspopup="true"><i class="govcy-search-icon"></i></a></span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <div class="govcy-header-search-area">
            <div class="govcy-container">
                <form action="" class="govcy-form" novalidate="">
                    <div class="govcy-form-control">
                        <label class="govcy-label" for="search1">Search gov.cy</label>
                        <input id="search1" type="text" class="govcy-text-input" enterkeyhint="search">
                        <button type="submit" class="govcy-btn-primary govcy-btn-search" aria-label="Search" aria-expanded="true">Search</button>
                    </div>
                </form>
            </div>
        </div>
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li class="govcy-dropdown govcy-dropdown-right">
                                <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Subpage 2<i></i></a>
                                <ul class="govcy-right-menu govcy-expandable">
                                    <li><a href="#" class="govcy-menu-item">Item 1</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 2</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 3</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 4</a></li>
                                </ul>
                            </li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
</div>

*HTML code*
```html
<header class="govcy-header govcy-d-print-none">
    <div class="govcy-header-top-area">
        <div class="govcy-container">
            <div class="govcy-header-top-area-wrapper">
                <ul class="govcy-sign-in">
                    <li><a href="#"><i class="govcy-signin-icon"></i> Sign In</a></li>
                    <li><span> / </span></li>
                    <li><a href="#">Register</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-main-area">
        <div class="govcy-container govcy-main-area-items">
            <div class="govcy-navigation-container">
                <div class="govcy-service-container">
                    <a href="/" class="govcy-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"></a>
                    <span class="govcy-service-name">Service Name</span>
                </div>
                <ul class="govcy-menu-items">
                    <li class="govcy-desktop-menu-only"><span><a href="#" class="govcy-menu-item"><i class="govcy-contact-icon"></i>Contact</a></span></li>
                    <li class="govcy-desktop-menu-only"><span><a href="#"
                        class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EN</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                        class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></span>
                    </li>
                    <li class="govcy-mobile-menu govcy-mobile-menu-only govcy-dropdown govcy-ms-auto"><span><a href="#" class="govcy-menu-item govcy-expand-btn">Menu</a></span></li>
                    <li class="govcy-global-search">
                        <span><a href="#" class="govcy-menu-item" aria-label="Search, expands search text box when clicked" aria-haspopup="true"><i class="govcy-search-icon"></i></a></span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-header-menu-area">
        <div class="govcy-header-search-area">
            <div class="govcy-container">
                <form action="" class="govcy-form" novalidate="">
                    <div class="govcy-form-control">
                        <label class="govcy-label" for="search1">Search gov.cy</label>
                        <input id="search1" type="text" class="govcy-text-input" enterkeyhint="search">
                        <button type="submit" class="govcy-btn-primary govcy-btn-search" aria-label="Search" aria-expanded="true">Search</button>
                    </div>
                </form>
            </div>
        </div>
        <nav class="govcy-mainmenu">
            <div class="govcy-container">
                <ul class="govcy-menu-items govcy-header-language-area govcy-mobile-menu-only">
                    <li><a href="#" class="govcy-menu-item" aria-label="Ελληνική γλώσσα" lang="el">EN</a></li>
                    <li><a href="#" aria-current="true" class="govcy-menu-item active" aria-label="English language" lang="en">EL</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="Türkçe" lang="tr">TR</a></li>
                </ul>
            </div>
            <div class="govcy-container">
                <ul class="govcy-menu-items" aria-label="Main Menu">
                    <li><a href="#" class="govcy-menu-item">Home</a></li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 1<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li class="govcy-dropdown govcy-dropdown-right">
                                <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Subpage 2<i></i></a>
                                <ul class="govcy-right-menu govcy-expandable">
                                    <li><a href="#" class="govcy-menu-item">Item 1</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 2</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 3</a></li>
                                    <li><a href="#" class="govcy-menu-item">Item 4</a></li>
                                </ul>
                            </li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 2<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 3<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-dropdown">
                        <a href="#" class="govcy-menu-item govcy-expand-btn" aria-haspopup="true" aria-expanded="false">Page 4<i></i></a>
                        <ul class="govcy-dropdown-menu govcy-expandable">
                            <li><a href="#" class="govcy-menu-item">Subpage 1</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 2</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 3</a></li>
                            <li><a href="#" class="govcy-menu-item">Subpage 4</a></li>
                        </ul>
                    </li>
                    <li class="govcy-mobile-menu-only"><a href="#" class="govcy-menu-item"><span><i class="govcy-contact-icon"></i>Contact</span></a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```
### Component text
Use the follow content on your header implementations:

**gov.cy logo**

| Text | English | Greek |
| ---- | ---- | ---- |
| **Title** | Go to the gov.cy homepage | Μεταβείτε στην αρχική σελίδα του gov.cy |
| **img alt text** | gov.cy Logo | Λογότυπο gov.cy |

{.govcy-table}

**General link text**

| Link | English | Greek |
| ---- | ---- | ---- |
| **Home** | Home | Αρχική |
| **Language** | Language | Γλώσσα |
| **Menu** | Menu | Μενου |
| **Contact** | Contact | Επικοινωνία  |

{.govcy-table}

**aria-label text**

| aria-label | English | Greek |
| ---- | ---- | ---- |
| **Change language** | Change language | Αλλαγή γλώσσας |
| **Main menu** | Main menu | Κυρίως μενού |
| **Search button** | Search, expands search text box when clicked | Αναζήτηση, επεκτείνει πλαίσιο για εισαγωγή κειμένου αναζήτησης όταν πατηθεί |
| **Search** | Search | Αναζήτηση |
| **Contact** | Contact | Επικοινωνία |

{.govcy-table}

## Accessibility
Make sure:
- you use the aria, alt and title tags as shown in the examples
- you use the correct lang attribute for each language link, for example use `lang="el"` for Greek 
- you use the correct `aria-label` for each language link as follows:
	- for Greek use `aria-label="Ελληνική γλώσσα"`
	- for English use `aria-label="English language"`
	- for Turkish use `aria-label="Türkçe"`
- you use `aria-current="true"` for the current menu `<a>` elements
- not to make header elements ‘sticky’ to the top of the page by using `position: fixed` or any other method