---
layout : "empty.njk"
title: "Template - Order of things - All"
date: 2022-02-01 00:00:01Z
---
<section class="govcy-container-fluid" id="bodyStartContainer"> 
    <a href="#mainContainer1" class="govcy-skip-link">Skip to main content</a>
    <div class="govcy-cookie-consent-banner">
        <div class="govcy-container">
            <h3>Cookies on gov.cy</h3>
            <p>We use some essential cookies to make this website work.</p>
            <p>We’d also like to use analytics cookies so we can understand how you use the service and make improvements.</p>
            <div class="govcy-d-flex govcy-align-items-center">
            <a href="#" class="govcy-btn-primary me-2">Accept cookies</a>
            <a href="#" class="govcy-btn-primary me-2">Reject cookies</a>
            <a href="#">Adjust cookies</a>
            </div>
        </div>
    </div>
</section>
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
                        aria-current="true" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα">EL</a></span>
                      </li>
                      <li class="govcy-desktop-menu-only"><span class="govcy-menu-language-last-item"><a href="#"
                                class="govcy-menu-item" aria-label="English language" lang="en">EN</a></span>
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
                    <li><a href="#" class="govcy-menu-item active" aria-label="Ελληνική γλώσσα" aria-current="true">EN</a></li>
                    <li><a href="#" class="govcy-menu-item" aria-label="English language" lang="el">EL</a></li>
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
<!--beforeMain-->
<section class="govcy-container" id="beforeMainContainer">
    <a class="govcy-back-link" href="#">Back</a>
    <div class="govcy-phase-banner govcy-phase-banner-light">
        <span class="govcy-tag">NEW SERVICE</span>
        <span class="govcy-ml-2">This is a new service - your <a href="#">feedback</a> will help us improve it.</span>
    </div>
</section>
 <!--main-->
<main class="govcy-container" id="mainContainer1">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
                <h2 role="alert">There is a problem</h2>
                <p class="govcy-mb-0">
                    <a href="#in-tel">Enter a valid telephone number</a>
                </p>
            </div>
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control govcy-form-control-error">
                    <h1><label class="govcy-label govcy-label-primary" for="in-tel">What is your telephone number?</label></h1>
                    <span class="govcy-hint" id="tel-hint">We’ll only use this for this application</span>
                    <p id="in-error" class="govcy-input-error-msg">
                        <span class="govcy-visually-hidden-error">Error:</span>Enter a valid telephone number
                    </p>
                    <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="in-tel" name="in-tel" type="tel" spellcheck="false" aria-describedby="tel-hint in-error" autocomplete="tel">
                </div>
                <button type="button" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility statement</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="/" class="govcy-footer-logo" title="Go to the GOV.CY homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>