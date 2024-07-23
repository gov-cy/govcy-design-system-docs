---
title: "Addresses"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for an address."
---
Help users provide addresses. 

## When to use this pattern
Follow this pattern whenever you need to display or ask users for an address.

Only ask for people’s address if you need that information to deliver a service and you cannot get the information from data we already have (for example from an API call with the Civil Registry and Migration Department).  

## How it works
Follow the instructions on how to ask and display addresses.

### How to ask
Depending on the case, you might ask for local (Cypriot) or international address. 

#### Cypriot address lookup
An address lookup helps users find a full address from partial information such as a postcode.

Use an address lookup when you’re asking users for a Cypriot address.

An address lookup lets users specify a Cypriot address by entering their postcode and selecting their address from a list. There is also an option to enter a street or apartment number.

Use the following flow to ask for a Cypriot address with the address lookup: 

1. Use a [whole number numeric input ](../numeric_inputs/#whole-numbers) to ask users to enter their postcode.
2. Ask the user's to select their street based on the post code provided. You can use a [select component](../../components/select/) for this. 
3. Use [text inputs](../../components/text_input/) to ask the users to enter the street number and optionally the apartment number. Also show the users their selected 'postcode', 'street', 'city or village' and 'district', and provide them with a 'Continue' [primary button](../../components/button/#primary-button) to store the address. 

For each step of the address lookup, use a [secondary button](../../components/button/#secondary-button) labeled `Search` to allow user's to search for streets based on the provided postcode. This allows the user to search again for streets at any time of the process.

Remember to run validations for each step and follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input. 

![Flow of Cypriot address lookup](../../img/v3_cy_address_lookup.png){style="aspect-ratio: auto;"}

When using an address lookup, you should:
- make it clear that it will only work for Cypriot addresses
- provide a manual option for people with international addresses or addresses that are missing or not properly listed in the address lookup.

#### Manual address
If you use multiple text inputs, you should:

- only make individual text inputs mandatory if you really need the information
- use [text inputs the appropriate width](../../components/text_input/#fixed-width-text-inputs) for the content – it helps people understand the form, for example, make postcode text inputs shorter than street text inputs

Make sure there are enough text inputs to accommodate longer addresses if you know your users will need them. For example, allow users to include a company name or flat number.

Use the `autocomplete` attribute on each individual address field to help users enter their address more quickly. This allows you to specify each input’s purpose so browsers can autofill the information on a user’s behalf if they’ve entered it previously.

Using multiple text inputs means:
- you can easily extract and use specific parts of an address
- you can give help for individual text inputs
- you can validate each part of the address separately
- users can complete the form using their browser’s autocomplete function

The disadvantages of using multiple text inputs are that:
- it’s hard to find a single format that works for all addresses
- there’s no guarantee that users will use the text inputs the way you think they will
- users cannot easily paste addresses from their clipboards

#### Cypriot manual address
Only use Cypriot manual address when you know the addresses will come from Cyprus only and can cannot implement the [Cypriot address lookup](#cypriot-address-lookup).  

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
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
</div>
</div>

*HTML code*
```html
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
</form>
```
#### International manual address
Depending on the service, you might allow users to enter international address. Use the manual address and add a dropdown of all countries other than Cyprus.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your address?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualAddressLine1">Address line 1</label>
               <input id="intManualAddressLine1" name="intManualAddressLine1" type="text" class="govcy-text-input" autocomplete="address-line1"> 
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualAddressLine2">Address line 2 (optional)</label>
                <input id="intManualAddressLine2" name="intManualAddressLine2" type="text" class="govcy-text-input" autocomplete="address-line2">  
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualTownOrCity">Town or city</label>
                <input id="intManualTownOrCity" name="intManualTownOrCity" type="text" class="govcy-text-input" autocomplete="address-level2">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualPostalCode">Postcode</label>
            <input id="intManualPostalCode" name="intManualPostalCode" type="text" class="govcy-text-input govcy-text-input-char_20 " autocomplete="postal-code">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="country">Country</label>
            <select id="country" name="country" class="govcy-select" enterkeyhint="done" autocomplete="country">
                <option selected="selected">Select country</option>
                <option value="660">AFGHANISTAN</option>
                <option value="70">ALBANIA</option>
                <option value="208">ALGERIA</option>
                <option value="43">ANDORRA</option>
                <option value="330">ANGOLA</option>
                <option value="459">ANTIGUA AND BARBUDA</option>
                <option value="528">ARGENTINA</option>
                <option value="77">ARMENIA</option>
                <option value="800">AUSTRALIA</option>
                <option value="38">AUSTRIA</option>
                <option value="78">AZERBAIJAN</option>
                <option value="453">BAHAMAS</option>
                <option value="640">BAHRAIN</option>
                <option value="666">BANGLADESH</option>
                <option value="469">BARBADOS</option>
                <option value="73">BELARUS</option>
                <option value="2">BELGIUM</option>
                <option value="421">BELIZE</option>
                <option value="284">BENIN</option>
                <option value="675">BHUTAN</option>
                <option value="516">BOLIVIA</option>
                <option value="93">BOSNIA AND HERZEGOVINA</option>
                <option value="391">BOTSWANA</option>
                <option value="508">BRAZIL</option>
                <option value="703">BRUNEI DARUSSALAM</option>
                <option value="68">BULGARIA</option>
                <option value="236">BURKINA FASO</option>
                <option value="328">BURUNDI</option>
                <option value="696">CAMBODIA (KAMBPUCHEA)</option>
                <option value="302">CAMEROON</option>
                <option value="404">CANADA</option>
                <option value="247">CAPE VERDE</option>
                <option value="306">CENTRAL AFRICAN REPUBLIC</option>
                <option value="244">CHAD</option>
                <option value="512">CHILE</option>
                <option value="720">CHINA</option>
                <option value="480">COLOMBIA</option>
                <option value="375">COMOROS</option>
                <option value="318">CONGO</option>
                <option value="833">COOK ISLANDS</option>
                <option value="436">COSTA RICA</option>
                <option value="272">COTE DE  IVOIRE</option>
                <option value="92">CROATIA</option>
                <option value="448">CUBA</option>
                <option value="61">CZECH REPUBLIC</option>
                <option value="724">DEMOCRATIC PEOPLES REPUBLIC OF KOREA</option>
                <option value="8">DENMARK</option>
                <option value="338">DJIBOYTI</option>
                <option value="460">DOMINICA</option>
                <option value="456">DOMINICAN REPUBLIC</option>
                <option value="702">EAST TIMOR</option>
                <option value="500">ECUADOR</option>
                <option value="220">EGYPT</option>
                <option value="428">EL SALVADOR</option>
                <option value="310">EQUATORIAL GUINEA</option>
                <option value="997">ERITREA</option>
                <option value="53">ESTONIA</option>
                <option value="334">ETHIOPIA</option>
                <option value="96">F.Y.R.O.M</option>
                <option value="815">FIJI</option>
                <option value="32">FINLAND</option>
                <option value="1">FRANCE</option>
                <option value="314">GABON</option>
                <option value="252">GAMBIA</option>
                <option value="76">GEORGIA</option>
                <option value="4">GERMANY</option>
                <option value="276">GHANA</option>
                <option value="9">GREECE</option>
                <option value="473">GRENADA</option>
                <option value="416">GUATEMALA</option>
                <option value="260">GUINEA</option>
                <option value="257">GUINEA - BISSAU</option>
                <option value="488">GUYANA</option>
                <option value="452">HAITI</option>
                <option value="424">HONDURAS</option>
                <option value="64">HUNGARY</option>
                <option value="24">ICELAND</option>
                <option value="664">INDIA</option>
                <option value="700">INDONESIA</option>
                <option value="616">IRAN</option>
                <option value="612">IRAQ</option>
                <option value="7">IRELAND</option>
                <option value="624">ISRAEL</option>
                <option value="5">ITALY</option>
                <option value="464">JAMAICA</option>
                <option value="732">JAPAN</option>
                <option value="628">JORDAN</option>
                <option value="79">KAZAKHSTAN</option>
                <option value="346">KENYA</option>
                <option value="812">KIRIBATI</option>
                <option value="636">KUWAIT</option>
                <option value="83">KYRGYZSTAN</option>
                <option value="684">LAO DEMOCRATIC REPUBLIC</option>
                <option value="54">LATVIA</option>
                <option value="604">LEBANON</option>
                <option value="395">LESOTHO</option>
                <option value="268">LIBERIA</option>
                <option value="216">LIBYA</option>
                <option value="14">LIECHTENSTEIN</option>
                <option value="55">LITHUANIA</option>
                <option value="12">LUXEMBOURG</option>
                <option value="370">MADAGASCAR</option>
                <option value="386">MALAWI</option>
                <option value="701">MALAYSIA</option>
                <option value="667">MALDIVES</option>
                <option value="232">MALI</option>
                <option value="46">MALTA</option>
                <option value="824">MARSHALL ISLANDS</option>
                <option value="228">MAURITANIA</option>
                <option value="373">MAURITIUS</option>
                <option value="412">MEXICO</option>
                <option value="823">MICRONESIA</option>
                <option value="74">MOLDOVA</option>
                <option value="13">MONACO</option>
                <option value="716">MONGOLIA</option>
                <option value="97">MONTENEGRO</option>
                <option value="204">MOROCCO</option>
                <option value="366">MOZAMBIQUE</option>
                <option value="676">MYANMAR</option>
                <option value="389">NAMIBIA</option>
                <option value="803">NAURU</option>
                <option value="672">NEPAL</option>
                <option value="3">NETHERLANDS</option>
                <option value="804">NEW ZEALAND</option>
                <option value="432">NICARAGUA</option>
                <option value="240">NIGER</option>
                <option value="288">NIGERIA</option>
                <option value="28">NORWAY</option>
                <option value="649">OMAN</option>
                <option value="662">PAKISTAN</option>
                <option value="901">PALAISTINE</option>
                <option value="818">PALAU</option>
                <option value="442">PANAMA</option>
                <option value="801">PAPUA NEW GUINEA</option>
                <option value="520">PARAGUAY</option>
                <option value="504">PERU</option>
                <option value="708">PHILIPPINES</option>
                <option value="60">POLAND</option>
                <option value="10">PORTUGAL</option>
                <option value="644">QATAR</option>
                <option value="728">REPUBLIC OF KOREA</option>
                <option value="66">ROMANIA</option>
                <option value="75">RUSSIAN FEDERATION</option>
                <option value="324">RWANDA</option>
                <option value="449">SAINT KITTS AND NEVIS</option>
                <option value="465">SAINT LUCIA</option>
                <option value="467">SAINT VINCENT AND THE GRENADINES</option>
                <option value="819">SAMOA</option>
                <option value="47">SAN MARINO</option>
                <option value="311">SAO TOME AND PRINCIPE</option>
                <option value="632">SAUDI ARABIA</option>
                <option value="248">SENEGAL</option>
                <option value="95">SERBIA</option>
                <option value="355">SEYCHELLES</option>
                <option value="264">SIERRA LEONE</option>
                <option value="706">SINGAPORE</option>
                <option value="63">SLOVAKIA</option>
                <option value="91">SLOVENIA</option>
                <option value="806">SOLOMON ISLANDS</option>
                <option value="342">SOMALIA</option>
                <option value="388">SOUTH AFRICA</option>
                <option value="11">SPAIN</option>
                <option value="669">SRI LANKA</option>
                <option value="224">SUDAN</option>
                <option value="492">SURINAME</option>
                <option value="393">SWAZILAND</option>
                <option value="30">SWEDEN</option>
                <option value="39">SWITZERLAND</option>
                <option value="608">SYRIAN ARAB REPUBLIC</option>
                <option value="736">TAIWAN, PROVINCE OF CHINA</option>
                <option value="82">TAJIKISTAN</option>
                <option value="352">TANZANIA</option>
                <option value="680">THAILAND</option>
                <option value="280">TOGO</option>
                <option value="817">TONGA</option>
                <option value="472">TRINIDAT AND TOBAGO</option>
                <option value="212">TUNISIA</option>
                <option value="52">TURKEY</option>
                <option value="80">TURKMENISTAN</option>
                <option value="807">TUVALU</option>
                <option value="400">U.S.A</option>
                <option value="350">UGANDA</option>
                <option value="72">UKRAINE</option>
                <option value="647">UNITED ARAB EMIRATES</option>
                <option value="6">UNITED KINGDOM</option>
                <option value="524">URUGUAY</option>
                <option value="81">UZBEKISTAN</option>
                <option value="816">VANUATU</option>
                <option value="45">VATICAN CITY STATE</option>
                <option value="484">VENEZUELA</option>
                <option value="690">VIETNAM</option>
                <option value="205">WESTERN SAHARA</option>
                <option value="653">YEMEN</option>
                <option value="378">ZAMBIA</option>
                <option value="382">ZIMBABWE</option>
            </select>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form class="govcy-form" novalidate action="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your address?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualAddressLine1">Address line 1</label>
               <input id="intManualAddressLine1" name="intManualAddressLine1" type="text" class="govcy-text-input" autocomplete="address-line1"> 
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualAddressLine2">Address line 2 (optional)</label>
                <input id="intManualAddressLine2" name="intManualAddressLine2" type="text" class="govcy-text-input" autocomplete="address-line2">  
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualTownOrCity">Town or city</label>
                <input id="intManualTownOrCity" name="intManualTownOrCity" type="text" class="govcy-text-input" autocomplete="address-level2">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="intManualPostalCode">Postcode</label>
            <input id="intManualPostalCode" name="intManualPostalCode" type="text" class="govcy-text-input govcy-text-input-char_20 " autocomplete="postal-code">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="country">Country</label>
            <select id="country" name="country" class="govcy-select" enterkeyhint="done" autocomplete="country">
                <option selected="selected">Select country</option>
                <option value="660">AFGHANISTAN</option>
                ...
                ...
                ...
            </select>
        </div>
    </fieldset>
</form>
```

#### Cypriot PO Box
If your service allows it, give the option to enter PO boxes. To allow users to enter PO box use the following:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your PO Box?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyPob">PO box</label>
                <input id="cyPob" name="cyPob" value="" type="text" class="govcy-text-input govcy-text-input-char_5" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyPobPostalCode">Postcode</label>
                <input id="cyPobPostalCode" name="cyPobPostalCode" value="" type="text" class="govcy-text-input govcy-text-input-char_4" autocomplete="postal-code">
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form class="govcy-form" novalidate action="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your PO Box?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyPob">PO box</label>
                <input id="cyPob" name="cyPob" value="" type="text" class="govcy-text-input govcy-text-input-char_5" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyPobPostalCode">Postcode</label>
                <input id="cyPobPostalCode" name="cyPobPostalCode" value="" type="text" class="govcy-text-input govcy-text-input-char_4" autocomplete="postal-code">
        </div>
    </fieldset>
</form>
```
#### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages).

### How to display
Displaying stored or summitted address in the following format:

```
Address line 1
Address line 2
Postal code, Town
Country
```

*For example:*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<span class="govcy-d-block">
	3 Strovolos Avenue<br>
	1234, Strovolos<br>
	Cyprus
</span>
</div>

*HTML code*
```html
<span class="govcy-d-block">
	3 Strovolos Avenue<br>
	1234, Strovolos<br>
	Cyprus
</span>
```

If you used a Cypriot lookup address, remember to add the `Apartment number` if provided and to adjust the `Street number` depending on the language used. 

For example the above example should appear as follows in Greek:
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<span class="govcy-d-block">
	Λεωφόρος Στροβόλου 3<br>
	1234, Στρόβολος<br>
	Κύπρος
</span>
</div>

*HTML code*
```html
<span class="govcy-d-block">
	Λεωφόρος Στροβόλου 3<br>
	1234, Στρόβολος<br>
	Κύπρος
</span>
```
## Pattern text
Use the following text:

| Label              | English                   | Greek                             |
| ------------------ | ------------------------- | --------------------------------- |
| **Address line 1** | Address line 1            | Διεύθυνση, γραμμή 1               |
| **Address line 2** | Address line 2 (optional) | Διεύθυνση, γραμμή 2 (προαιρετικό) |
| **Town**           | Town or city              | Πόλη ή χωριό                      |
| **Post code**      | Postcode                  | Ταχυδρομικός κώδικας              |
| **Country**        | Country                   | Χώρα                              |
| **PO box**         | PO box                    | PO box                            |

{.govcy-table} 