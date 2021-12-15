# AltaPay Omni app for Shopify

You can use the AltaPay Omni app for Shopify to configure the gateway, and access various gateway features directly in Shopify.

The Shopify plugin consists of the following, and you need to install both:

- The AltaPay Omni gateway for Shopify
- The AltaPay Omni app for Shopify

Installing and configuring it is very straightforward. You simply take the following steps:

1. Install the app and gateway
2. Configure the gateway
3. Configure the app
4. Configure your payment methods
5. Style your payment forms

We will talk you through each of the steps in detail in the following sections, after which you will be ready to use your app.

**Versions**

New versions of the AltaPay Omni-Channel plugin for Shopify will be released as new features are added and bugs are fixed.#

# PrestaShop Payment plugin installation guide

Installing this plug-in will enable the web shop to handle card transactions through AltaPay's gateway.

**Table of Contents**

[Prerequisites](#prerequisites)

[Installation](#installation)

[Configuration](#configuration)

[Styling](#styling)

[Viewing Payment Details](#viewing-payment-details)

[Switching between production and test environments](#environments)

[Making a test order](#making-a-test-order)

[Editing Shopify Theme Code](#editing-shopify-theme-code)

# Prerequisites

Before configuring the plugin, you need the below information. These can
be provided by AltaPay.

1.  AltaPay credentials:

-   Username

-   Password

2.  AltaPay gateway information:

-   Terminal

-   Gateway

# Installation
**The Gateway and App for Shopify**

The Shopify plugin consists of the following, and you need to install both:

- The AltaPay Omni gateway for Shopify
- The AltaPay Omni app for Shopify
    
> **Prerequisites**
>
> You will need:
> 
>  The username and password for your AltaPay Omni-Channel account. These will be provided by AltaPay.
> - If you have a production account, you will need a URL, e.g. https://testgateway.altapaysecure.com. This will be provided by AltaPay.
> - The <shop_name> in the URL for your Shopify shop's admin page
> (It is typically in the format https://<shop_name>.myshopify.com/admin)

1. First, you need to install the AltaPay Omni gateway for Shopify.
Go to the appropriate link. If you are working in the production environment, replace <shop_name> with the one identified in your admin page:

<table>
<tbody>
  <tr>
    <td><strong>Test</strong></td>
    <td>https://&lt;shop_name&gt;.myshopify.com/admin/authorize_gateway/1054445</td>
  </tr>
  <tr>
    <td><strong>Production</strong></td>
    <td>https://&lt;shop_name&gt;.myshopify.com/admin/authorize_gateway/1054447</td>
  </tr>
</table>
</tbody>

- Follow the installation steps.
2. Now, install the AltaPay Omni app.
- Go to the appropriate link, replacing <shop_name> with the one identified in your admin page:

<table>
<tbody>
  <tr>
    <td><strong>Test</strong></td>
    <td>https://shopifystaging.altapayplatform.com/api/shopify/apps/authentication?shopHostName=&lt;shop_name&gt;.myshopify.com</td>
  </tr>
  <tr>
    <td><strong>Production</strong></td>
    <td>https://shopify.altapayplatform.com/api/shopify/apps/authentication?shopHostName=&lt;shop_name&gt;.myshopify.com</td>
  </tr>
</table>
</tbody>

- You will be prompted for your AltaPay Omni-Channel username and password, and the URL if you are setting up a production account.
3. Next, you need to configure the gateway. See [Configuring the AltaPay Omni Gateway for Shopify](#configuring-the-altapay-omni-gateway-for-shopify) for more details.

# Configuration

## Configuring the AltaPay Omni Gateway for Shopify

When you first open the app from the administration page in Shopify, you need to configure the gateway account.

> **Prerequisites**
> 
> You will need:
> 
> - The API password for your AltaPay Omni-Channel account. This will be provided by AltaPay.
> - Your Shopify shop name, which you define when you create your shop

1. Navigate to the **Admin** page, using the URL.
2. Select the **Settings** button in the bottom left of the screen.
3. Go to **Payment Providers**
4. Scroll down to **Alternative Payment Methods** and do one of the following:
- If you see AltaPay Omni, click on the Edit button beside it.
- If AltaPay Omni is not displayed, select the **Choose alternative payment** buttont, and select AltaPay Omni from the list
5. The account information is displayed.
6. Key in the shop name and password, and then select the payment methods that you support.
7. You may choose to enable test mode by selecting the checkbox at the bottom of the screen.
**If test mode is enabled, all transactions, including those made using the Production tab, will go to the test gateway. No actual financial transactions will take place.**
8. Click **Activate** when you have completed the details.
9. Next, you need to configure the app. See [Configuring the AltaPay Omni App for Shopify](#configuring-the-altapay-omni-app-for-shopify) for more details.

## Configuring the AltaPay Omni App for Shopify

Having configured the AltaPay Omni gateway, you now need to configure the app.

> **Prerequisites**
> 
> To log in, you will need:
> - The username and password for your AltaPay Omni-Channel account
> - The URL for the AltaPay Omni-Channel gateway
> 
> All of these will be provided by AltaPay.

1. Navigate to the Admin page, using the URL.
2. Select Apps and then the gateway.
3. The configuration window is displayed.
4. You will see that there are two tabs on this page, even if you do not have a production account:
- **Test** for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
- **Production** for configuring the production account, i.e. the account which will enable actual financial transactions. **If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.**

5. Make sure that you are working in the correct tab.
6. Enter the username and password AltaPay has given to you.
7. If you are working in the Production account, specify the AltaPay Omni-Channel URL.

![shopify_gateway_config](/Docs/configuration/shopify-gateway-config.png)

8. Save the details.
9. Next, you need to configure the payment methods (terminals). See [Configuring the Payment Method terminals in the Shopify App](#configuring-the-payment-method-terminals-in-the-shopify-app) for more details.

## Configuring the Payment Method terminals in the Shopify app

> **Prerequisites**
> 
> To log in, you will need:
> 
> - The username and password for your AltaPay Omni-Channel account. These are provided by AltaPay.
> - The URL for your Shopify shop's admin page.
(It is typically in the format https://<shop_name>.myshopify.com/admin)

1. Navigate to the Admin page, using the URL.
2. You will see that there are two tabs on this page:

>- Test for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
>- Production for configuring the production account, i.e. the account which will enable actual financial transactions. **If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.**

3. Make sure that you are working in the correct tab.
4. You will see a list of payment methods configured by AltaPay according to the agreement you have made with us.

![shopify_config_pm_1](/Docs/configuration/shopify_config_pm_1.png)

The default names of the payment methods come from the title the payment method has been given by AltaPay.

5. Click on a given terminal/payment method to change the configuration.
6. The payment method details are displayed. Configure the details as required, using the notes and illustration for guidance.

![shopify_config_pm_2](/Docs/configuration/shopify_config_pm_2.png)

>- Complete the details:

<table>
<tbody>
  <tr>
    <td><strong>Payment method name as displayed to customer</strong></td>
    <td>Key in the name you want shown on the screen</td>
  </tr>
  <tr>
    <td><strong>Secret</strong></td>
    <td>The payment method <strong>secret</strong>. If it is decided as part of the onboarding process that this parameter is relevant for you, it will be provided by AltaPay.</td>
  </tr>
  <tr>
    <td><strong>Display priority</strong></td>
    <td>Enter a value to indicate the order in which you want payment methods displayed on the page where the customer selects their preferred payment method. 1 is the highest priority. If you give the same display priority to more than one payment method, they will be shown in alphabetical order.
</td>
  </tr>
</table>
</tbody>

- If necessary, enable the payment method as a **gift card payment method**.
- Specify whether **order details** will be shown in the payment form.

>**Tips**
>
>If a high amount of orders are placed in a shop (more than 2 orders per second), it might require additional time (up to 5 seconds) to fetch the order details from Shopify due to their API call limit. If you do not want this delay, disable this option. If the retrieval time exceeds 5 seconds, the order details will not be shown or sent to the gateway.

- Select whether the **payment method is active** - this decides whether the customer can select this payment method to complete the transaction.
- Choose from the predefined **icons** to display to the customer for a given payment method. You can select a single icon from the left hand column. If the payment method is Credit Card, you can select multiple icons. These will be shown in the Select Payment Method page, and the Payment Form page.

7. Click on <strong>Save </strong>to save the details.

**Requirements for Specific Payment Methods**

**Klarna**

A customer telephone number is required when using Klarna.

1. In Shopify, navigate to Settings > Checkout.
2. Go to the <strong>Form Options</strong> section, and mark the <strong>Shipping address phone number</strong> in the checkout flow as “Required”.

![shopify_klarna](/Docs/configuration/shopify_klarna.png)

# Styling 

**Styling the Payment Pages in the AltaPay Omni app for Shopify**

You can style the Select Payment Method and Payment Form pages within the Shopify plugin.

> **Prerequisites**
> 
> To log in, you will need:
> 
> - The username and password for your AltaPay Omni-Channel account
> - The URL for your Shopify shop's admin page.
(It is typically in the format <strong>https://<shop_name>.myshopify.com/admin)</strong>
> 
> All of these details will be emailed to you by AltaPay as part of the onboarding.
> 
> **You cannot change certain elements of the page. The AltaPay logo must remain in the header, and the statement in the footer must not be altered.**

1. Navigate to the Admin page, using the URL.
2. Select Apps in the left hand pane, and then AltaPay Omni Gateway.
3. You will see that there are two tabs on this page:

>- <b>Test</b> for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
>- <b>Production</b> for configuring the production account, i.e. the account which will enable actual financial transactions

4. Make sure that you are working in the correct tab.
5. Select Settings at the top of the window.
6. Scroll down to the Payment pages styling section, where you will find the code for the <b>Select Payment Method</b> page, followed by the <b>Payment Form page</b>.
7. Make your changes, noting the following:

>- <b>You cannot change certain elements of the page. The AltaPay logo must remain in the header, and the statement in the footer must not be altered.</b>
>- In the Select <b>Payment Method</b> page:
>- The mandatory payment method placeholder is<br>
< div class="sm:w-1/2 sm:mr-2 md:mr-4 order-2 sm:order-1" id="PaymentMethodsPlaceholder"></div>
>- The order details placeholder is<br>
< div class="sm:w-1/2 sm:ml-2 md:ml-4 sm:mb-0 order-1 sm:order-2" id="OrderDetailsPlaceholder">

In the <b>Payment Form</b> page:

- The credit cards placeholder is<br>
< div class="px-4 md:px-10 text-center mb-8" id="CreditCardsPlaceholder"><br>
- The dynamic cancel payment url will be replaced on a <a> tag with CancelPaymentLinkPlaceholder
- The cancel payment button <b>(CancelPaymentButtonPlaceholder)</b> will be removed for credit customer and verify card transactions
>You should adhere to the rules and advice specified in the online help in the testgateway - https://testgateway.altapaysecure.com/merchant/help/FrontendIntegration#Payment_page__form_callback

8. Click on <b>Save</b> to save the details, or <b>Reset HTML to Default</b> to restore the default settings.

## Enable Credit Card Form by Defaul on Checkout
  
**Display the credit card inputs by default on the terminal selection page**
  
To display the credit card inputs by default on the terminal selection page follow the below steps.
• Login to the Shopify admin section.
  
• Navigate to the **Apps** section.
  
• Click on the **AltaPay Gateway** app.
  
• Click on the **Settings** tab.
  
• Scroll to **Show credit card form by default** section and click on **Enable** button and **Save** the
settings.

![shopify_klarna](/Docs/enable_cc-by_default/enable_cc_by_default.jpg)
  
> Note: Existing merchants need to perform the below step to load
> the new elements on the payment page.
> It's recommended to take a backup of existing HTML on the **Settings** page.
  
• Scroll bottom of the **Settings** page and click on **Reset HTML to default** and then click **Save**.
  
![shopify_klarna](/Docs/enable_cc-by_default/reset_html.jpg)
  
**Frontend View**
  
![shopify_klarna](/Docs/enable_cc-by_default/front_end.jpg)

# Using the AltaPay Omni app for Shopify

**Crediting a customer**

To refund orders, you can just go to the given order and click “Refund”. However, you might want to credit a customer who has not placed an order. In this case you can use the <b>Credit Customer</b> functionality in the app. There are two ways to credit a customer; by credit card token, and by credit card details.

**Credit by credit card token**

If the credit should go on a card that the customer has used on an order, but the customer does not want to give out their payment details, you can use a unique credit card token instead. All you need is the customer email address which was used on the order.

1. Navigate to the Admin page, using the URL.
2. Select **Apps** in the left hand pane, and then **AltaPay Omni Gateway**.
3. Then go to the **Credit Customer** screen.

> **Notes.**
>  
> There are two tabs; Production and Test. Make sure you are working in the correct one.

![shopify_credit](/Docs/use_plugin/shopify_credit.png)

4. Key in the email address.
5. Click on <b>Lookup credit cards.</b>
6. A drop down list of previously used credit cards is displayed, with masked PANs.
7. Verify which card the customer wishes to credit.
8. Select the relevant payment method, enter a description and the amount to credit.

![shopify_credit_complete](/Docs/use_plugin/shopify_credit_complete.png)

9. Click <b>Credit customer.</b>
10. A new window with a payment form will be opened, prefilled with the credit card details related to the selected credit card. You must still ask the customer for the CVC/CVV2 for security reasons. The link to the payment form will be shown in the app as well, in case you have disabled pop-up windows.

![when_the_email_address_has_2](/Docs/use_plugin/when_the_email_address_has_2.png)

Making the credit via AltaPay’s payment form means that you as a merchant do not need to be PCI compliant.

**Credit by credit card details**

If the customer has not placed an order in your shop before, or wants to use a card he/she has not used in your store before, you should credit by credit card details.

1. Navigate to the Admin page, using the URL.
2. Select <b>Apps</b> in the left hand pane, and then <b>AltaPay Omni Gateway.</b>
3. Then go to the <b>Credit Customer</b> screen.

![shopify_credit](/Docs/use_plugin/shopify_credit.png)

>**Notes**
> 
>There are two tabs; Production and Test. Make sure you are working in the correct one.

4. In the Credit by credit card details section, select the relevant payment method, enter a description and the amount to credit.
5. Click **Credit customer**.
6. A new window with a payment form will be opened, and you need to fill out the payment details supplied by the customer. If the customer does not want to give their credit details over the phone, you can verify the card using a link. See [Verifying a Card via Link](#verifying-a-card-via-link) for more details.
  

**Verifying the Order against Stock**

In the Settings, you can configure whether you want a given order to be verified in relation to product stock, as well as discount and shipping validity during the authorization flow before the payment is taken.

1. Navigate to the **Admin** page, using the URL.
2. Select **Apps** in the left hand pane, and then **AltaPay Omni Gateway**.
3. In the **Settings** section, choose whether you want to enable/disable the verification.

![shopify_settings_verify_order](/Docs/use_plugin/shopify_settings_verify_order.png)

There are two tabs; Production and Test. Make sure you are working in the correct one.

## Verifying a Card via Link
If a customer does not want to give out their payment details by phone, you can generate a link to AltaPay’s secure PCI compliant payment form, and send it to them via email.

The customer can use the link to the payment form to enter their payment details securely, and you (the merchant) can then use a unique credit card token for the card, e.g. for crediting the customer.

1. Navigate to the Admin page, using the URL.
2. Select Apps in the left hand pane, and then AltaPay Omni Gateway.
3. Then select the Miscellaneous button at the top of the window.
4. You will see two tabs. Ensure you are working in the correct one:

- <b>Test</b> for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
- <b>Production</b> for configuring the production account, i.e. the account which will enable actual financial transactions. <b>If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.</b>

5. Navigate to the <b>Verify card</b> page.

![shopify_verify_card](/Docs/use_plugin/shopify_verify_card.png)

6. Specify the customer email, and the terminal/payment method.
7. Click on Send verify card link.
8. The customer will receive an email from the AltaPay payment gateway, which will contain a link to the payment form.
9. When the customer completes and returns the details, a token is generated.
10. When you (the merchant) are told by the customer that the details have been submitted, you can use the token in place of the card details to complete transactions.

**Querying a Gift Card**

If your agreement with AltaPay includes the gift card payment method, you can query the remaining amount on the gift card, if a customer requests this information.

> **Prerequisites**
> 
> You must have at least one terminal with gift card enabled, as explained in [Configuring the Payment Method terminals in the Shopify App](#configuring-the-payment-method-terminals-in-the-shopify-app).

The query can either be made by the account identifier (gift card number), or by gift card token.

**Query by account identifier (number)**

1. Navigate to the Admin page, using the URL.
2. Select Apps in the left hand pane, and then AltaPay Omni Gateway.
3. Then select the Miscellaneous button at the top of the window.
4. You will see two tabs. Ensure you are working in the correct one:
- <b>Test</b> for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
- <b>Production</b> for configuring the production account, i.e. the account which will enable actual financial transactions. If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.
5. Navigate to the Query by id page.
6. Complete the details, specifying the relevant payment method, the card number of the gift card, and the gift card provider.

![when_the_email_address_has_6](/Docs/use_plugin/when_the_email_address_has_6.png)

Click on <b>Lookup amount</b> to display the remaining balance.

**Query by gift card token**

To query by gift card token, select the relevant payment method in the **Terminal to check against** field, and enter the gift card token.

1. Navigate to the Admin page, using the URL.
2. Select **Apps** in the left hand pane, and then **AltaPay Omni Gateway**.
3. Then select the **Miscellaneous** button at the top of the window. You will see two tabs; ensure that you are working in the correct one:
- **Test** for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
- **Production** for configuring the production account, i.e. the account which will enable actual financial transactions. **If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.**
4. Navigate to the **Query by id** page.
5. Complete the details, specifying the relevant payment method, and the gift card token.

![when_the_email_address_has_7](/Docs/use_plugin/when_the_email_address_has_7.png)

6. Click on **Lookup amount** to display the remaining balance.

# Viewing Payment Details

You can view details on payments in the Shopify app, including payment method, fraud information, payment options, and, if relevant, gift card details.

1. Navigate to the Admin page, using the URL.
2. Select Orders in the left hand pane.
3. Select the order you want to view.
4. In the Additional Details pane, on the right hand side, you will see the AltaPay Omni-Channel transaction ID, and an overview of the order.
5. Here, you can see which payment method was used for a given payment in the order timeline, and high level fraud information. You can also see whether an option is supported for a given payment. (Some of the payment methods provided by AltaPay may not support all payment options such as payment release, refund or multiple refunds.)
You can change the information that you see by clicking on **Edit** and updating the details.
6. For more detailed information, use the transaction ID to search for the transaction in the Merchant Information Interface.
7.If your agreement with AltaPay includes a gift card payment method, you can enable customers to query the remaining amount of their gift card. In order to do this, you must:
-	Enable the gift card option on the given terminal - see [Configuring the payment methods (terminals)](https://docs.google.com/document/d/1E3Gbdpp2LVoT2Bvl8fEnhEvj-illN0msvizJpNjs27U/edit#heading=h.t53ej0y6yaf7?ts=5dc125cb) for more information.
-	Insert a piece of code in your Shopify theme code. Which code to insert depends on which theme you are using, but an example of the code can be seen in [Editing Shopify Theme Code](#editing-shopify-theme-code)

# Environments

**Switching between production and test environments**

If you want to test the gateway in the test environment and switch to the production environment, or vice versa, you must remember to:

-	Change the account details on the gateway, and set the test flag accordingly:
>1.	Go to Settings > Payment providers.
>2. Scroll down to **Alternative payment methods**.
>3. Click **Edit** where it says “AltaPay Omni is active”.

![shopify_altve_pm](/Docs/switching_bw_test_and_producrtion_env/shopify_altve_pm.jpg)

> **Tips**
> 
> Ensure the relevant account is defined in the app, as described in [Configuring the AltaPay Omni Gateway for Shopify](#configuring-the-altapay-omni-gateway-for-shopify).

# Making a test order

In order to place an order and pay with the AltaPay Omni-Channel test gateway, you should first ensure the test environment is properly set up:

- Change the account details on the gateway, and set the test flag accordingly:
>1. Go to Settings > Payment providers.
>2. Scroll down to **Alternative payment methods**.
>3. Click **Edit** where it says “AltaPay Omni is active”.

![shopify_altve_pm](/Docs/making_a_test_order/shopify_altve_pm.jpg)

> **Tips**
> 
> Ensure the relevant account is defined in the app, as described in [Configuring the AltaPay Omni Gateway for Shopify](#configuring-the-altapay-omni-gateway-for-shopify).

1. Place an order, selecting the AltaPay Omni-Channel gateway in the checkout.
2. Select the payment method on the following page and enter some dummy payment details.
3. You know that it has completed successfully when the Success page is displayed.

> **Notes**
> 
> The payment can be released, captured and/or refunded as well.

# Editing Shopify Theme Code

If you want to use a gift card terminal, you can enable the customer to query a gift card by inserting the source code below in the theme.

1. Navigate to Online Store > Themes
2. Click Actions > Edit code on the current theme.
3. **If you are using the test gateway**, insert the following:

```html
  <form action="https://shopifystaging.altapayplatform.com/api/shopify/public/giftcards">
            <input type="hidden" name="environment" value="test">
            <input type="hidden" name="shopName" value="<shop_name>">
      Account identifier:<br>
      <input type="text" name="accountIdentifier">
      <br>
      Gift card provider:<br>
      <select name="provider">
          <option value="test">test</option>
    </select>
      <br><br>
      < input type="submit" value="Submit">
</form>
  ```

> **Notes**
> 
> <shop_name> should be replaced by the shop name, as explained in the [Installation](#installation) of The Gateway and App for Shopify.

4. **If you are using the production gateway,** replace the test code with the following:

```html
  <form action="https://shopify.altapaysecure.com/api/shopify/public/giftcards">
            <input type="hidden" name="environment" value="prod">
            <input type="hidden" name="shopName" value="<shop_name>">
      Account identifier:<br>
      <input type="text" name="accountIdentifier">
      <br>
      Gift card provider:<br>
      <select name="provider">
          <option value="test">PPS</option>
          <option value="test">SVS</option>
    </select>
      <br><br>
      <input type="submit" value="Submit">
</form> 
 ```
