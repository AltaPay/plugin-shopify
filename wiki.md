# AltaPay Payments App

You can use the AltaPay Payments App to configure the gateway, and access various gateway features directly in Shopify.

Installing and configuring it is very straightforward. You simply take the following steps:

1. Install the app
2. Configure the app
3. Configure your payment methods
4. Style your payment forms

We will take you through each of the steps in detail in the following sections, after which you will be ready to use your app.

**Versions**

New versions of the app will be released as new features are added and bugs are fixed.

# Installation

Installing this app will enable the web shop to handle card transactions through AltaPay's gateway.

**Table of Contents**

 - [Prerequisites](#prerequisites)

 - [Installation Link](#installation-link)

 - [Configuration](#configuration) 
  
    * [Configuring the checkout options](#configuring-the-checkout-options)
      
    * [Configuring the AltaPay Payments App](#configuring-the-altapay-payments-app)

    * [Configuring the Payment Methods](#configuring-the-payment-methods)

 - [Styling](#styling)

    * [Styling the Payment Pages in the AltaPay Payments App for Shopify](#styling-the-payment-pages-in-the-altapay-payments-app-for-shopify)

    * [Enable Credit Card Form by Default on Checkout](#enable-credit-card-form-by-default-on-checkout) 

 - [Using the AltaPay Payments App for Shopify](#using-the-altapay-payments-app-for-shopify)

 - [Viewing Payment Details](#viewing-payment-details)

 - [Switching between production and test environments](#environments)

 - [Making a test order](#making-a-test-order)

# Prerequisites

Before configuring the app, you need the below information. These can
be provided by AltaPay.

1.  AltaPay credentials:

    * Username
    * Password

2.  AltaPay gateway information:

    * Terminal
    * Gateway

# Installation Link

You can install the app directly by following the below installation link

``https://accounts.shopify.com/store-login?redirect=settings%2Fpayments%2Falternative-providers%2F1059191``

# Configuration

## Configuring the checkout options

When you first open the app from the admin page in Shopify, you need to configure the checkout options.

1. Navigate to the **Admin** page, using the URL.
2. Select the **Settings** button in the bottom left of the screen.

![shopify_settings_menu](/Docs/configuration/shopify_settings_menu_updated.png)

3. Go to **Payments**

4. Scroll down to **Supported payment methods** and do one of the following:
- If you see AltaPay, click on the **Manage** button beside it. 

![shopify_manage_AltaPay_Omni](/Docs/configuration/altapay_supported_payment_methods.jpg)

- If AltaPay is not displayed, select the **Add payment methods** button, and select AltaPay from the list
5. Select the payment icons that you want to display with AltaPay payment method on checkout page.

![shopify_select_icons](/Docs/configuration/shopify_select_icons.jpg)

**Note:** Maximum of 4 icons will be displayed or ‘and more’ will be displayed in the checkout.

![altapay_on_checkout](/Docs/configuration/altapay_on_checkout.jpg)

8. You may choose to enable test mode by selecting the checkbox at the bottom of the screen.
**If test mode is enabled, all transactions, including those made using the Production tab, will go to the test gateway. No actual financial transactions will take place.**

If linking the account to testgateway.altapaysecure.com, then ‘TEST MODE’ must be enabled to avoid error in checkout! 

![shopify_enable_test_mode](/Docs/configuration/shopify_enable_test_mode.jpg)

9. Click **Activate** when you have completed the details.
10. Next, you need to configure the app. See [Configuring the AltaPay Payments App for Shopify](#configuring-the-altapay-omni-app-for-shopify) for more details.

## Configuring the AltaPay Payments App

Having configured the AltaPay payments, you now need to configure the app.

> **Prerequisites**
> 
> To log in, you will need:
> - The username and password for your AltaPay Omni-Channel account
> - The URL for the AltaPay Omni-Channel gateway
> 
> All of these will be provided by AltaPay.

1. Navigate to the **Admin** page, using the URL.
2. Select **Settings** and then **Payments**.
3. Scroll down to **Supported payment methods** and click **Manage** link besides AltaPay payment method.
4. Click on **Manage** button from **Account status** section.
5. This will redirect you to **AltaPay Payments App** configuration page.
6. You will see that there are two tabs on this page, even if you do not have a production account:
- **Test** for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
- **Production** for configuring the production account, i.e. the account which will enable actual financial transactions. **If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.**

5. Make sure that you are working in the correct tab.
6. Enter the username and password AltaPay has given to you.
7. If you are working in the Production account, specify the AltaPay Omni-Channel URL.

![shopify_gateway_config](/Docs/configuration/shopify_gateway_config.jpg)

8. Save the details.
9. Next, you need to configure the payment methods (terminals). See [Configuring the Payment Methods](#configuring-the-payment-methods) for more details.

## Configuring the Payment Methods

> **Prerequisites**
> 
> To log in, you will need:
> 
> - The username and password for your AltaPay Omni-Channel account. These are provided by AltaPay.
> - The URL for your Shopify shop's admin page.
(It is typically in the format **https://<shop_name>.myshopify.com/admin**)

1. Navigate to the Admin page, using the URL.
2. You will see that there are two tabs on this page:

>- **Test** for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
>- **Production** for configuring the production account, i.e. the account which will enable actual financial transactions. **If test mode is enabled in the AltaPay Omni gateway, all transactions, including those done in the Production tab, will go to the test gateway and no actual transactions will take place.**

3. Make sure that you are working in the correct tab.
4. You will see a list of payment methods configured by AltaPay according to the agreement you have made with us.

![shopify_config_pm_1](/Docs/configuration/shopify_config_pm_1.png)

The default names of the payment methods come from the title the payment method has been given by AltaPay.

5. Click on a given terminal/payment method to change the configuration.
6. The payment method details are displayed. Configure the details as required, using the notes and illustration for guidance.

![config_terminals](/Docs/configuration/config_terminals.jpg)

>- Complete the details:

<table>
<tbody>
  <tr>
    <td><strong>Payment method name as displayed to customer</strong></td>
    <td>Key in the name you want show on the screen</td>
  </tr>
  <tr>
    <td><strong>Secret</strong></td>
    <td>The payment method <strong>secret</strong>. If it is decided as part of the onboarding process that this parameter is relevant for you, it will be provided by AltaPay.</td>
  </tr>
  <tr>
    <td><strong>Display priority</strong></td>
    <td>Enter a value to indicate the order in which you want payment methods to be displayed on the page, where the customer selects their preferred payment method. 1 is the highest priority. If you give the same display priority to more than one payment methods, they will be shown in alphabetical order.
</td>
  </tr>
</table>
</tbody>

- Specify whether **order lines** will be shown in the payment form.

>**Tips**
>
> Order lines are required for Klarna payments. So you have to enable the order lines optionfor Klarna in Terminal settings.
To enable the order lines, click on a Klarna terminal and scroll to the "Order lines" section, and click on the "Enable" button.

- Select whether the **payment method is active** - this decides whether the customer can select this payment method to complete the transaction.
- Choose from the predefined **icons** to display to the customer for a given payment method. You can select a single icon from the left hand column. If the payment method is **Credit Card**, you can select multiple icons. These will be shown in the **Select Payment Method** page, and the **Payment Form** page.

7. Click on <strong>Save </strong>to save the details.

**Requirements for Specific Payment Methods**

## Klarna

A customer telephone number is required when using Klarna.

1. In Shopify, navigate to Settings > Checkout.
2. Go to the <strong>Form Options</strong> section, and mark the <strong>Shipping address phone number</strong> in the checkout flow as **“Required”**.

![shopify_klarna](/Docs/configuration/shopify_klarna.png)

# Styling 

### Styling the Payment Pages in the AltaPay Omni app for Shopify

You can style the **Select Payment Method** and **Payment Form** pages within the **Shopify plugin**.

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

1. Navigate to the **Admin** page, using the URL.
2. Select **Apps** in the left hand pane, and then AltaPay Omni Gateway.
3. You will see that there are two tabs on this page:

>- <b>Test</b>, for configuring a test account which can be used to test the gateway. No actual financial transactions will be made via this account.
>- <b>Production</b>, for configuring the production account, i.e. the account which will enable actual financial transactions

4. Make sure that you are working in the correct tab.
5. Select **Settings** at the top of the window.
6. Scroll down to the **Payment pages styling** section, where you will find the code for the <b>Select Payment Method</b> page, followed by the <b>Payment Form page</b>.
7. Make your changes, noting the following:

>- <b>You cannot change certain elements of the page. The AltaPay logo must remain in the header, and the statement in the footer must not be altered.</b>
>- In the Select <b>Payment Method</b> page:
>- The mandatory payment method placeholder is
```html
    <div class="sm:w-1/2 sm:mr-2 md:mr-4 order-2 sm:order-1" id="PaymentMethodsPlaceholder"></div>
```
>- The order details placeholder is<br>
```html
    <div class="sm:w-1/2 sm:ml-2 md:ml-4 sm:mb-0 order-1 sm:order-2" id="OrderDetailsPlaceholder">
```
In the <b>Payment Form</b> page:

- The credit cards placeholder is<br>
```html
    <div class="px-4 md:px-10 text-center mb-8" id="CreditCardsPlaceholder">
 ```
- The dynamic cancel payment url will be replaced on a <a> tag with CancelPaymentLinkPlaceholder
- The cancel payment button <b>(CancelPaymentButtonPlaceholder)</b> will be removed for credit customer and verify card transactions
>You should adhere to the rules and advice specified in the online help in the testgateway - https://testgateway.altapaysecure.com/merchant/help/FrontendIntegration#Payment_page__form_callback

8. Click on <b>Save</b> to save the details, or <b>Reset HTML to Default</b> to restore the default settings.

## Enable Credit Card Form by Default on Checkout
  
**Display the credit card inputs by default on the terminal selection page**

![shopify_klarna](/Docs/enable_cc-by_default/front_end.jpg)
  
To display the credit card inputs by default on the terminal selection page follow the below steps.
Login to the Shopify admin section.
  
- Navigate to the **Apps** section.
  
- Click on the **AltaPay Gateway** app.
  
- Click on the **Settings** tab.
  
- Scroll to **Show credit card form by default** section and click on **Enable** button and **Save** the
settings.

![shopify_klarna](/Docs/enable_cc-by_default/enable_cc_by_default.jpg)
  
> Note: Existing merchants need to perform the below step to load
> the new elements on the payment page.
> It's recommended to take a backup of existing HTML on the **Settings** page.
  
- Scroll bottom of the **Settings** page and click on **Reset HTML to default** and then click **Save**.
  
![shopify_klarna](/Docs/enable_cc-by_default/reset_html.jpg)

# Using the AltaPay Payments App for Shopify

# Viewing Payment Details

You can view details on payments in the Shopify app, including payment method, fraud information, payment options, and, if relevant, gift card details.

1. Navigate to the **Admin** page, using the URL.
2. Select **Orders** in the left hand pane.
3. Select the order you want to view.
4. In the **Additional Details** pane, on the right hand side, you will see the AltaPay Omni-Channel transaction ID, and an overview of the order.
5. Here, you can see which payment method was used for a given payment in the order timeline, and high level fraud information. You can also see whether an option is supported for a given payment. (Some of the payment methods provided by AltaPay may not support all payment options such as payment release, refund or multiple refunds.)
You can change the information that you see by clicking on **Edit** and updating the details.
6. For more detailed information, use the transaction ID to search for the transaction in the Merchant Information Interface.

# Environments

**Switching between production and test environments**

If you want to test the gateway in the test environment and switch to the production environment, or vice versa, you must remember to:

-	Change the account details on the gateway, and set the test flag accordingly:
>1.	Go to Settings > Payment providers.
>2. Scroll down to **Alternative payment methods**.
>3. Click **Manage** where it says “AltaPay Omni is active”.

![shopify_altve_pm](/Docs/switching_bw_test_and_producrtion_env/shopify_altve_pm.jpg)

> **Tips**
> 
> Ensure the relevant account is defined in the app, as described in [Configuring the AltaPay Omni Gateway for Shopify](#configuring-the-altapay-omni-gateway-for-shopify).

# Making a test order

In order to place an order and pay with the AltaPay Omni-Channel test gateway, you should first ensure the test environment is properly set up:

- Change the account details on the gateway, and set the test flag accordingly:
>1. Go to Settings > Payment providers.
>2. Scroll down to **Alternative payment methods**.
>3. Click **Manage** where it says “AltaPay Omni is active”.

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
