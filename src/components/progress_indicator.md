---
title: "Progress indicator"
date: 2022-02-01 00:01:01Z
description: "Use progress indicator informs users on their progress through a multi-step process on linear service flows."
---
The progress indicator informs users on their progress through a multi-step process on linear service flows. This helps users understand the progression of long processes and reduces uncertainty as they complete each screen.

## When to use this component
Use the progress indicator when a user is completing a [linear, multi-page service process](../../patterns/service_structure/#variant-1---linear-structure) that can be organized into two or more high-level steps or chapters.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			The progress indicator is meant to complement the standard <strong>Back</strong> and <strong>Continue</strong> navigation in a linear sequence. It should <strong>not</strong> be used as a navigation element on its own.
		</p>
    </div>
</div>

## When not to use this component
- **Long services with conditional logic.** Avoid using a progress indicator if the number or order of steps may change based on user input.
- **Nonlinear processes.** This component is not suitable for journeys where steps can be completed in any order, for example the [break the service into sections service structure](../../patterns/service_structure/#variant-2---break-the-service-into-sections).
- **Very short services.** Don’t use a progress indicator if the process has fewer than two steps or chapters. For simple services without clear sections, it's unnecessary and may add clutter.

## How it works
Place the progress at the top of the [main section](../../getting-started/page-template/#sections)(`<main>`) container, right above the `<h1>`. If your page includes an [error summary](../error_summary) the progress indicator must be placed right below it. For example the order of elements in a page with a progress indicator should look like this:

1. **Before main section** 
    1. [Back link](../back_link/) component
    2. [Phase banner](../phase_banner/) component, in case it is used
2. **Main section** 
    1. [Error summary](../error_summary/) component, in the case of errors.
    2. **Progress indicator**
    3. [Header 1 `<h1>`](../../styles/typography/#headings). If your using an input component and you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header accordingly. 
    4. Other [components](../../components/), [patterns](../../patterns/) or [typography](../../styles/typography/)

More information about element placement on a page can be found in the [page template](../../getting-started/page-template/#element-placement-order).

Always use the progress indicator with a [back link](../back_link) and a [continue primary button](../button/#primary-button) for navigation.

Make sure to use the correct variant depending on the number of steps.

### 2 to 5 steps variant

For services with more than 2 and less than 6 steps, use the progress indicator with step labels, step segments and step counters.

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

```html
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
```

Use the following classes on the `<li>` element for each step to indicate the step status:
- for **completed steps** use `govcy-step-indicator__segment govcy-step-indicator__segment--complete`
- for **current step** use `govcy-step-indicator__segment govcy-step-indicator__segment--current`
- for **uncompleted steps** use `govcy-step-indicator__segment` 

Use the following visually hidden text to help screen readers indicate the status of the step (for translations see the [content text section below](#component-text)): 
- for **completed steps** use`<span class="govcy-visually-hidden">completed</span>` 
- for **uncompleted steps** use `<span class="govcy-visually-hidden">not completed</span>` 

Use the `aria-current="step"` attribute indicates the current step.

Use the `<span class="govcy-visually-hidden">Step </span>` visually hidden text to help screen readers indicate the step in the counter (for translations see the [content text section below](#component-text)).

On mobile devices, the step labels are hidden.

### 6 to 10 steps variant

For services with more than 6 and less than 11 steps, use the progress indicator with step segments and step counters, without the step labels. You may also use this variant for services with less than 6 steps, if the step names are too long to comfortably fit in the step indicator. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-step-indicator">
    <ol class="govcy-step-indicator__segments" aria-hidden="true">
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--complete">
        </li>
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--current" aria-current="step">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
    </ol>
</div>
<div class="govcy-step-indicator__counter">
    <span class="govcy-visually-hidden">Step </span>
    <span class="govcy-step-indicator__current-counter">2</span> of 10
</div>
</div>

```html
<div class="govcy-step-indicator">
    <ol class="govcy-step-indicator__segments" aria-hidden="true">
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--complete">
        </li>
        <li class="govcy-step-indicator__segment govcy-step-indicator__segment--current" aria-current="step">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
        <li class="govcy-step-indicator__segment">
        </li>
    </ol>
</div>
<div class="govcy-step-indicator__counter">
    <span class="govcy-visually-hidden">Step </span>
    <span class="govcy-step-indicator__current-counter">2</span> of 10
</div>
```

Use the following classes on the `<li>` element for each step to indicate the step status:
- for **completed steps** use `govcy-step-indicator__segment govcy-step-indicator__segment--complete`
- for **current step** use `govcy-step-indicator__segment govcy-step-indicator__segment--current`
- for **uncompleted steps** use `govcy-step-indicator__segment` 

Use the `aria-hidden="true"` attribute on the `<ol>` element to hide the step labels from screen readers.

Use the `aria-current="step"` attribute indicates the current step.

Use the `<span class="govcy-visually-hidden">Step </span>` visually hidden text to help screen readers indicate the step in the counter (for translations see the [content text section below](#component-text)).

### More than 10 steps variant 

For services with more than 10 steps, use the progress indicator with only step counters.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-step-indicator__counter">
    <span class="govcy-visually-hidden">Step </span>
    <span class="govcy-step-indicator__current-counter">2</span> of 15
</div>
</div>

```html
<div class="govcy-step-indicator__counter">
    <span class="govcy-visually-hidden">Step </span>
    <span class="govcy-step-indicator__current-counter">2</span> of 15
</div>
```

Use the `<span class="govcy-visually-hidden">Step </span>` visually hidden text to help screen readers indicate the step in the counter (for translations see the [content text section below](#component-text)).

### Component text
Use the following text for the visually hidden text:

| Label | English | Greek |
| ---- | ---- | ---- |
| **Completed** | Completed | Ολοκληρώθηκε |
| **Not completed** | Not completed | Δεν ολοκληρώθηκε |
| **Step** | Step | Βήμα |
| **Of** | Of | από |

{.govcy-table}

## Accessibility
Be sure to:
- Use the following visually hidden text to help screen readers indicate the status of the step 
- Use the `aria-current="step"` attribute indicates the current step.
- Use the visually hidden text to help screen readers indicate the step in the counter 
- If using the 6 to 10 steps variant, use `aria-hidden="true"` to the `<ol>` element.