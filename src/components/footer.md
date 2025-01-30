---
"title" : "Footer"
date: 2022-02-01 00:01:01Z
description: "Use the footer to provide copyright information and links for privacy statements, cookie policy and accessibility statements"
---

The footer provides copyright information and links for privacy statements, cookie policy and accessibility statements.

## When to use this component
Use the footer at the bottom of every page of your service or website.

## How it works
The footer component should only exist in the [footer section](../../getting-started/page-template/#sections).

Add a copyright notice to the footer to clarify who owns the copyright. For gov.cy services, add the coat of arms to keep things consistent with the rest of gov.cy.  

Users can navigate within the footer links also by using the keyboard.

See below the different variants of the footer component. Make sure to change the links `href` according to your implementation. The gov.cy logo link should lead to `https://gov.cy` for the Greek version of the site and `https://www.gov.cy/en/` for the English version.

Use the `govcy-d-print-none` to hide the footer on print media.  

### Default footer
The default footer has links for copyright notice, gov.cy logo and links for:
- [privacy statement](../../patterns/privacy_policy_page/)
- [cookie policy](../../patterns/cookies_pages/)
- [accessibility statements](../../patterns/accessibility_pages/)

Also when applicable you may add 
- the help us improve this service (feedback) link
- the "Funded by the European Union" and "Cyprus to tomorrow" logos

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility</a></li>
                    <li><a href="#">Help us improve this service</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
</div>

*HTML code*
```html
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility</a></li>
                    <li><a href="#">Help us improve this service</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
```
### EU Funded sites and services
For EU funded sites and services, also display the "Funded by the European Union" and "Cyprus to tomorrow" logos. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility</a></li>
                    <li><a href="#">Help us improve this service</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                    <a href="https://europa.eu/" title="Go to EU website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/FundedbyEU_NextGeneration_H53-EN.png" alt="Funded by the EU Next Generation EU"></a>
                    <a href="http://www.cyprus-tomorrow.gov.cy/" title="Go to Cyprus Tomorrow website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/CYpros to aurio logo eng_H53_EN.png" alt="Cyprus tomorrow, recovery and resilience plan"></a>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
</div>

*HTML code*
```html
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Privacy statement</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Accessibility</a></li>
                    <li><a href="#">Help us improve this service</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                    <a href="https://europa.eu/" title="Go to EU website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/FundedbyEU_NextGeneration_H53-EN.png" alt="Funded by the EU Next Generation EU"></a>
                    <a href="http://www.cyprus-tomorrow.gov.cy/" title="Go to Cyprus Tomorrow website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/CYpros to aurio logo eng_H53_EN.png" alt="Cyprus tomorrow, recovery and resilience plan"></a>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
```
### Greek variant
In Greek use the following variant. Make sure the use the correct text at the `alt` and `title` attributes.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Δήλωση απορρήτου</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Προσβασιμότητα</a></li>
                    <li><a href="#">Βοηθήστε μας να βελτιώσουμε αυτή την υπηρεσία</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Κυπριακή Δημοκρατία, 2023</span>
                    <a href="https://europa.eu/" title="Μετάβαση στην ιστοσελίδα της ΕΕ" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/FundedbyEU_NextGeneration_H53-EL.png" alt="Χρηματοδοτείται από την ΕΕ Next Generation EU"></a>
                    <a href="http://www.cyprus-tomorrow.gov.cy/" title="Μετάβαση στην ιστοσελίδα Κύπρος το Αύριο" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/CYpros to aurio logo eng_H53_EL.png" alt="Κύπρος το Αύριο, σχέδιο ανάκαμψης και ανθεντικότητας"></a>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Μετάβαση στην αρχική σελίδα του gov.cy"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
</div>

*HTML code*
```html
<footer class="govcy-footer govcy-d-print-none">
    <div class="govcy-container">
        <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
            <div class="govcy-my-4">
                <ul>
                    <li><a href="#">Δήλωση απορρήτου</a></li>
                    <li><a href="#">Cookies</a></li>
                    <li><a href="#">Προσβασιμότητα</a></li>
                    <li><a href="#">Βοηθήστε μας να βελτιώσουμε αυτή την υπηρεσία</a></li>
                </ul>
                <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                    <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                    <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Κυπριακή Δημοκρατία, 2023</span>
                    <a href="https://europa.eu/" title="Μετάβαση στην ιστοσελίδα της ΕΕ" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/FundedbyEU_NextGeneration_H53-EL.png" alt="Χρηματοδοτείται από την ΕΕ Next Generation EU"></a>
                    <a href="http://www.cyprus-tomorrow.gov.cy/" title="Μετάβαση στην ιστοσελίδα Κύπρος το Αύριο" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/CYpros to aurio logo eng_H53_EL.png" alt="Κύπρος το Αύριο, σχέδιο ανάκαμψης και ανθεντικότητας"></a>
                </div>
            </div>
            <div class="govcy-my-4">
                <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Μετάβαση στην αρχική σελίδα του gov.cy"><img alt="gov.cy Logo"/></a>
            </div>
        </div>
    </div>
</footer>
```
### Adding Secondary navigation
Only add secondary navigation if you’re creating a gov.cy service, and you want users to be able to navigate away from the service to somewhere else on the website. For example, you probably don’t want to encourage a user to navigate away from a linear, form-type service.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<footer class="govcy-footer govcy-d-print-none"> 
    <div class="govcy-px-4">
        <div class="govcy-container">
            <div class="govcy-row">
                <div class="govcy-col-md-8 govcy-footer-column">
                    <h3>Two column list</h3>
                    <div class="govcy-row">
                        <div class="govcy-col-md-6">
                            <ul>
                                <li><a href="#">Navigation Item 1</a></li>
                                <li><a href="#">Navigation Item 2</a></li>
                                <li><a href="#">Navigation Item 3</a></li>
                            </ul>
                        </div>
                        <div class="govcy-col-md-6">
                            <ul>
                                <li><a href="#">Navigation Item 4</a></li>
                                <li><a href="#">Navigation Item 5</a></li>
                                <li><a href="#">Navigation Item 6</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="govcy-col-md-4 govcy-footer-column">
                    <h3>One column list</h3>
                    <ul>
                        <li><a href="#">Navigation Item 1</a></li>
                        <li><a href="#">Navigation Item 2</a></li>
                        <li><a href="#">Navigation Item 3</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="govcy-container govcy-footer-separator">
            <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
                <div class="govcy-my-4">
                    <ul>
                        <li><a href="#">Privacy statement</a></li>
                        <li><a href="#">Cookies</a></li>
                        <li><a href="#">Accessibility</a></li>
                        <li><a href="#">Help us improve this service</a></li>
                    </ul>
                    <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                        <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                        <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                        <a href="https://europa.eu/" title="Go to EU website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/FundedbyEU_NextGeneration_H53-EN.png" alt="Funded by the EU Next Generation EU"></a>
                        <a href="http://www.cyprus-tomorrow.gov.cy/" title="Go to Cyprus Tomorrow website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" style="aspect-ratio: auto;" src="../../img/CYpros to aurio logo eng_H53_EN.png" alt="Cyprus tomorrow, recovery and resilience plan"></a>
                    </div>
                </div>
                <div class="govcy-my-4">
                    <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
                </div>
            </div>
        </div>
    </div>
</footer>
</div>

*HTML code*
```html
<footer class="govcy-footer govcy-d-print-none"> 
    <div class="govcy-px-4">
        <div class="govcy-container">
            <div class="govcy-row">
                <div class="govcy-col-md-8 govcy-footer-column">
                    <h3>Two column list</h3>
                    <div class="govcy-row">
                        <div class="govcy-col-md-6">
                            <ul>
                                <li><a href="#">Navigation Item 1</a></li>
                                <li><a href="#">Navigation Item 2</a></li>
                                <li><a href="#">Navigation Item 3</a></li>
                            </ul>
                        </div>
                        <div class="govcy-col-md-6">
                            <ul>
                                <li><a href="#">Navigation Item 4</a></li>
                                <li><a href="#">Navigation Item 5</a></li>
                                <li><a href="#">Navigation Item 6</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="govcy-col-md-4 govcy-footer-column">
                    <h3>One column list</h3>
                    <ul>
                        <li><a href="#">Navigation Item 1</a></li>
                        <li><a href="#">Navigation Item 2</a></li>
                        <li><a href="#">Navigation Item 3</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="govcy-container govcy-footer-separator">
            <div class="govcy-d-flex govcy-justify-content-between govcy-align-items-end govcy-flex-wrap">
                <div class="govcy-my-4">
                    <ul>
                        <li><a href="#">Privacy statement</a></li>
                        <li><a href="#">Cookies</a></li>
                        <li><a href="#">Accessibility</a></li>
                        <li><a href="#">Help us improve this service</a></li>
                    </ul>
                    <div class="govcy-d-flex govcy-align-items-center govcy-flex-wrap">
                        <span class="govcy-fs-2 govcy-fw-bold govcy-mr-6">gov.cy</span>
                        <span class="govcy-mr-6 govcy-mt-2 govcy-mb-2">&copy; Republic of Cyprus, 2023</span>
                        <a href="https://europa.eu/" title="Go to EU website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/FundedbyEU_NextGeneration_H53-EN.png" alt="Funded by the EU Next Generation EU"></a>
                        <a href="http://www.cyprus-tomorrow.gov.cy/" title="Go to Cyprus Tomorrow website" target="_blank"><img class="govcy-eu-logo govcy-mb-2" src="../../img/CYpros to aurio logo eng_H53_EN.png" alt="Cyprus tomorrow, recovery and resilience plan"></a>
                    </div>
                </div>
                <div class="govcy-my-4">
                    <a href="https://www.gov.cy/en/" class="govcy-footer-logo" title="Go to the gov.cy homepage"><img alt="gov.cy Logo"/></a>
                </div>
            </div>
        </div>
    </div>
</footer>
```

## Accessibility

Make sure
- you use the alt and title tags as shown in the examples
- not to make footer elements ‘sticky’ to the bottom of the page by using `position: fixed` or any other method 