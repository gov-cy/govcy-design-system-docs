---
title: "How to create new design elements using the gov.cy utility classes"
date: 2022-02-01 00:01:02Z
description: "How to use the gov.cy utility classes to create a brand new HTML design element."
image: v3_custom_design_element.png
---

In this guide we will be looking at an example for developers, of how to use the gov.cy utility classes to create a brand new HTML design element. If you would like to see an example of building a page using the gov.cy developer assets, see article on [how to create a page using the gov.cy Unified Design System](../create_a_page).

The gov.cy Unified Design System provides the basic components for creating digital sites and service straight out of the box. There may be cases where these components will not be enough to build all services or sites, so we have created a library of [CSS utility classes](../../css_utilities) that apply unique styling and formatting to HTML elements, that can be used to build new design elements, in the ‘gov.cy way’.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			The ability to create or overwrite existing components, does not mean you should change the elements of the design system in any way you like. Consistency is an important principle, so we ask that you use the components as explained in the design system, for gov.cy sites and services.
		</p>
    </div>
</div>

In the guide's example, we will be looking at how to create a component to display additional information about a page. The component is similar to the [inset text component](../../components/inset_text/), but will display an 'info' coloured left border.

We start by creating a `<div>` container. In order to comply with the [vertical spacing requirements](../../styles/vertical_spacing/#custom-components) of our design system we will assign the `govcy-mb-6` class in our `<div>`.

```html
<div class="govcy-mb-6"></div>
```

We can now add the rest of the utility classes to apply our styling preferences:
- `govcy-p-6` to set the padding left
- `govcy-br-left-4` to set the border left of 4px
- `govcy-br-left-info` to set the border left colour to info

Next add the rest of the text inside the `<div>`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-mb-6 govcy-pl-4 govcy-br-left-4 govcy-br-left-info">
    It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.
</div>
</div>

*HTML code*
```html
<div class="govcy-mb-6 govcy-pl-4 govcy-br-left-4 govcy-br-left-info">
    It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.
</div>
```
If we wish to create another design element to display the danger border colour, we can simply replace the `govcy-br-left-info` class with the `govcy-br-left-danger`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-mb-6 govcy-pl-4 govcy-br-left-4 govcy-br-left-danger">
    It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.
</div>
</div>

*HTML code*
```html
<div class="govcy-mb-6 govcy-pl-4 govcy-br-left-4 govcy-br-left-danger">
    It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.
</div>
```

This is it. We were able to easily create a new design element, aligned with the styles of gov.cy, meeting user needs, without writing any new styling code and this saves a lot of time.

## Accessibility
It is important to always test your implementation for compliance with the EN 301 549 Standard. 

Be extra careful when using background colours in containers, as they will need to be tested in terms of contrast ration against it's contents. 
