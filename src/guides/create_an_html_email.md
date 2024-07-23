---
title: "How to create an HTML email"
date: 2022-02-01 00:01:03Z
description: "How to create an HTML email to be sent by your service using the styles of the gov.cy."
image: v3_custom_design_element.png
---

In this guide we will be looking at an example of an HTML email that is sent by your service, using the styles of the gov.cy, and how developers can create it.

HTML emails are tricky. Because of the vast variety of devices, email clients and email providers, it can be difficult to create an email that is consistent. 

We wanted to create an HTML email template to be used by gov.cy services that:
- uses the styles and branding of gov.cy
- follows the HTML best practices for emails (for example max-width: 600px, use of inline styling)
- minimizes the risk of being stuck in “SPAM”
- ensures that it works well with most email clients
- is responsive (work well on desktop and mobiles)
- follows accessibility guidelines
- allows multi-language content

## Example of an HTML email

After a lot of trial and error, we have come with the following example that can be used as a template to create an HTML email. 

*Example*
[Open in new tab](../../htmls/submission-email/){rel="noreferrer noopener" target="_blank"}

<iframe src="../../htmls/submission-email/" width="100%" frameborder="0" scrolling="no" class="govcy-br-1 govcy-br-standard govcy-mb-4" onload="resizeIframe(this)"></iframe>

*HTML code*
```html
<!doctype html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml" xmlns:v="urn:schemas-microsoft-com:vml"
    xmlns:o="urn:schemas-microsoft-com:office:office">
<head>
    <title>Service email</title>
    <!--[if !mso]><!-->
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <!--<![endif]-->
    <!--[if (gte mso 9)|(IE)]>
        <style>
        li {
        margin-left:10px !important;
        mso-special-format: bullet;
        }
        </style>
        <![endif]-->
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
    <!-- PRE HEADER TEXT -->
    <div
        style="display:none;font-size:1px;color:#ffffff;line-height:1px;max-height:0px;max-width:0px;opacity:0;overflow:hidden;">
        We have received your application.</div>
    <table border="0" cellpadding="0" cellspacing="0" width="100%">
        <tr>
            <td align="center">
                <!--[if mso]>
                    <table align="center" border="0" cellspacing="0" cellpadding="0" width="600">
                    <tr>
                    <td align="center" valign="top" width="600">
                    <![endif]-->
                <!-- HEADER -->
                <table border="0" cellpadding="0" cellspacing="0" width="100%" style="max-width: 600px;">
                    <tr>
                        <!-- IMAGE -->
                        <td align="left" valign="top"
                            style="padding: 12px 16px 0px;background:#31576f;background-color:#31576f;">
                            <img src="https://cdn.jsdelivr.net/gh/gov-cy/govdesign@main/govcylogo_v3.png" alt="gov.cy"
                                border="0" />
                        </td>
                    </tr>
                    <tr>
                        <td align="left" valign="top"
                            style="padding:0px 16px 12px;border-bottom: 4px solid #ffad2d;background:#31576f;background-color:#31576f;">
                            <!-- SERVICE NAME -->
                            <div style="font-family:Arial;font-size:18px;line-height:1.5;text-align:left; color:#ffffff;"
                                lang="el">Service name</div>
                        </td>
                    </tr>
                </table>
                <!-- SUCCESS -->
                <!-- BODY -->
                <table border="0" cellpadding="0" cellspacing="0" width="100%"
                    style="max-width: 600px; padding:10px 0;">
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">
                                First and Last name
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 0;">
                            <table border="0" cellpadding="0" cellspacing="0" width="100%"
                                style="padding:10px 0;max-width: 600px;background:#00703c;background-color:#00703c;">
                                <tr>
                                    <td align="center" valign="top" style="padding:10px 16px;">
                                        <!-- Received -->
                                        <div
                                            style="font-family:helvetica;font-size:24px;font-weight:bold;line-height:1.5;text-align:center;color:#ffffff;">
                                            We have received your application</div>
                                    </td>
                                </tr>
                                <tr>
                                    <td align="center" valign="top" style="padding:10px 16px;">
                                        <!-- details -->
                                        <div
                                            style="font-family:Arial;font-size:18px;line-height:1.5;text-align:center;color:#ffffff;">
                                            The application was submitted on 12/1/2024 your reference number is
                                            DSF123456789.</div>
                                    </td>
                                </tr>
                            </table>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;" lang="en">

                                <h1 style="font-size:28px;font-weight:700;margin: 0;">
                                    Heading 1
                                </h1>

                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">
                                If we need any other information during the review of your application, we will contact
                                you
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">

                                <h2 style="font-size:24px;font-weight:700;margin: 0;">
                                    Heading 2
                                </h2>

                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce scelerisque sapien
                                facilisis dolor congue faucibus. Interdum et malesuada fames ac ante ipsum primis in
                                faucibus. Mauris ut dolor in elit volutpat maximus. Etiam sit amet viverra ligula.
                                Vivamus ultricies, leo convallis imperdiet vehicula, diam ex commodo urna, id tempus
                                elit ex aliquam enim. Sed imperdiet erat arcu, nec scelerisque ante volutpat quis. Morbi
                                venenatis pharetra varius. Sed libero lectus, finibus eget hendrerit vitae, lacinia id
                                augue. Praesent ullamcorper congue neque, sit amet volutpat nisl aliquet et.
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">

                                <h3 style="font-size:20px;font-weight:700;margin: 0;">
                                    Heading 3
                                </h3>

                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce scelerisque sapien
                                facilisis dolor congue faucibus. Interdum et malesuada fames ac ante ipsum primis in
                                faucibus. Mauris ut dolor in elit volutpat maximus. Etiam sit amet viverra ligula.
                                Vivamus ultricies, leo convallis imperdiet vehicula, diam ex commodo urna, id tempus
                                elit ex aliquam enim. Sed imperdiet erat arcu, nec scelerisque ante volutpat quis. Morbi
                                venenatis pharetra varius. Sed libero lectus, finibus eget hendrerit vitae, lacinia id
                                augue. Praesent ullamcorper congue neque, sit amet volutpat nisl aliquet et.
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">

                                <h4 style="font-size:18px;font-weight:700;margin: 0;">
                                    Heading 4
                                </h4>

                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce scelerisque sapien
                                facilisis dolor congue faucibus. Interdum et malesuada fames ac ante ipsum primis in
                                faucibus. Mauris ut dolor in elit volutpat maximus. Etiam sit amet viverra ligula.
                                Vivamus ultricies, leo convallis imperdiet vehicula, diam ex commodo urna, id tempus
                                elit ex aliquam enim. Sed imperdiet erat arcu, nec scelerisque ante volutpat quis. Morbi
                                venenatis pharetra varius. Sed libero lectus, finibus eget hendrerit vitae, lacinia id
                                augue. Praesent ullamcorper congue neque, sit amet volutpat nisl aliquet et.
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">

                                <ol style="margin:0; margin-left: 16px; padding:0; line-height:22px;" align="left">
                                    <li>item 1</li>
                                    <li>item 2</li>
                                    <li>item 3</li>
                                </ol>

                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td align="center" valign="top" style="padding:10px 16px;">
                            <div style="font-family:Arial;font-size:16px;line-height:1.5;text-align:left;">

                                <ul style="margin:0; margin-left: 16px; padding:0; line-height:22px;" align="left"
                                    type="disc">
                                    <li>item 1</li>
                                    <li>item 2</li>
                                    <li>item 3</li>
                                </ul>

                            </div>
                        </td>
                    </tr>
                </table>
                <!-- FOOTER  -->
                <table border="0" cellpadding="0" cellspacing="0" width="100%" style="max-width: 600px;">
                    <tr>
                        <td align="center" valign="top"
                            style="padding:10px 16px 10px;border-top: 4px solid #ffad2d;background:#ebf1f3;background-color:#ebf1f3;">
                            <div
                                style="font-family:Arial; font-size: 24px;text-align:left;margin-bottom: 10px;line-height:1;">
                                <a href="https://gov.cy" style="color:#000000; text-decoration: none;font-weight: 500;">
                                    <strong
                                        style="color:#000000; text-decoration: none;font-weight: 500;">gov.cy</strong>
                                </a>
                            </div>
                            <div
                                style="font-family:Arial;font-size:16px;text-align:left;margin-bottom: 10px;line-height:1;">
                                Service name
                            </div>
                        </td>
                    </tr>
                </table>
                <!--[if mso]>
                    </td>
                    </tr>
                    </table>
                    <![endif]-->
            </td>
        </tr>
    </table>
</body>
</html>
```

