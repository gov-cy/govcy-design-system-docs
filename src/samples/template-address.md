---
title: "Template - Page asking for address"
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
            <form class="govcy-form" novalidate action="">
                <fieldset class="govcy-fieldset">
                    <legend class="govcy-legend"><h1>What is your address?</h1></legend>
                    <div class="govcy-form-control">
                        <label class="govcy-label govcy-label-primary" for="cyManualAddressLine1">Address line 1</label>
                        <input id="cyManualAddressLine1" name="cyManualAddressLine1" type="text" class="govcy-text-input" autocomplete="address-line1"> 
                    </div>
                    <div class="govcy-form-control">
                        <label class="govcy-label govcy-label-primary" for="cyManualAddressLine2">Address line 2 (optional)</label>
                            <input id="cyManualAddressLine2" name="cyManualAddressLine2" type="text" class="govcy-text-input" autocomplete="address-line2">  
                    </div>
                    <div class="govcy-form-control">
                        <label class="govcy-label govcy-label-primary" for="cyManualTownOrCity">Town or city</label>
                            <input id="cyManualTownOrCity" name="cyManualTownOrCity" type="text" class="govcy-text-input" autocomplete="address-level2">
                    </div>
                    <div class="govcy-form-control">
                        <label class="govcy-label govcy-label-primary" for="cyManualPostalCode">Postcode</label>
                        <input id="cyManualPostalCode" name="cyManualPostalCode" type="text" class="govcy-text-input govcy-text-input-char_4 " autocomplete="postal-code">
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>