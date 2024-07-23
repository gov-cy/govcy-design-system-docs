---
title: "Cookies page and cookies consent"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Tell users about the cookies you’re setting on their device and let them accept or reject different types of non-essential cookies."
---

Tell users about the cookies you’re setting on their device and let them accept or reject different types of non-essential cookies.

## When to use this pattern
Use a cookies page to tell users about any cookies your service or website uses - or any other technologies that work in a similar way and store information on their device.

## How it works

A cookies page helps you to be transparent about the cookies you’re using.

Keep use of cookies to a minimum, and be transparent about the ones you do use. You must:

- use as few cookies as possible, and stop setting any cookies that are not needed anymore
- store the smallest amount of information that you need, for as short a time as necessary
- publish a cookie policy telling users about the cookies you’re using
- get users’ consent before you set any cookies that are not essential to providing the service

The Cookie policy can be accessed by a link at the footer of any service and website.

This page should have the following sections and items:

- Cookie policy description
- the purpose and scope of the policy
- what information is collected and for what purposes
- contact information regarding the policy
- cookie settings
- review of policy
- go back link
- make the page available in all service / site languages 

Make sure to include the name of the service in the cookie policy description to help users understand that the policy you’re talking about is different from the one set by the main gov.cy platform, or a different site or service.

Do not use:

- breadcrumbs
- red text to warn people

### Preparing your cookies page

You must publish a cookies page by the time your service goes into public beta. The cookies page must be unique to your service: do not link to the cookie policy for the main gov.cy website.

Follow the steps below to create a cookie policy.

1. audit your cookies.
2. categorise your cookies.
3. write your cookies page.

### Writing your cookies page

Work with your organisation’s privacy expert to write the cookies page.

The cookie policy must be written in plain language.

List the cookies individually on the cookies page, under the relevant category. For each cookie, give:

- the cookie name
- a brief description of what the cookie does
- for third party cookies, who is setting the cookie (for example, social media websites may require users to accept their cookies in order to provide their functionality as part of your service)
- when the cookie will expire

Do not bury your cookie policy in a ‘terms and conditions’ page.

Have an agreed process for updating the cookie policy when you add or remove a cookie. Make sure the relevant people on your team know what the process is.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not copy the examples in this page without amending the specifics. Make sure to adjust your cookies page according to your case.
		</p>
    </div>
</div>

### Strictly necessary cookies 
See below examples of the cookies page when using only ‘strictly necessary’ cookies. A cookie is ‘strictly necessary’ if the service will not work without it.

