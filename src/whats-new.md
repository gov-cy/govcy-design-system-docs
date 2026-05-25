---
title: "What's new"
"layout" : "base.njk"
showCategoryMenu : false
showIndexInCategoryMenu : false
showTOC: false
twoThirds: true
---

## v3.3.0 - 25/5/2026
Version 3.3.0 of the Design system has been released.

### Added {data-toc-exclude}
- [Share component](https://gov-cy.github.io/govcy-design-system-docs/components/share/). New component ([issue](https://github.com/gov-cy/govcy-design-system/issues/158){rel="noreferrer noopener" target="_blank"}).
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
  <div
      class="govcy-share"
      data-govcy-share-title="Request for consent"
      data-govcy-share-text="Give your consent here https://url to issue passport for Andreas Andreou"
      data-govcy-share-url="https://url"
      data-govcy-share-copy-success-message="Copied"
    >
      <!-- Buttons list -->
      <ul class="govcy-list-unstyled govcy-share__list">
        <!-- Share button -->
        <li class="govcy-mb-2 govcy-share__item">
          <a
            tabindex="0"
            role="button"
            class="govcy-link-no-visited-state govcy-share__btn"
          >
            <svg
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              class="govcy-share__icon"
              viewBox="0 0 16 16"
            >
              <path
                fill-rule="evenodd"
                d="M3.5 6a.5.5 0 0 0-.5.5v8a.5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5v-8a.5.5 0 0 0-.5-.5h-2a.5.5 0 0 1 0-1h2A1.5 1.5 0 0 1 14 6.5v8a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 14.5v-8A1.5 1.5 0 0 1 3.5 5h2a.5.5 0 0 1 0 1z"
              />
              <path
                fill-rule="evenodd"
                d="M7.646.146a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 1.707V10.5a.5.5 0 0 1-1 0V1.707L5.354 3.854a.5.5 0 1 1-.708-.708z"
              />
            </svg>
            Share
          </a>
        </li>
        <!-- SMS button -->
        <li class="govcy-mb-2 govcy-share__item">
          <a
            role="button"
            class="govcy-link-no-visited-state govcy-share__sms"
            href="sms:?body="
          >
            <svg
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              class="govcy-share__icon"
              viewBox="0 0 16 16"
            >
              <path
                d="M2 1a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h9.586a2 2 0 0 1 1.414.586l2 2V2a1 1 0 0 0-1-1zm12-1a2 2 0 0 1 2 2v12.793a.5.5 0 0 1-.854.353l-2.853-2.853a1 1 0 0 0-.707-.293H2a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2z"
              />
              <path
                d="M3 3.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5M3 6a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9A.5.5 0 0 1 3 6m0 2.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5"
              />
            </svg>
            SMS
          </a>
        </li>
        <!-- Email button -->
        <li class="govcy-mb-2 govcy-share__item">
          <a
            role="button"
            class="govcy-link-no-visited-state govcy-share__email"
            href="mailto:?subject=&body="
          >
            <svg
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              class="govcy-share__icon"
              viewBox="0 0 16 16"
            >
              <path
                d="M2 2a2 2 0 0 0-2 2v8.01A2 2 0 0 0 2 14h5.5a.5.5 0 0 0 0-1H2a1 1 0 0 1-.966-.741l5.64-3.471L8 9.583l7-4.2V8.5a.5.5 0 0 0 1 0V4a2 2 0 0 0-2-2zm3.708 6.208L1 11.105V5.383zM1 4.217V4a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v.217l-7 4.2z"
              />
              <path
                d="M14.247 14.269c1.01 0 1.587-.857 1.587-2.025v-.21C15.834 10.43 14.64 9 12.52 9h-.035C10.42 9 9 10.36 9 12.432v.214C9 14.82 10.438 16 12.358 16h.044c.594 0 1.018-.074 1.237-.175v-.73c-.245.11-.673.18-1.18.18h-.044c-1.334 0-2.571-.788-2.571-2.655v-.157c0-1.657 1.058-2.724 2.64-2.724h.04c1.535 0 2.484 1.05 2.484 2.326v.118c0 .975-.324 1.39-.639 1.39-.232 0-.41-.148-.41-.42v-2.19h-.906v.569h-.03c-.084-.298-.368-.63-.954-.63-.778 0-1.259.555-1.259 1.4v.528c0 .892.49 1.434 1.26 1.434.471 0 .896-.227 1.014-.643h.043c.118.42.617.648 1.12.648m-2.453-1.588v-.227c0-.546.227-.791.573-.791.297 0 .572.192.572.708v.367c0 .573-.253.744-.564.744-.354 0-.581-.215-.581-.8Z"
              />
            </svg>
            Email
          </a>
        </li>
      </ul>
      <!-- Message -->
      <p class="govcy-fw-bolder">Notification content</p>
      <pre class="govcy-share__message"></pre>
      <!-- Copy button -->
      <ul class="govcy-list-unstyled govcy-share__list">
        <li class="govcy-mb-2 govcy-share__item">
          <a
            tabindex="0"
            role="button"
            class="govcy-link-no-visited-state govcy-share__copy-btn"
          >
            <svg
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              class="govcy-share__icon"
              viewBox="0 0 16 16"
            >
              <path
                fill-rule="evenodd"
                d="M4 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2zm2-1a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1zM2 5a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1v-1h1v1a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h1v1z"
              />
            </svg>
            Copy notification
          </a>
        </li>
      </ul>
      <!-- Toast used when copy is successful -->
      <div
        class="govcy-share__toast"
        role="alert"
        aria-live="assertive"
        aria-atomic="true"
      ></div>
    </div>
</div>

### Changed {data-toc-exclude}
- Fixed issue `.govcy-link-no-visited-state:visited:focus` color [issue](https://github.com/gov-cy/govcy-design-system/issues/154){rel="noreferrer noopener" target="_blank"}

-----------------------

## v3.2.1 - 19/5/2026
Version 3.2.1 of the Design system has been released.

### Changed {data-toc-exclude}
- Fixed [Date Picker's](https://gov-cy.github.io/govcy-design-system-docs/components/date_picker/) next years group button [issue](https://github.com/gov-cy/govcy-design-system/issues/203){rel="noreferrer noopener" target="_blank"}

-----------------------

## v3.2.0 - 24/4/2026
Developer assets are the same with v3.2.0, this update concerns the documentation.

### Added {data-toc-exclude}
- [Cannot use the service pages (eligibility)](https://gov-cy.github.io/govcy-design-system-docs/patterns/cannot-use-the-service/). New pattern.
- [How to handle errors and problems in a service](https://gov-cy.github.io/govcy-design-system-docs/guides/how_to_handle_errors_and_problems/). New guide.

### Updated {data-toc-exclude}
- [Structuring a service](https://gov-cy.github.io/govcy-design-system-docs/patterns/service_structure/). Updated pattern to include eligibility and submission checks.

-----------------------

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