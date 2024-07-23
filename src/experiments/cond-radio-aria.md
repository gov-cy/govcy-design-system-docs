---
title: "Conditional Radio - ARIA"
date: 2022-02-01 00:00:01Z
layout : "base_for_samples.njk"
locale: "en"
---
 <!--main-->
 <main class="govcy-container" id="mainContainer">
    <div class="govcy-row">
        <article class="govcy-col-8">

<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-email" name="collapseGroupSimple" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupSimple" type="radio" id="option6-simple-emailDif" value="emailDif"
                aria-expanded="true" data-aria-controls="email-simple-different"/>
                <label class="govcy-label" for="option6-simple-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-simple-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple">Email Address</label>
                    <span id="in4-simple-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple" type="text" class="govcy-text-input" aria-describedby="in4-simple-hint"/>
                </div>
            </div>
        </div>
    </fieldset>
</form>

</article>
</div>
</main>