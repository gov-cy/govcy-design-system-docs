---
title: "Template - Page with radios question"
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
                <fieldset class="govcy-fieldset" aria-describedby="option4-fildset-hint">
                    <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
                    <div class="govcy-form-control">
                        <span class="govcy-hint" id="option4-fildset-hint">Different options will appear depending on your option.</span>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-1" aria-describedby="option4-1-hint">
                            <label class="govcy-label" for="option4-1">Vaccination</label>
                            <span id="option4-1-hint" class="govcy-hint">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-2" aria-describedby="option4-2-hint">
                            <label class="govcy-label" for="option4-2">Recovery</label>
                            <span id="option4-2-hint" class="govcy-hint">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-3" aria-describedby="option4-3-hint">
                            <label class="govcy-label" for="option4-3">Laboratory testing</label>
                            <span id="option4-3-hint" class="govcy-hint">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>