---
title: "Typography"
date: 2022-02-01 00:00:06Z
searchKeys: "fonts text Paragraph Headings Unordered Ordered list Links"
--- 

## Base fonts 
Unless otherwise stated, use the following font properties for the default body fonts. 

|Propery     |Value       |
|------------|------------|
|font-family | Roboto     |
|font-size   | 18px       |
|font-weight | normal     |
|color       | [body](../colour/)|

{.govcy-table}

## Responsive text
The Design System uses the  [Responsive Font Size (RFS)](https://github.com/twbs/rfs/) engine to resize font sizes. The engine generates CSS that automatically calculates the appropriate values for your font sizes based on the dimensions of the browser viewport. Use the Design System’s CSS for [paragraphs](#paragraph) and [headings](#headings) CSS.

## Paragraph
To be used for paragraph text. Use the default fonts described above.

## Headings
To be used for headings h1, h2, h3, h4, h5 and h6. Use the default fonts described above with the following differences. 

- Font-Weight: **500**;
- Font-Size: The size is calculated in relation to the [base font](#base-fonts) size as described in the table below. 

|Heading |Size                     |
|--------|-------------------------|
|h1      | $font-size-base * 2.5;  |
|h2      | $font-size-base * 2;    |
|h3      | $font-size-base * 1.75; |
|h4      | $font-size-base * 1.5;  |
|h5      | $font-size-base * 1.25; |
|h6      | $font-size-base         |

{.govcy-table}

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>  
<h6>Heading 6</h6>
</div>

*Sample HTML Code*
```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

## Unordered list <ul>
To be used for unordered vertical lists (i.e. bullet points). 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<ul>
    <li>one</li>
    <li>two</li>
</ul>
</div>

*Sample HTML Code*
```html
<ul>
    <li>one</li>
    <li>two</li>
</ul>
```

## Ordered list <ol>
To be used for ordered vertical lists. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<ol>
    <li>one</li>
    <li>two</li>
</ol>
</div>

*Sample HTML Code*
```html
<ol>
    <li>one</li>
    <li>two</li>
</ol>
```

## Links

Unless otherwise stated, use the following properties for the links style. 

|Property               |Value                     |
|-----------------------|--------------------------|
|**Default state**      |                          |
|color                  |[link standard](../colour/#link-colours)|
|text-decoration        |underline|
|**Hover state**      |                          |
|color                  |[link hover](../colour/#link-colours)|
|text-decoration        |underline|
|**Visited state**      |                          |
|color                  |[link visited](../colour/#link-colours)|
|text-decoration        |underline|
|**Active state**      |                          |
|color                  |[link active](../colour/#link-colours)|
|text-decoration        |underline|

{.govcy-table-borderless}

## Opening links in a new tab
Avoid opening links in a new tab or window. It can be disorienting - and can cause accessibility problems for people who cannot visually perceive that the new tab has opened.

If you need a link to open in a new tab, then include the words ‘opens in new tab’ as part of the link. 

Include `rel="noreferrer noopener"` along with `target="_blank"` to reduce the risk of [reverse tabnabbing](https://owasp.org/www-community/attacks/Reverse_Tabnabbing) as shown in the following example.

```html
<a href="#" rel="noreferrer noopener" target="_blank">some link (opens in new tab)</a>
```

Use the following best practices:
- If your link is at the end of a sentence or paragraph, make sure that the linked text does not include the full stop.
- If it’s an external link to a non-government website, make that clear in the link text. For example, read advice on writing link text from [name of organisation]’. 
- Avoid opening links in a new tab or window. It can be disorienting - and can cause accessibility problems for people who cannot visually perceive that the new tab has opened.
