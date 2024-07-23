---
title: "Get Started"
order: 1
tags : ['top_menu']
date: 2022-02-01 00:00:01Z
---

## Principles
When designing and implementing websites and services throughout gov.cy, consider the [design system principles](principles/)

## Designing a service
If you are implementing a service, start with the [structuring a service pattern]({{ '/patterns/service_structure/' | url }}) to understand basic structure of a service. 

### Designing individual pages of a service
To design pages that are part of a service, we prefer to use [questions]({{ '/patterns/question_pages/' | url }}) and split them across multiple pages with each page containing just one thing.  

#### Mandatory elements on each page
Make sure to use the [page template]({{ '/getting-started/page-template/' | url }}) for the [head]({{ '/getting-started/page-template/#head' | url }}) (including the [manifest.json]({{ '/getting-started/page-template/#theme%2C-app-manifest-and-apple-touch-icon' | url }})) and the [body]({{ '/getting-started/page-template/#body' | url }}) sections , use one of the [layouts]({{ '/styles/layout/' | url }}) in the `main` area and include at least, the following mandatory elements in the [correct order]({{ '/getting-started/page-template/#element-placement-order' | url }}):
- [skip link]({{ '/getting-started/page-template/#skip-to-main-content' | url }})
- [header]({{ '/components/header/' | url }}) component
- [username]({{ '/components/user_name_and_sign_out/' | url }}) component when needed
- [back]({{ '/components/back_link/' | url }}) or [breadcrumbs]({{ '/components/breadcrumbs/' | url }}) components
- [page title (header `<h1>`)]({{ '/styles/typography/#headings' | url }})
- [footer]({{ '/components/footer/' | url }}) component

![Mandatory elements illustration]({{ '/img/v3_mandatory_elemenets.png' | url }})

Additionally, make sure that to comply with the following design values:
- [max width]({{ '/getting-started/page-template/#max-width' | url }}) 
- [responsive breakpoint]({{ '/getting-started/page-template/#responsive-breakpoint' | url }})
- [vertical spacing]({{ '/styles/vertical_spacing/' | url }})
- [grid and gutter]({{ '/styles/grid/' | url }})
- [typography]({{ '/styles/typography/' | url }})
- [colours]({{ '/styles/colour/' | url }})

Also make sure to follow the guidance for [focus state]({{ '/patterns/focus_state/' | url }}) and if displaying validation errors to use the [error summary]({{ '/components/error_summary/' | url }}) together with the [error message]({{ '/components/error_message/' | url }}) components.

For any other design element, use the [components]({{ '/components/' | url }}) and [patterns]({{ '/patterns/' | url }}) of the design system. 

If you decide to opt for different designs than the ones specified in the design system, make sure to back your decisions with evidence how the existing designs fail, how the new  designs benefit the users and how they align the [principles]({{ '/getting-started/principles/' | url }}) of the design system.  

## Developing with gov.cy CSS
Code examples exist throughout this website that utilize the gov.cy CSS and JavasScript (developer assets) to create various design elements. To get started in developing websites and services using the developer assets: 
- Get the [gov.cy developer assets]({{ '/getting-started/developer-assets/' | url }})
- Use the [page template]({{ '/getting-started/page-template/' | url }}) 
- Select and use one of the [layouts]({{ '/styles/layout/' | url }}) for main section
- Use code for [components]({{ '/components/' | url }}) and [patters]({{ '/patterns/' | url }})

Take a look at our [create a page guide]({{ '/guides/create_a_page/' | url }}) for complete example.

## Accessibility
It is important to always test your implementation for compliance with the EN 301 549 Standard.

All elements presented in the design system documentation, have been tested and they comply with the [include everyone principle]({{ '/getting-started/principles/#7.-include-everyone' | url }}). We have also included in this website, recommendations on how to enhance accessibility using our components and patterns (for example [input text accessibility recommendations](../components/text_input/#accessibility)). However, that does not mean that any implementation that uses the developer assets, automatically complies with the Standard.

The way the design elements are used affect the accessibility of each page. For example [The order of heading elements (opens in new tab)](https://webdesign.tutsplus.com/articles/the-importance-of-heading-levels-for-assistive-technology--cms-31753){rel="noreferrer noopener" target="_blank"} should descend, based on the “depth” of the content and as such a `h4` element should not appear on a page before the first `h3` element declaration.

Be extra careful when including components within other components, when you are overwriting the default appearance of elements, or when you are implementing custom elements. 