## Testing the HTML email

The email template has been tested with [Mailtrap (opens in new tab)](https://mailtrap.io/){rel="noreferrer noopener" target="_blank"} to verify HTML compatibility. Here are the compatibility results we got for different email clients.

| Client     | Desktop | Mobile | Web  | 
| ------     | ------- | ------ |----- |
| **Apple mail** | 97%     |  95%   | 100% |
| **Gmail**      | 100%    |  89%   | 92%  |
| **Outlook**    | 80%     |  93%   | 94%  |
| **Yahoo Mail** | 100%    |  80%   | 80%  |
| **Other**      | 100%    |  89%   | 89%  |

{.govcy-table}

Mailtrap also provides a spam analysis scoring from 0 to 5. The higher the score, the more likely the email is a SPAM. Our email template has scored **0.1** which is considered a great score.

The template has also been tested manually with a variaty of email clients and devices and was consistent with very little diviations in older clients. 

## NPM package

We realize that it is diffuclt to be consistent when all you have is an HTML example, so we have created the [dsf-email-templates NPM package (opens in new tab)](https://www.npmjs.com/package/@gov-cy/dsf-email-templates){rel="noreferrer noopener" target="_blank"} to create HTML emails. You can find instructions on how to use it in the package's readme file.

Note that the package has been created for internal use by the DSF team, but we have made it as reusable as possible for any implementation team. However, we cannot guarantee it will work flawlessly in all cases, so please test extensively if you plan to include the package as a production dependency.

## Contribute
If you have used the NPM package, please let us have your feedback, so we can make it better for everyone. Send us an email at <a href="mailto:dsf@dits.dmrid.gov.cy" target="_blank">dsf@dits.dmrid.gov.cy</a> to get in touch. 


