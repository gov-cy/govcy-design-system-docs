---
title: "Images"
date: 2022-02-01 00:00:04Z
description: "Understand the presentation of different imagery such as the aspect ratio, how the images scale, and how to write alternative text."
--- 

Avoid unnecessary decoration. Only use images if there is a real user need.  

All images should be 960 pixels wide by 640 pixels high at 72 dpi.  

You can resize images using free software like GIMP or an online photo editor like PIXLR.
## Aspect Ratio

The aspect ratio for photographs should be 3:2.  

Typically a 3:2 aspect ratio is 960×640 pixels, but scales accordingly for each breakpoint.

### Photography
![Representation of the 3:2 ratio]({{ '/img/v3_images_aspect_ratio.png' | url }})

### Scaling
Scale the browser’s window to see the different breakpoints and image scalings.

| Screen size          | Image Size |
| -------------------- | ---------- |
| **XXL** (1440+)      | 960 x 640  |
| **XL** (1200-1439px) | 840 x 560  |
| **L** (992-1199px)   | 660 x 440  |
| **M** (768-991px)    | 570 x 380  |
| **S** (577-767px)    | auto       |
| **XS** (0-576px)     | auto       |

{.govcy-table}

Using our [developers assets](../../getting-started/developer-assets), the images scaling adjusts automatically.  

*Example*
![Bike Ride]({{ '/img/v3_images_32_bike.jpg' | url }})

### Illustrations or representative imagery
If your image represents something physical, such as a letter, document or credit card you should use the aspect ratio of that item. You can do that by adding the class `govcy-img-ar-auto"` on your image.

*Example*

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h3 data-toc-exclude>Do you have a document printed in your name?</h3>
<img src="{{ '/img/v3_physical_imagery.jpg' | url }}" alt="Example of physical representation of a document" class="govcy-img-ar-auto">
</div>

*HTML code*
```html
<h3>Do you have a document printed in your name?</h3>
<img src="{{ '/img/v3_physical_imagery.jpg' | url }}" alt="Example of physical representation of a document" class="govcy-img-ar-auto">
```

## Captions

The caption field is optional. You can use a caption to:
- label a graph, infographic or diagram
- name a person in a photo
- attribute an image

If you add a caption, you should also add alt text. A caption with no alt text is poor for screen reader users because:
- some assistive technology does not read captions if the alt text field is empty, which means users miss the information
- some assistive technology always reads captions, but if the alt text field is empty the user may not be aware that the caption relates to an image

Do not use the caption field to describe the image or duplicate content in the body text.

If you do not need a caption, do not use one.
## Alt Text
Alternative text, or alt text, is read out by screen readers or displayed if an image does not load or if images have been switched off.  

All images, except decorative images, must have alt text that:
- tells people what information the image provides
- describes the content and function of the image
- is specific, meaningful and concise

Use normal punctuation, like commas and full stops, so the text is easy to read and understand.  

Do not:
- include the name of the photographer or person who created the image
- start with ‘Image of’, ‘Graphic of’ or ‘Photo of’
- repeat information from the page
- include extra information not in the image

*Example*
![Max the brown dog, sitting at a natures trail road, looking patiently at his owner.]({{ '/img/v3_dog.png' | url }})

*HTML code*
```html
<img src="/assets/images/max-the-dog.jpg" alt="Max the brown dog, sitting at a natures trail road, looking patiently at his owner.">
```

Some images do not need descriptions. Use `alt=""` if the image is:
- decorative and does not include important content
- an icon that has a text label that the alt text would repeat
- used in a link and the image is not needed to understand the link

Use the Web Accessibility initiative alt decision tree to work out if the image needs alt text.

## Images that contain text
Avoid images that contain text, especially PNGs and JPGs because the text becomes unreadable when the user zooms in. If the image does contain text, use SVG because it remains readable when the user zooms in. The alt text should be the same as the text displayed in the image.

## Accessibility
Make sure you follow the instructions: 
- on use of [alt](#alt-text)
- on use of [images that contain text](#images-that-contain-text)