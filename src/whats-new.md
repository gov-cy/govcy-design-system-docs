---
title: "What's new"
"layout" : "base.njk"
showCategoryMenu : false
showIndexInCategoryMenu : false
showTOC: false
twoThirds: true
---

## v3.2.0 - 17/4/2025
Version 3.2.0 of the Design system has been released.

### Added {data-toc-exclude}
- [Progress indicator](https://gov-cy.github.io/govcy-design-system-docs/components/progress_indicator/). New component.
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-step-indicator">
    <ol class="govcy-step-indicator__segments">
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--complete">
            <span class="govcy-step-indicator__label">
                Personal information <span class="govcy-visually-hidden">completed</span>
            </span>
        </li>
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--current" aria-current="step">
            <span class="govcy-step-indicator__label">
                Phone number
            </span>
        </li>
        <li class="govcy-step-indicator__segment">
            <span class="govcy-step-indicator__label">
                Address <span class="govcy-visually-hidden">not completed</span>
            </span>
        </li>
        <li class="govcy-step-indicator__segment">
            <span class="govcy-step-indicator__label">
                Other details <span class="govcy-visually-hidden">not completed</span>
            </span>
        </li>
        <li class="govcy-step-indicator__segment">
            <span class="govcy-step-indicator__label">
                Consent <span class="govcy-visually-hidden">not completed</span>
            </span>
        </li>
    </ol>
</div>
<div class="govcy-step-indicator__counter">
    <span class="govcy-visually-hidden">Step </span>
    <span class="govcy-step-indicator__current-counter">2</span> of 5
</div>
</div>

### Changed {data-toc-exclude}
- [Summary List](https://gov-cy.github.io/govcy-design-system-docs/components/summary_list/): Changes on key with better spacing and better typography on mobile.

-----------------------

## v3.1.0 - 5/2/2025
Version 3.1.0 of the Design system has been released.

### Added {data-toc-exclude}
- [Accessibility statement pages pattern](https://gov-cy.github.io/govcy-design-system-docs/patterns/accessibility_pages/). New pattern.
- [Privacy policy pages pattern](https://gov-cy.github.io/govcy-design-system-docs/patterns/privacy_policy_page/). New pattern.
- [Date Input: Mobile friendly variant](https://gov-cy.github.io/govcy-design-system-docs/components/date_input/#mobile-friendly-input). New component variant. 
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4" style="max-width: 380px; width: 100%; margin-left: 0;">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="dateMobile-hint">
        <legend class="govcy-legend">Date input</legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="dateMobile-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_mobile">Day</label>
                    <input id="day_mobile" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_mobile">Month</label>
                    <select id="month_mobile" class="govcy-select">
                        <option value="" selected=""></option>
                        <option value="1">1</option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                        <option value="4">4</option>
                        <option value="5">5</option>
                        <option value="6">6</option>
                        <option value="7">7</option>
                        <option value="8">8</option>
                        <option value="9">9</option>
                        <option value="10">10</option>
                        <option value="11">11</option>
                        <option value="12">12</option>
                    </select>
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_mobile">Year</label>
                    <input id="year_mobile" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

- [Step by step: Always visible variant](https://gov-cy.github.io/govcy-design-system-docs/patterns/step_by_step_navigation/). New pattern variant. 
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-accordion govcy-accordion-steps govcy-mb-0">
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">1</div>
        <h3 class="govcy-pt-4">
            <span class="govcy-visually-hidden">Step 1, </span>Make an appointment
        </h3> 
        <div>
            <p><a href="#">Make an appointment</a> at the service point</p>
        </div>
    </div>
    <div class="govcy-accordion-item">
        <div class="govcy-accordion-step">2</div>
        <h3 class="govcy-pt-4">
                <span class="govcy-visually-hidden">Step 2, </span>Pick up
        </h3>
        <div>
            <p>Pick up your documents from the service point</p>
        </div>
    </div>
</div>
</div>

- [Confirmation pages: Next steps variant](https://gov-cy.github.io/govcy-design-system-docs/patterns/confirmation-pages/#next-steps). New pattern variant. 

### Fixed {data-toc-exclude}
- [Details component](https://gov-cy.github.io/govcy-design-system-docs/components/details/): Better bottom spacing.
- [Summary List](https://gov-cy.github.io/govcy-design-system-docs/components/summary_list/): Better spacing between key and value.
- [Conditional radio](https://gov-cy.github.io/govcy-design-system-docs/components/radio/#conditional-radios-(revealing-a-question)): Better font size for labels and legends inside conditional radios.

-----------------------

## v3.0.0 - 18/6/2024

Total redesign of the design system, with branding and styling changes. 

### Added {data-toc-exclude}
We have added new elements to the design system:
- 11 new components
	- accordion 
	- character count
	- cookie banner
	- data tables
	- date picker
	- inset text
	- phase banner
	- summary list
	- tag
	- textarea
	- warning text
- 1 style
	- Images
- 14 patterns
	- accessibility statement page
	- addresses
	- bank details
	- confirm an email address
	- confirmation pages
	- contact page
	- cookies page
	- filter results
	- gender or sex
	- numeric inputs
	- privacy policy
	- social insurance number
	- step by step navigation
	- task list page

### Changed {data-toc-exclude}

All styles, components and patters have changed. 

[Read the full change log (opens in new tab)](https://github.com/gov-cy/govcy-design-system/blob/main/CHANGELOG.md){rel="noreferrer noopener" target="_blank"}.