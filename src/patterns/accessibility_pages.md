---
title: "Accessibility statement pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Inform users about the accessibility conformance."
---

Inform users about the accessibility conformance.

## When to use this pattern
Use an accessibility statement page to inform users about the accessibility conformance of the service.

## Why use this pattern
The accessibility statement is required by national law. It also shows our users that we care about accessibility and about them. 

## How it works

To implement an accessibility statement:

1. Create an accessibility statement page that’s specific to the service or website  
2. Add a link in the [footer](../../components/footer/) of all pages of your service or website, so users can access it anytime. Use the following content for the link: 
	- in Greek: “Προσβασιμότητα” 
	- in English: “Accessibility”

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not link to the accessibility statement of the gov.cy portal for your service or website. 
		</p>
    </div>
</div>

### Understand the accessibility standard  
Your services and websites must achieve compliance with the European Standard EN 301 549 which adopts W3C's [Web Content Accessibility Guidelines (WCAG) 2.1 level AA](https://www.w3.org/TR/WCAG21/){rel="noreferrer noopener" target="_blank"}. 

The guidance is based on 4 design principles: 
- perceivable 
- operable 
- understandable 
- robust

Think about the different ways users interact with content and consider them during designing and implementing your service or website. Teams should keep in mind that users may: 
- use a keyboard instead of a mouse 
- change browser settings to make content easier to read 
- rely on screen readers to ‘read’ (speak) content out loud 
- use screen magnifiers to enlarge parts of the screen 
- navigate using voice commands 

### Test your service or site for accessibility 

Use a combination of automated tools and manual tests to identify potential issues, such as: 
- reporting tools 
- automated testing 
- manual testing 
- user research 

#### Reporting tools 

There are several reporting tools available for accessibility testing, including: 
- [WAVE](https://wave.webaim.org/){rel="noreferrer noopener" target="_blank"} 
- [Axe DevTools](https://www.deque.com/axe/devtools/){rel="noreferrer noopener" target="_blank"} 

#### Automated testing 
Automated testing can be integrated into your development and delivery workflows using different tools, such as DSF's [govcy-frontend-tester](https://www.npmjs.com/package/@gov-cy/govcy-frontend-tester){rel="noreferrer noopener" target="_blank"}, which uses [pa11y](https://pa11y.org/){rel="noreferrer noopener" target="_blank"} for accessibility testing.   

#### Manual testing
Manual testing is essential because tools alone can't fully ensure accessibility. Manual testing involves: 
- testing for keyboard navigation (using arrow keys, tab, enter, space) 
- testing with a screen reader. You should at least test with [NVDA (windows)](https://www.nvaccess.org/download/){rel="noreferrer noopener" target="_blank"} and [VoiceOver (macOS)](https://support.apple.com/guide/voiceover/welcome/mac){rel="noreferrer noopener" target="_blank"}. Other screen readers you could use are:
	- JAWS 
	- ZoomText/Fusion 
	- VoiceOver (iOS) 
	- TalkBack (Android) 
	- Orca (Linux) 
	- Narrator (Windows) 
- testing voice command, for example macOS voice controls 
- testing zoom functions and magnifiers, for example Windows magnifier 
- testing contrast themes, for example Windows high contrast mode.

#### User research
User research is crucial because the experience of real users who rely on assistive technology, cannot be replicated through other testing methods.  

Collaborate with organisations like [KYSOA](https://www.kysoa.org.cy/){rel="noreferrer noopener" target="_blank"} (Κυπριακή Συνομοσπονδία Οργανώσεων Αναπήρων - ΚΥΣΟΑ) and the [Pancyprian Organization of the Blind](https://pot.org.cy/){rel="noreferrer noopener" target="_blank"} (Παγκύπρια Οργάνωση Τυφλών - ΠΟΤ) to test your service or website with actual users.  

### Writing your accessibility statement page 

Write the accessibility statements in plain language, just like any other content. Explain, clearly and concisely:
- **Compliance status**: State one of the following: 
	- The service or website is fully conformant with WCAG 2.1 level AA. 
	- The service or website is partially compliant with WCAG 2.1 level AA, due to the [the non-compliance(s)] [and/or] [the exemptions] listed below.  
	- The service [or website] is not compliant with WCAG 2.1 level AA. The [the non-compliance(s)] [and/or] [the exemptions] are listed below.  
- **Non-accessible content**: This section can be removed if not applicable. List the non-accessible content and the reason for that, such as: 
	- non-compliance with [national legislation] 
	- disproportionate burden 
	- the content is not within the scope of the applicable legislation 
- **Assessment approach**: Indicate the methods used to assess accessibility
- **Compatibility with browsers**: State the browser compatibility of your service or site 
- **Limitations and alternatives**: State any limitations such as the need to use JavaScript, or areas that could be improved. 
- **Feedback and complaints**: Provide contact information for feedback and outline the enforcement procedure to be followed in these cases. 
- **Dates**: Indicate the date the statement was prepared and if applicable the date when it was last reviewed

Also make sure to: 
- include a go back link 
- make the page available in all service / site languages  

Do not use breadcrumbs or red text to warn people. 

Each accessibility statement should be tailored to the specific service or website, so it’s important not to copy from others. 

You can use an accessibility statement generator such as [w3c’s tool](https://www.w3.org/WAI/planning/statements/generator/#create){rel="noreferrer noopener" target="_blank"}, to guide you. 


<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not copy the examples on this page without amending the specifics. Make sure to adjust your accessibility statement page according to your case.  
		</p>
    </div>
</div>

#### Examples

*Example in English*
[Open in new tab](../../samples/accessibility-en/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/accessibility-en/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>


*Example in Greek*
[Open in new tab](../../samples/accessibility-el/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../samples/accessibility-el/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>
