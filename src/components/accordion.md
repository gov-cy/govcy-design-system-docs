---
title: "Accordion"
date: 2022-02-01 00:01:01Z
description: "The accordion component lets users show and hide sections of related content on a page."
---

The accordion component lets users show and hide sections of related content on a page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion">
    <div class="govcy-accordion-item">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
            Writing well for the web
        </button>
        </h2>
        <div id="collapseOne" class="govcy-accordion-collapse collapse show" aria-label="headingOne">
            <div class="govcy-accordion-body">
                This is the content for Writing well for the web.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                Writing well for specialists
            </button>
        </h2>
        <div id="collapseTwo" class="govcy-accordion-collapse collapse" aria-label="headingTwo">
            <div class="govcy-accordion-body">
                This is the content for Writing well for specialists.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingThree">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                Know your audience
            </button>
        </h2>
        <div id="collapseThree" class="govcy-accordion-collapse collapse" aria-label="headingThree">
            <div class="govcy-accordion-body">
                This is the content for Know your audience.
            </div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-accordion">
    <div class="govcy-accordion-item">
        <h2 class="govcy-accordion-header" id="headingOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
            Writing well for the web
        </button>
        </h2>
        <div id="collapseOne" class="govcy-accordion-collapse collapse show" aria-label="headingOne">
            <div class="govcy-accordion-body">
                This is the content for Writing well for the web.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <h2 class="govcy-accordion-header" id="headingTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                Writing well for specialists
            </button>
        </h2>
        <div id="collapseTwo" class="govcy-accordion-collapse collapse" aria-label="headingTwo">
            <div class="govcy-accordion-body">
                This is the content for Writing well for specialists.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <h2 class="govcy-accordion-header" id="headingThree">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                Know your audience
            </button>
        </h2>
        <div id="collapseThree" class="govcy-accordion-collapse collapse" aria-label="headingThree">
            <div class="govcy-accordion-body">
                This is the content for Know your audience.
            </div>
        </div>
    </div>
</div>
```

## When to use this component
Only use an accordion if there’s evidence it’s helpful for the user to:
- see an overview of multiple, related sections of content
- choose to show and hide sections that are relevant to them
- look across information that might otherwise be on different pages

Accordions can also work well for people who use a service regularly. For example, users of case-working systems who need to do familiar tasks quickly.

Test with users to decide if using an accordion outweighs the potential problems with hiding content.

## When not to use this component
Accordions hide content from the user. Not all users will notice them or understand how they work. For this reason, you should only use them in specific situations and if user research supports it.

Do not use an accordion for content that all users need to see. It’s usually better to:
- simplify and reduce the amount of content  
- split the content across multiple pages  
- keep the content on a single page, separated by headings  
- use a list of links at the start of the page (known as ‘anchor links’) to take the user to particular sections of a page

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Accordions work best for simple content and links. Do not use accordions to split up a series of <a href="../../patterns/question_pages/">questions</a>. Use separate pages instead. See the <a href="../../patterns/service_structure/">Structuring a service</a> pattern for more information.
		</p>
    </div>
</div>

Do not put accordions within accordions, as it will make content difficult to find.

Do not use the accordion component if the amount of content inside will make the page slow to load.

## How it works
The accordion component should only exist in the [main section](../../getting-started/page-template/#sections). The component uses JavaScript. To use it with the gov.cy [developer assets](../../getting-started/developer-assets/), make sure to include the main JavaScript file in your page.

An accordion will usually start with all sections hidden. To show a section, the user can interact anywhere in the heading button.  

The heading button includes all of these areas:  
- heading text  
- summary line (if you decide to add one)  
- call-to-action text to ‘show’ or ‘hide’

It’s not always necessary to accompany the accordion with a header. In some instances the use of just the accordion toggle button should be enough.

### Starting with sections open
Users might need some sections to be open from the start. If they leave and then return to the page, they might also need sections they opened to stay open.

To start with a section open:
- remove the class `collapsed` from the heading button
- set the heading button `aria-expanded` to `"true"`
- add the class `show` to the accordion item's body (elements with class `govcy-accordion-collapse`) 

### Do not disable sections
Disabling controls is normally confusing for users. If there is no content for a section, either remove the section or, if this would be confusing for your users, explain why there is no content when the section is opened.

### Show content on print
Add the `govcy-d-print-block` class to always display individual items' content (elements with class `govcy-accordion-collapse`), on print media, regardless if the accordion item is collapsed or expanded.

## With borders
Use the accordion with borders only if evidence exist that the default variant is confusing for the users.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion">
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingOneBordered">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseOneBordered" aria-expanded="true" aria-controls="collapseOneBordered">
            Writing well for the web
        </button>
        </h2>
        <div id="collapseOneBordered" class="govcy-accordion-collapse collapse show" aria-label="headingOneBordered">
            <div class="govcy-accordion-body">
                This is the content for Writing well for the web.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingTwoBordered">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseTwoBordered" aria-expanded="false" aria-controls="collapseTwoBordered">
                Writing well for specialists
            </button>
        </h2>
        <div id="collapseTwoBordered" class="govcy-accordion-collapse collapse" aria-label="headingTwoBordered">
            <div class="govcy-accordion-body">
                This is the content for Writing well for specialists.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingThreeBordered">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseThreeBordered" aria-expanded="false" aria-controls="collapseThreeBordered">
                Know your audience
            </button>
        </h2>
        <div id="collapseThreeBordered" class="govcy-accordion-collapse collapse" aria-label="headingThreeBordered">
            <div class="govcy-accordion-body">
                This is the content for Know your audience.
            </div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-accordion">
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 class="govcy-accordion-header" id="headingOneBordered">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseOneBordered" aria-expanded="true" aria-controls="collapseOneBordered">
            Writing well for the web
        </button>
        </h2>
        <div id="collapseOneBordered" class="govcy-accordion-collapse collapse show" aria-label="headingOneBordered">
            <div class="govcy-accordion-body">
                This is the content for Writing well for the web.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 class="govcy-accordion-header" id="headingTwoBordered">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseTwoBordered" aria-expanded="false" aria-controls="collapseTwoBordered">
                Writing well for specialists
            </button>
        </h2>
        <div id="collapseTwoBordered" class="govcy-accordion-collapse collapse" aria-label="headingTwoBordered">
            <div class="govcy-accordion-body">
                This is the content for Writing well for specialists.
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item govcy-accordion-bordered">
        <h2 class="govcy-accordion-header" id="headingThreeBordered">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseThreeBordered" aria-expanded="false" aria-controls="collapseThreeBordered">
                Know your audience
            </button>
        </h2>
        <div id="collapseThreeBordered" class="govcy-accordion-collapse collapse" aria-label="headingThreeBordered">
            <div class="govcy-accordion-body">
                This is the content for Know your audience.
            </div>
        </div>
    </div>
</div>
```

