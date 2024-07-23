---
title: "Typography"
date: 2022-02-01 00:00:06Z
searchKeys: "fonts text Paragraph Headings Unordered Ordered list Links"
description: "The typography provides a consistent set of typography styles for all gov.cy content."
--- 

## Base fonts
Unless otherwise stated, use the following font properties for the default body fonts.

| Key | Value  |
| ---- | ---- |
| **font-family** | `Roboto` |
| **font-size** | `16px` |
| **font-weight** | `normal` |
| **color** | `#272525` ([body colour](../colour/#text)) |
| **Line height** | `24px` |
| **Letter spacing** | `0px` |

{.govcy-table}

## Font Sizes

### Headings

Use headings consistently to create a clear hierarchy throughout your content, and to allow people using assistive technology to quickly scan and move through the page.

Mark up headings semantically using the appropriate `<h#>` level HTML element.

Write all headings in sentence case, with the exception of proper nouns, which require initial capitals.

Use only one `H1` at the top of each page or service, followed by the most commonly used `H2` heading for titles, followed by `H3` and `H4` for less important headings and titles of the page. Use `H3` and `H4` accordingly to enhance visual hierarchy.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>H1 This is a H1 title</h1>
<h2>H2 This is a H2 title</h2>
<h3>H3 This is a H3 title</h3>
<h4>H4 This is a H4 title</h4>
</div>

*HTML code*
```html
<h1>H1 This is a H1 title</h1>
<h2>H2 This is a H2 title</h2>
<h3>H3 This is a H3 title</h3>
<h4>H4 This is a H4 title</h4>
```
The typography scales the font-size accordingly in different viewports as shown below:

|Breakpoint|H1|H2|H3|H4|
|---|---|---|---|---|
|XXL (1440+)|45px|34px|25px|18px|
|XL (1200-1439px)|41px|31px|23px|17px|
|L (992-1199px)|38px|29px|21px|17px|
|M (768-991px)|35px|27px|19px|16px|
|S (577-767px)|32px|25px|18px|16px|
|XS (0-576px)|29px|23px|18px|16px|

{.govcy-table}

### Default paragraph
The default paragraph uses the [base fonts](#base-fonts). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p>This is paragraph</p>
</div>

*HTML code*
```html
<p>This is paragraph</p>
```

Paragraphs do not scale, they have a consistent size throughout the breakpoints.

| Breakpoint | Paragraph font-size |
| ---- | ---- |
| All breakpoints | 16px |

{.govcy-table}

### Lead paragraph
A lead paragraph is an introductory paragraph that you can use at the top of a page to summarise the content.  

Lead paragraphs should only be used in content pages and only once per page if needed.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p class="govcy-lead">This is lead paragraph</p>
</div>

*HTML code*
```html
<p class="govcy-lead">This is lead paragraph</p>
```

Lead paragraphs do not scale, they have a consistent size throughout the breakpoints.

| Breakpoint | Lead Paragraph font-size |
| ---- | ---- |
| All breakpoints | 20px |

{.govcy-table}

## Font weights

You can add a font weight override class to any other typographic class or element to change the font weight to light, regular, bold or semibold weight.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p class="govcy-fw-300">Light Font Weight: 300</p>
<p class="govcy-fw-400">Default/Regular Font Weight: 400</p>
<p class="govcy-fw-500">Semibold Font Weight: 500</p>
<p class="govcy-fw-700">Bold Font Weight: 700</p>
</div>

*HTML code*
```html
<p class="govcy-fw-300">Light Font Weight: 300</p>
<p class="govcy-fw-400">Default/Regular Font Weight: 400</p>
<p class="govcy-fw-500">Semibold Font Weight: 500</p>
<p class="govcy-fw-700">Bold Font Weight: 700</p>
```
### When to use Light
Use light text to create contrast between clustered sections to make the text readable.  

Do not use light text with light colours or light background.  

Do not use light text on small body text sizes.
### When to use Semibold
You can use bold to emphasise particular words, to highlight critical information that users need to refer to or when evidence shows the users have missed important information within a paragraph.  

For example, “Your reference number is <span class="govcy-fw-500">ABC12345678</span>. Use this to track your application. Updates will be sent to name@example.com“  

Do not overuse semibold text.
### When to use Bold
The bold weight is used for main headers `h1` and `h2`.

## Links
Links apply the [link colours](../colour/#links) and are underlined by default. 

If your link is at the end of a sentence or paragraph, make sure that the linked text does not include the full stop.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p>Jump to the <a href="#">Top of the page</a></p>
</div>

*HTML code*
```html
<p>Jump to the <a href="#">Top of the page</a></p>
```
### Links with no visited state
Use the `govcy-link-no-visited-state` modifier class where it is not helpful to distinguish between visited and unvisited states, for example when linking to pages with frequently changing content such as the dashboard for an admin interface.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p>Jump to the <a href="#" class="govcy-link-no-visited-state">Top of the page</a></p>
</div>

*HTML code*
```html
<p>Jump to the <a href="#" class="govcy-link-no-visited-state">Top of the page</a></p>
```

### Opening links in a new tab
Avoid opening links in a new tab or window. It can be disorienting - and can cause accessibility problems for people who cannot visually perceive that the new tab has opened.

If you need a link to open in a new tab, then include the words ‘opens in new tab’ as part of the link.

Include `rel="noreferrer noopener"` along with `target="_blank"` to reduce the risk of [reverse tabnabbing (opens in new tab)](https://owasp.org/www-community/attacks/Reverse_Tabnabbing){rel="noreferrer noopener" target="_blank"} as shown in the following example.

```html
<a href="#" rel="noreferrer noopener" target="_blank">some link (opens in new tab)</a>
```
### External Links
If it’s an external link to a non-government website, make that clear in the link text. For example, ‘read advice on writing link text from \[name of organisation\]’. There’s no need to say explicitly that you’re linking to an external site.

### Links on dark backgrounds
If you are implementing custom design elements, use the `govcy-link-inverse` modifier class to show white links on dark backgrounds. 

Make sure all users can see the links. The white links and background colour must have a contrast ratio of at least 4.5:1.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p class="govcy-p-4 govcy-bg-primary">
	<a href="#" class="govcy-link-inverse">Jump to the Top of the page</a>
</p>
</div>

*HTML code*
```html
<p class="govcy-p-4 govcy-bg-primary">
	<a href="#" class="govcy-link-inverse">Jump to the Top of the page</a>
</p>
```
### Links without underlines
Use the `govcy-link-no-underline` modifier class to remove underlines from links.

Only do this if the context tells the user that the text is a link, even without the underline.

For example, links in a header or side navigation might not need underlines. Users will understand that they are links because of where they are, at the same place, across different pages.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p>Jump to the <a href="#" class="govcy-link-no-underline">Top of the page</a></p>
</div>

*HTML code*
```html
<p>Jump to the <a href="#" class="govcy-link-no-underline">Top of the page</a></p>
```

### Linking to an element on the same page
Use the hash (`#`) character and the id of an element in the `href` attribute, to link to an element on the same page. This is helpful when linking [error summary](../../components/error_summary/) messages to the field where the user can make a correction. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p><a href="#Section_further_down">Jump to the heading below</a></p>

<h2 data-toc-exclude id="Section_further_down">Section further down</h2>
</div>

*HTML code*
```html
<p><a href="#Section_further_down">Jump to the heading below</a></p>

<h2 id="Section_further_down">Section further down</h2>
```

## Lists
Use lists to make blocks of text easier to read, and to break information into manageable chunks.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<ul class="govcy-list-unstyled">
    <li><a href="#">Benefits calculators</a></li>
    <li><a href="#">Benefit overpayments</a></li>
    <li><a href="#">Benefits calculators</a></li>
    <li><a href="#">More</a></li>
</ul>
</div>

*HTML code*
```html
<ul class="govcy-list-unstyled">
    <li><a href="#">Benefits calculators</a></li>
    <li><a href="#">Benefit overpayments</a></li>
    <li><a href="#">Benefits calculators</a></li>
    <li><a href="#">More</a></li>
</ul>
```
### Bulleted lists
Introduce bulleted lists with a lead-in line ending in a colon. Start each item with a lowercase letter, and do not use a full stop at the end.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<p>You can buy:</p>
<ul>
    <li>apples</li>
    <li>oranges</li>
    <li>pears</li>
</ul>
</div>

*HTML code*
```html
<p>You can buy:</p>
<ul>
    <li>apples</li>
    <li>oranges</li>
    <li>pears</li>
</ul>
```

If needed you can use indentation.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<ul>
	<li>Soda</li>
	<li>Coffee</li>
	<li>Tea:
		<ul>
			<li>Black tea</li>
			<li>Green tea</li>
			<li>Hibiscus tea</li>
		</ul>
	</li>
	<li>Milk</li>
</ul>
</div>

*HTML code*
```html
<ul>
	<li>Soda</li>
	<li>Coffee</li>
	<li>Tea:
		<ul>
			<li>Black tea</li>
			<li>Green tea</li>
			<li>Hibiscus tea</li>
		</ul>
	</li>
	<li>Milk</li>
</ul>
```
### Numbered lists
Use numbered lists instead of bulleted lists when the order of the items is relevant.

You do not need to use a lead-in line for numbered lists. Items in a numbered list should end in a full stop because each should be a complete sentence.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<ol>
    <li>Delivery address</li>
    <li>Payment</li>
    <li>Confirmation</li>
</ol>
</div>

*HTML code*
```html
<ol>
    <li>Delivery address</li>
    <li>Payment</li>
    <li>Confirmation</li>
</ol>
```

If needed you can use indentation.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<ol>
    <li>Water</li>
    <li>Bread</li>
    <li>Salad:
        <ol>
            <li>Lettuce</li>
            <li>Egg</li>
            <li>Tomato</li>
        </ol>
    </li>
    <li>Apple</li>
</ol>
</div>

*HTML code*
```html
<ol>
    <li>Water</li>
    <li>Bread</li>
    <li>Salad:
        <ol>
            <li>Lettuce</li>
            <li>Egg</li>
            <li>Tomato</li>
        </ol>
    </li>
    <li>Apple</li>
</ol>
```
## Lines
You can use the `govcy-line` classes on an `<hr>` element to create a line between sections of content.
### Default line
The default line has applied `20px` padding top and `20px` margin bottom.

Do not overuse lines. Be default the design system is designed for users to distinguish between sections on a page without having to use lines.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<hr class="govcy-line">
</div>

*HTML code*
```html
<hr class="govcy-line">
```
### No bottom line
The alternative line has applied `20px` padding top and `0px` margin bottom, and must only be used when adding a line above a heading element `h1`,`h2`,`h3`,`h4`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<hr class="govcy-line-no-bottom">
</div>

*HTML code*
```html
<hr class="govcy-line-no-bottom">
```
## Typography with gov.cy CSS
Using our [developers assets](../../getting-started/developer-assets) and the code in our documentation, typography adjust automatically. 

## Accessibility
If you need to include content in a different language that the defined [lang attribute](../../getting-started/page-template/#html5-doctype-and-lang) of your page, make sure you define the correct `lang` in your element. For example:

```html
<p>Dear <span lang="el">Όμομα Επώνυμο</span>"</p>
```

Also make sure:
- to have a color contrast ration of at least 4.5:1 if your implementing a custom component
- to implement the [focus state](../../patterns/focus_state/) on interactive text such as links