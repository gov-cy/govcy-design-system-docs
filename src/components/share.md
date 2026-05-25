---
title: "Share"
date: 2022-02-01 00:01:01Z
description: "Use the share component to let users share content using apps installed on their device via the Web Share API, with fallback options such as SMS and Email."
---
Use the share component to let users share content using apps installed on their device via the Web Share API, with fallback options such as SMS and Email.

## When to use this component

Use this component when users need to send a link or message to another person using their preferred app.

Typical examples:
- Ask another parent to provide consent through a shared link.
- Let users forward a service URL and message through SMS or Email.

## When not to use this component

Do not use this component when sharing is not essential to completing the user journey.

Avoid using it when:
- Users must always complete the flow only inside your service.
- The shared content contains sensitive information that should not be sent through third-party apps.
- Your service requires auditable, controlled delivery instead of user-initiated sharing.

## How it works

The share component should only exist in the [main section](../../getting-started/page-template/#sections). The component uses JavaScript. To use it with the gov.cy [developer assets](../../getting-started/developer-assets/), make sure to include the main JavaScript file in your page.

To use this component, create a root element with class `govcy-share` and define content via `data-govcy-*` attributes.

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

*HTML code*
```html
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
```

The component is progressively enhanced:
- If `navigator.share` is available, the **Share** action is shown and triggers the native share dialog.
- If `navigator.share` is not available, the **Share** action is hidden.
- SMS and Email fallback links are always available when present in markup.
- Copy action is available only when `navigator.clipboard.writeText` is supported.

### Data attributes

The component uses the following data attributes:

- `data-govcy-share-title`: title passed to Web Share API and used in `mailto` subject.
- `data-govcy-share-text`: main message content. This is used for SMS body, Email body, Copy, and message preview.
- `data-govcy-share-url`: optional URL passed separately to Web Share API.
- `data-govcy-share-copy-success-message`: optional toast message shown after successful copy. If not provided, the default message `Copied` will be used.

### Optional elements

The share component was designed to offer fallback options when a device or browser does not support a sharing option. To ensure maximum device compatibility, it is recommended to use all available elements, though the component can function without them.
 
The following elements are optional and safe to omit:
- `.govcy-share__sms`
- `.govcy-share__email`
- `.govcy-share__message`
- `.govcy-share__copy-btn`
- `.govcy-share__toast`

For example, a variant with share and fallback links only is also valid:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
    <div
      class="govcy-share"
      data-govcy-share-title="Request for consent"
      data-govcy-share-text="Give your consent here https://url to issue passport for Andreas Andreou"
      data-govcy-share-url="https://url"
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
    </div>
</div>

*HTML code*
```html
    <div
      class="govcy-share"
      data-govcy-share-title="Request for consent"
      data-govcy-share-text="Give your consent here https://url to issue passport for Andreas Andreou"
      data-govcy-share-url="https://url"
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
    </div>
```


### JavaScript initialization

The component is auto-initialized by UDS on `DOMContentLoaded`.

If content is rendered dynamically on the client, initialize manually:

```js
parent.querySelectorAll('.govcy-share').forEach((element) => {
  new GOVCY.Share(element)
})
```

### Component text
Use the following text:

| Text                     | English              | Greek                   |
| ------------------------ | -------------------- | ----------------------- |
| **Share button**         | Share                | Share (κοινή χρήση)     |
| **SMS button**           | SMS                  | SMS                     |
| **Email button**         | Email                | Email                   |
| **Notification content** | Notification content | Περιεχόμενο ειδοποίησης |
| **Copy button**          | Copy                 | Αντιγραφή               |
| **Copy success message** | Copied               | Αντιγράφηκε             |

{.govcy-table}

## Accessibility

- Keep icon SVGs with `aria-hidden="true"`.
- For anchor-as-button actions, use `role="button"` and `tabindex="0"`.
- Keyboard activation supports:
  - `Enter`
  - `Space`
- Copy feedback toast uses:
  - `role="alert"`
  - `aria-live="assertive"`
  - `aria-atomic="true"`

## Browser and platform notes

- `navigator.share` is available only in supported secure contexts.
- On some devices/apps, shared URL display may vary; include critical URL directly in `data-govcy-share-text` when required.
- Clipboard API support also depends on browser/security context.

