---
title: "Template - Page with a question"
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
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control">
                    <h1><label class="govcy-label govcy-label-primary" for="in-tel">What is your telephone number?</label></h1>
                    <input class="govcy-text-input govcy-text-input-char_20" id="in-tel" name="in-tel" type="tel" spellcheck="false" autocomplete="tel">
                </div>
                <button type="button" class="govcy-btn-primary" onclick="window.location.href='../template-heading-error-summary/#errorSummary'">Continue</button>
            </form>
        </article>
    </div>
</main>