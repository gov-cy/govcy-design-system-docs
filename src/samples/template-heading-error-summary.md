---
title: "Template - Page with an error"
date: 2022-02-01 00:00:01Z
layout : "base_for_samples.njk"
---
<!--beforeMain-->
<section class="govcy-container" id="beforeMainContainer">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
<main class="govcy-container" id="mainContainer">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
                <h2 id="errorSummary" >There is a problem</h2>
                <p class="govcy-mb-0">
                    <a href="#in-tel">Enter a valid telephone number</a>
                </p>
            </div>
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control govcy-form-control-error">
                    <h1><label class="govcy-label govcy-label-primary" for="in-tel">What is your telephone number?</label></h1>
                    <p id="in-error" class="govcy-input-error-msg">
                        <span class="govcy-visually-hidden-error">Error:</span>Enter a valid telephone number
                    </p>
                    <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="in-tel" name="in-tel" type="tel" spellcheck="false" aria-describedby="in-error" autocomplete="tel">
                </div>
                <button type="button" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>