## Step by step accordion
Step by step accordion is mostly used for services. Refer to [step by step navigation pattern](../../patterns/step_by_step_navigation/) for more details.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepOne" aria-expanded="true" aria-controls="collapseStepOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">2</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepTwo" aria-expanded="false" aria-controls="collapseStepTwo">
                <span class="govcy-visually-hidden-error">Step 2, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 class="govcy-accordion-header" id="headingStepOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepOne" aria-expanded="true" aria-controls="collapseStepOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">2</div>
        <h2 class="govcy-accordion-header" id="headingStepTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepTwo" aria-expanded="false" aria-controls="collapseStepTwo">
                <span class="govcy-visually-hidden-error">Step 2, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
```
### Step by step using “and”
Use ‘and’ to show when you can or must complete steps at the same time.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepAndOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepAndOne" aria-expanded="true" aria-controls="collapseStepAndOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepAndOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepAndOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step govcy-accordion-step-conditional">and</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepAndTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepAndTwo" aria-expanded="false" aria-controls="collapseStepAndTwo">
                <span class="govcy-visually-hidden-error">And, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepAndTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepAndTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 class="govcy-accordion-header" id="headingStepAndOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepAndOne" aria-expanded="true" aria-controls="collapseStepAndOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepAndOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepAndOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step govcy-accordion-step-conditional">and</div>
        <h2 class="govcy-accordion-header" id="headingStepAndTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepAndTwo" aria-expanded="false" aria-controls="collapseStepAndTwo">
                <span class="govcy-visually-hidden-error">And, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepAndTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepAndTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
```

### Step by step using “or”
Use ‘or’ to show when there’s a choice between 2 steps.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepOrOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepOrOne" aria-expanded="true" aria-controls="collapseStepOrOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepOrOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepOrOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step govcy-accordion-step-conditional">or</div>
        <h2 data-toc-exclude class="govcy-accordion-header" id="headingStepOrTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepOrTwo" aria-expanded="false" aria-controls="collapseStepOrTwo">
                <span class="govcy-visually-hidden-error">Or, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepOrTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepOrTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-accordion govcy-accordion-steps">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h2 class="govcy-accordion-header" id="headingStepOrOne">
        <button class="govcy-accordion-button" type="button" data-govcy-target="#collapseStepOrOne" aria-expanded="true" aria-controls="collapseStepOrOne">
            <span class="govcy-visually-hidden-error">Step 1, </span>Make sure you’re allowed to drive
        </button>
        </h2>
        <div id="collapseStepOrOne" class="govcy-accordion-collapse collapse show" aria-label="headingStepOrOne">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Check what age you can drive</a></li>
                    <li><a href="#">Requirements for driving legally</a></li>
                    <li><a href="#">Driving eyesight rules</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step govcy-accordion-step-conditional">or</div>
        <h2 class="govcy-accordion-header" id="headingStepOrTwo">
            <button class="govcy-accordion-button collapsed" type="button" data-govcy-target="#collapseStepOrTwo" aria-expanded="false" aria-controls="collapseStepOrTwo">
                <span class="govcy-visually-hidden-error">Or, </span>Get a provisional licence
            </button>
        </h2>
        <div id="collapseStepOrTwo" class="govcy-accordion-collapse collapse" aria-label="headingStepOrTwo">
            <div class="govcy-accordion-body">
                <p>Most people can start learning to drive when they’re 17.</p>
                <ul class="govcy-list-spaced govcy-list-unstyled">
                    <li><a href="#">Apply for your first provisional driving licence</a> - €20 to €50</li>
                </ul>
            </div>
        </div>
    </div>
</div>
```

## Accessibility
Make sure:
- you add `aria-expanded` attribute to the control element. Using the gov.cy developer assets, the value of the attribute is controlled automatically. If the collapsible element is closed by default, the attribute on the control element should have a value of `aria-expanded="false"`. If you’ve set the collapsible element to be open by default using the `show` class, set `aria-expanded="true"` on the control instead
- you add the `aria-controls` attribute to the control element, containing the `id` of the collapsible element
- for Step by step accordions, use `<span class="govcy-visually-hidden-error">Step 1, </span>` to allow screen readers read the step number
- if the control element’s HTML element is not a button (e.g., an `<a>` or `<div>`), the attribute `role="button"` should be added to the element
- use meaningful expansion button labels. Aim for informative labels like “Get a provisional licence” rather than vague ones like “Click here.”