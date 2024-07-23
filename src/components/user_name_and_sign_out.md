---
title: "User’s name and sign out"
date: 2022-02-01 00:01:01Z
description: "Use this component to help the user’s identify which account they are signed in with and provide them with a link to sign out of their account."
---
Use this component to help the user’s identify which account they are signed in with and provide them with a link to sign out of their account.

## When to use this component
Always use this component when the service requires users to be signed in with a CY Login account.

## When not to use this component
Do not use the component when the service is public and does not require users to be signed in.

## How it works
The component is placed in header section. Use the [header with username](../header/#header-with-user-name-and-sign-out) variation to implement the user’s name and sign out component.

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
                        aria-current="true" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                class="govcy-menu-item" aria-label="English language" lang="en">EN</a></span>
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
                    <li><a href="#" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα" aria-current="true">EN</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="English language" lang="el">EL</a></li>
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
                        aria-current="true" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                class="govcy-menu-item" aria-label="English language" lang="en">EN</a></span>
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
                    <li><a href="#" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα" aria-current="true">EN</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="English language" lang="el">EL</a></li>
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

The `User’s name` in this component should contain the name (not the username) of the signed in CY Login profile account.

Make sure to implement the sign out mechanism according to CY Login’s standards when the user clicks the `sign out` link.

### Component text
For the sign out link, use the following content:
- In English: `Sign out`
- In Greek: `Αποσύνδεση`