*Example in English*
[Open in new tab](../../samples/cookies-essential-en/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/cookies-essential-en/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>


*Example in Greek*
[Open in new tab](../../samples/cookies-essential-el/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/cookies-essential-el/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>

### Optional cookies that need consent for
You do not need the user’s consent to set essential or ‘strictly necessary’ cookies. A cookie is ‘strictly necessary’ if the service will not work without it.

You must get the user’s consent before you set any cookies that are not strictly necessary.

You can get the user’s consent:

- by using a cookie banner
- by letting the user change and save their settings on the cookies page

#### Cookie banner
Use the [cookie banner component](../../components/cookie_banner) to get the user’s consent. The component should include the following:

- Text informing the user that the site or service uses cookies
- Accept cookies option
- Decline cookies option
- Adjust cookies option (settings)

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-cookie-consent-banner">
    <div class="govcy-container">
        <h3>Cookies on xyz service</h3>
        <p>We use some essential cookies to make this website work.</p>
        <p>We’d like to set additional cookies to understand how you use the service, remember your settings and improve government services.</p>
        <div class="govcy-d-flex govcy-align-items-center">
        <a href="#" class="govcy-btn-primary me-2">Accept cookies</a>
        <a href="#" class="govcy-btn-primary me-2">Reject cookies</a>
        <a href="#">Adjust cookies</a>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-cookie-consent-banner">
    <div class="govcy-container">
        <h3>Cookies on xyz service</h3>
        <p>We use some essential cookies to make this website work.</p>
        <p>We’d like to set additional cookies to understand how you use the service, remember your settings and improve government services.</p>
        <div class="govcy-d-flex govcy-align-items-center">
        <a href="#" class="govcy-btn-primary me-2">Accept cookies</a>
        <a href="#" class="govcy-btn-primary me-2">Reject cookies</a>
        <a href="#">Adjust cookies</a>
        </div>
    </div>
</div>
```

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-cookie-consent-banner">
    <div class="govcy-container">
        <h3>Cookies στην υπηρεσία xyz</h3>
        <p>Χρησιμοποιούμε ορισμένα απαραίτητα cookies για να λειτουργήσει αυτός ο ιστότοπος.</p>
        <p>Θα θέλαμε να ορίσουμε επιπλέον cookies για να κατανοήσουμε πώς χρησιμοποιείτε την υπηρεσία, να θυμόμαστε τις ρυθμίσεις σας και να βελτιώνουμε τις κρατικές υπηρεσίες.</p>
        <div class="govcy-d-flex govcy-align-items-center">
        <a href="#" class="govcy-btn-primary me-2">Αποδοχή cookies</a>
        <a href="#" class="govcy-btn-primary me-2">Απόρριψη cookies</a>
        <a href="#">Προσαρμόστε τα cookies</a>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-cookie-consent-banner">
    <div class="govcy-container">
        <h3>Cookies στην υπηρεσία xyz</h3>
        <p>Χρησιμοποιούμε ορισμένα απαραίτητα cookies για να λειτουργήσει αυτός ο ιστότοπος.</p>
        <p>Θα θέλαμε να ορίσουμε επιπλέον cookies για να κατανοήσουμε πώς χρησιμοποιείτε την υπηρεσία, να θυμόμαστε τις ρυθμίσεις σας και να βελτιώνουμε τις κρατικές υπηρεσίες.</p>
        <div class="govcy-d-flex govcy-align-items-center">
        <a href="#" class="govcy-btn-primary me-2">Αποδοχή cookies</a>
        <a href="#" class="govcy-btn-primary me-2">Απόρριψη cookies</a>
        <a href="#">Προσαρμόστε τα cookies</a>
        </div>
    </div>
</div>
```
If the user selects to adjust the cookies, the cookies page should open, displaying the cookies and what each one does. They should be given the ability to adjust the cookies, accept all, save their settings or deny the cookies.

The popup should appear at the top of the page, in the ["body start" section](../../getting-started/page-template/#sections) of the page.

Do not use different backgrounds with low opacity to hide the main content of the pages.

See below an example of a page with the cookie banner.

[Open in new tab](../../samples/cookies-with-concent/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/cookies-with-concent/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>

#### Cookies page, letting users accept or reject cookies
List the optional cookies and their purpose and use [radios](../../components/radio) and a [button](../../components/button) to let users accept or reject non-essential cookies.

Load the page with the radios set to ‘no’ on the user’s first visit. If they’ve previously used the service and set their preferences, load the page with those preferences selected.

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h2 data-toc-exclude>Analytics cookies (optional)</h2>
<p>With yout permission, we use additional analytics to collect data about how you use this service. This infomation helps us improve our service.</p>
<table class="govcy-table">
	<thead>
		<tr class="govcy-br-input">
			<th scope="col">Name</th>
			<th scope="col">Purpose</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>_abc</th>
			<td>This cookie helps us counts how many people visited the service, by telling us if you've visited before.</td>
		</tr>
		<tr>
			<th>_efg</th>
			<td>This cookie helps us calculate the time spend in the service.</td>
		</tr>
	</tbody>
</table>
<div class="govcy-form">
	<fieldset class="govcy-fieldset">
		<legend class="govcy-legend">Do you want to accept analytics cookies?</legend>
		<div class="govcy-form-control">
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-yes">
				<label class="govcy-label" for="option-yes">Yes</label>
			</div>
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-no" checked>
				<label class="govcy-label" for="option-no">No</label>
			</div>
		</div>
	</fieldset>
	<button type="button" class="govcy-btn-primary">Save cookie settings</button>
</div>
</div>

*HTML code*
```html
<h2>Analytics cookies (optional)</h2>
<p>With yout permission, we use additional analytics to collect data about how you use this service. This infomation helps us improve our service.</p>
<table class="govcy-table">
	<thead>
		<tr class="govcy-br-input">
			<th scope="col">Name</th>
			<th scope="col">Purpose</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>_abc</th>
			<td>This cookie helps us counts how many people visited the service, by telling us if you've visited before.</td>
		</tr>
		<tr>
			<th>_efg</th>
			<td>This cookie helps us calculate the time spend in the service.</td>
		</tr>
	</tbody>
</table>
<form action="" class="govcy-form" novalidate>
	<fieldset class="govcy-fieldset">
		<legend class="govcy-legend">Do you want to accept analytics cookies?</legend>
		<div class="govcy-form-control">
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-yes">
				<label class="govcy-label" for="option-yes">Yes</label>
			</div>
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-no" checked>
				<label class="govcy-label" for="option-no">No</label>
			</div>
		</div>
	</fieldset>
	<button type="submit" class="govcy-btn-primary">Save cookie settings</button>
</form>
```

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h2 data-toc-exclude>Αναλυτικά cookies (προαιρετικά)</h2>
<p>Με την άδειά σας, χρησιμοποιούμε πρόσθετα αναλυτικά στοιχεία για τη συλλογή δεδομένων σχετικά με τον τρόπο χρήσης αυτής της υπηρεσίας. Αυτές οι πληροφορίες μας βοηθούν να βελτιώσουμε τις υπηρεσίες μας.</p>
<table class="govcy-table">
	<thead>
		<tr class="govcy-br-input">
			<th scope="col">Όνομα</th>
			<th scope="col">Σκοπός</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>_abc</th>
			<td>Αυτό το cookie μας βοηθά να μετράμε πόσα άτομα επισκέφτηκαν την υπηρεσία, λέγοντάς μας εάν την έχετε επισκεφτεί στο παρελθόν.</td>
		</tr>
		<tr>
			<th>_efg</th>
			<td>Αυτό το cookie μας βοηθά να υπολογίσουμε τον χρόνο που χρησιμοποιείτε την υπηρεσία.</td>
		</tr>
	</tbody>
</table>
<div class="govcy-form">
	<fieldset class="govcy-fieldset">
		<legend class="govcy-legend">Θέλετε να αποδεχτείτε τα cookies αναλυτικών στοιχείων;</legend>
		<div class="govcy-form-control">
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-yes-el">
				<label class="govcy-label" for="option-yes-el">Ναι</label>
			</div>
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-no-el" checked>
				<label class="govcy-label" for="option-no-el">Όχι</label>
			</div>
		</div>
	</fieldset>
	<button type="button" class="govcy-btn-primary">Αποθήκευση ρυθμίσεων cookie</button>
</div>
</div>

*HTML code*
```html
<h2>Αναλυτικά cookies (προαιρετικά)</h2>
<p>Με την άδειά σας, χρησιμοποιούμε πρόσθετα αναλυτικά στοιχεία για τη συλλογή δεδομένων σχετικά με τον τρόπο χρήσης αυτής της υπηρεσίας. Αυτές οι πληροφορίες μας βοηθούν να βελτιώσουμε τις υπηρεσίες μας.</p>
<table class="govcy-table">
	<thead>
		<tr class="govcy-br-input">
			<th scope="col">Όνομα</th>
			<th scope="col">Σκοπός</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>_abc</th>
			<td>Αυτό το cookie μας βοηθά να μετράμε πόσα άτομα επισκέφτηκαν την υπηρεσία, λέγοντάς μας εάν την έχετε επισκεφτεί στο παρελθόν.</td>
		</tr>
		<tr>
			<th>_efg</th>
			<td>Αυτό το cookie μας βοηθά να υπολογίσουμε τον χρόνο που χρησιμοποιείτε την υπηρεσία.</td>
		</tr>
	</tbody>
</table>
<form action="" class="govcy-form" novalidate>
	<fieldset class="govcy-fieldset">
		<legend class="govcy-legend">Θέλετε να αποδεχτείτε τα cookies αναλυτικών στοιχείων;</legend>
		<div class="govcy-form-control">
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-yes-el">
				<label class="govcy-label" for="option-yes-el">Ναι</label>
			</div>
			<div class="govcy-radio">
				<input class="govcy-radio-input" type="radio" name="cookiesRadio" id="option-no-el" checked>
				<label class="govcy-label" for="option-no-el">Όχι</label>
			</div>
		</div>
	</fieldset>
	<button type="submit" class="govcy-btn-primary">Αποθήκευση ρυθμίσεων cookie</button>
</form>
```

When the user sets or changes their cookie preferences, use a green notification banner at the top of the [main section](../../getting-started/page-template/#sections) before the `<h1>`, to confirm that the service has updated the user’s cookie settings. Make sure focus is on the success banner and that the message is also read by screen readers.

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-notification govcy-br-5 govcy-br-success govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-success">Success</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6 govcy-fw-bold">You’ve set your cookie preferences.</p>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-notification govcy-br-5 govcy-br-success govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-success">Success</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6 govcy-fw-bold">You’ve set your cookie preferences.</p>
    </div>
</div>
```
*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-notification govcy-br-5 govcy-br-success govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-success">Επιτυχία</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6 govcy-fw-bold">Έχετε ορίσει τις προτιμήσεις σας για τα cookies.</p>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-notification govcy-br-5 govcy-br-success govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-success">Επιτυχία</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6 govcy-fw-bold">Έχετε ορίσει τις προτιμήσεις σας για τα cookies.</p>
    </div>
</div>
```
#### Cookies page with consent examples
See below examples of the cookies page when including the consent for optional cookies. 

*Example in English*
[Open in new tab](../../samples/cookies-optional-en/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/cookies-optional-en/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>


*Example in Greek*
[Open in new tab](../../samples/cookies-optional-el/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/cookies-optional-el/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>
