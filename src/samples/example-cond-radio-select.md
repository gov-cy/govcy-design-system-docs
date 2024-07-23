---
title: "Template - Heading with title and other headings"
date: 2022-02-01 00:00:01Z
layout : "base_for_samples.njk"
---
<!--beforeMain-->
<section class="govcy-container" id="beforeMainContainer">
</section>
 <!--main-->
<main class="govcy-container" id="mainContainer">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <h1>Departments / Directorates</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris tempor turpis ac lorem venenatis cursus. Phasellus pellentesque rhoncus ligula et blandit. Phasellus id metus nulla. Nunc maximus mi ligula, vel vestibulum justo rutrum nec. Vestibulum gravida tellus lacus, elementum ornare arcu rutrum nec. Maecenas nec eros sapien. Fusce malesuada mattis purus, at euismod lectus gravida vitae. Nullam diam leo, pharetra suscipit purus eu, commodo tincidunt metus. Phasellus eget nisi sapien. Ut efficitur nunc sit amet lacus sagittis, et hendrerit quam porttitor. In eu imperdiet quam. Donec at ornare quam, ac ultrices sem. Mauris rhoncus porta mauris at pretium. Aliquam tempus pulvinar felis non posuere. Aliquam eget tristique sem.</p>
            <h2>Radio</h2>
            <form action="" class="govcy-form" novalidate="">
                <fieldset class="govcy-fieldset">
                    <legend class="govcy-legend">What contact details should we use?</legend>
                    <div class="govcy-form-control">
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" id="option6-simple-email" name="collapseGroupSimple" type="radio" value="existingContactDetails" />
                            <label class="govcy-label" for="option6-simple-email">Use existing contact details</label>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" name="collapseGroupSimple" type="radio" id="option6-simple-emailDif" value="emailDif" data-aria-controls="email-simple-different"/>
                            <label class="govcy-label" for="option6-simple-emailDif">
                                <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                                Use different email address
                            </label>
                        </div>
                        <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-simple-different">
                            <div class="govcy-form-control">
                                <label class="govcy-label govcy-label-primary" for="sort2">Sort by</label>
                                <select class="govcy-select" id="sort2" name="sort2">
                                    <option value="" selected>None</option>
                                    <option value="published">Recently published</option>
                                    <option value="updated">Recently updated</option>
                                    <option value="views">Most views</option>
                                    <option value="comments">Most comments</option>
                                </select>
                            </div>
                        </div>
                    </div>
                </fieldset>
            </form>
        </article>
    </div>
</main>