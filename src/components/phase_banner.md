---
title: "Phase banner"
date: 2022-02-01 00:01:01Z
description: "Use the phase banner component to show users your service is still being worked on."
---
Use the phase banner component to show users your service is still being worked on.

## When to use this component
Services hosted on a gov.cy domain that are in Alpha, Beta or Pilot phase must use the [New service phase banner](#new-service).  

Also all services that are hosted on the gov.cy staging area must use the [Testing phase banner](#testing).

## When not to use this component
Never use the panel component to highlight important information within body content.

## How it works
Your banner must be directly under the gov.cy header in the [before-main section](../../getting-started/page-template/#sections) area (with id=`beforeMainContainer`).

### Testing
Use the `TESTING` banner for testing instances of your service that resides in the staging area, but are still accessible over the internet. This will warn users that the service is only there for test purposes and not a real service

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-phase-banner">
    <span class="govcy-tag">TESTING</span>
    <span class="govcy-ml-2">This is not a real service. It is only used for testing purposes. Any submissions made through this service will be ignored.</span>
</div>
</div>

*HTML code*
```html
<div class="govcy-phase-banner">
    <span class="govcy-tag">TESTING</span>
    <span class="govcy-ml-2">This is not a real service. It is only used for testing purposes. Any submissions made through this service will be ignored.</span>
</div>
```
### New service
Use an `NEW SERVICE` banner when your service is in alpha, private or public beta or in pilot release.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-phase-banner">
    <span class="govcy-tag">NEW SERVICE</span>
    <span class="govcy-ml-2">This is a new service - your <a href="#">feedback</a> will help us improve it.</span>
</div>
</div>

*HTML code*
```html
<div class="govcy-phase-banner">
    <span class="govcy-tag">NEW SERVICE</span>
    <span class="govcy-ml-2">This is a new service - your <a href="#">feedback</a> will help us improve it.</span>
</div>
```

In some cases you might need to add a version of a service like “Version 1.0.0”.

#### Add a feedback link
Use a ‘feedback’ link to collect on-page feedback about your service. This can open an email or take the user to a dedicated page or form. Whatever option you use, make sure that users do not lose their place in the service and can return to the page they were on.

### Light version
You can use the light version of the phase banner as follows:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-phase-banner govcy-phase-banner-light">
    <span class="govcy-tag">NEW SERVICE</span>
    <span class="govcy-ml-2">This is a new service - your <a href="#">feedback</a> will help us improve it.</span>
</div>
</div>

*HTML code*
```html
<div class="govcy-phase-banner govcy-phase-banner-light">
    <span class="govcy-tag">NEW SERVICE</span>
    <span class="govcy-ml-2">This is a new service - your <a href="#">feedback</a> will help us improve it.</span>
</div>
```
### Component text
Use the following text:
	
| Phase | English | Greek |
| ---- | ---- | ---- |
| **Testing** | `TESTING` This is not a real service. It is only used for testing purposes. Any submissions made through this service will be ignored. | `TESTING` Αυτή δεν είναι πραγματική υπηρεσία. Χρησιμοποιείται μόνο για σκοπούς δοκιμών. Οποιεσδήποτε υποβολές γίνουν μέσω της υπηρεσίας αυτής θα αγνοηθούν. |
| **Alpha, Beta or Pilot** | `NEW SERVICE` This is a new service - your feedback will help us improve it. | `NEW SERVICE` Αυτή είναι μια νέα υπηρεσία - τα σχόλιά σας θα μας βοηθήσουν να τη βελτιώσουμε. |

{.govcy-table}

## Accessibility
Make sure:
- not to make the phase banner ‘sticky’ to the top of the page by using `position: fixed` or any other method, so that it does not cover or obscure any content which has a focus applied.
- not to use any other colours for the phase banner