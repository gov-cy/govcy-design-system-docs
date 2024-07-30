---
title: "Accessibility bad example with radio and no legend"
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
                    <fieldset class="govcy-fieldset">
                        <h1>Do you wish to continue?</h1>
                        <div class="govcy-form-control">
                            <div class="govcy-radio">
                                <input class="govcy-radio-input" type="radio" name="option3" id="option3-yes">
                                <label class="govcy-label" for="option3-yes">Yes</label>
                            </div>
                            <div class="govcy-radio">
                                <input class="govcy-radio-input" type="radio" name="option3" id="option3-no">
                                <label class="govcy-label" for="option3-no">No</label>
                            </div>
                        </div>
                    </fieldset>
                <button type="button" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>