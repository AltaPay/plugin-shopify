# Changelog
All notable changes to this project will be documented in this file.

## [app-1.3.3]

- Add support for Twint and SEPA.
- Update logo for iDEAL and ViaBill.

## [app-1.3.2]

 - Add support for Open Banking (Using Finshark).
 - On cancel or abandon payments, redirect buyers back to Shopify’s checkout if the merchant has only a single payment method enabled.

## [app-1.3.1]

- Add support for the Bancontact individual app.

## [app-1.3.0]
 - Add a new design option with a modern look for the payment form.
 - Add terminal logo for Bancontact & Bank payments.
 - Fix styling for redirect page.

## [app-1.2.9]
 - Fix: Duplicate Klarna payment not releasing when auto-capture is enabled.

## [app-1.2.8]

- Fix: Cookies conflict when installing multiple apps simultaneously.
- Make errors messages distict in the app configuration pages.

## [app-1.2.7]

- Add support for the Swish individual app.
- Fix Swish app payment form styling issues.
- Add checksum validation functionality.

## [app-1.2.6]

- Add support for the ViaBill individual app.
- Redirect merchant to payment method page after app onboarding.

## [app-1.2.4]

- Add support for the iDEAL individual app.

## [app-1.2.3.1]

- Add support for the Klarna individual app.

## [app-1.2.3]

- Fix: Improvements to make Shopify payment statuses update jobs more robust.

## [app-1.2.2.1]

- Add support for the Vipps individual app.
- Add support for the Card Payments individual app.

## [app-1.2.2]

- Fix: terminal icon not assigned automatically for individual apps

## [app-1.2.1]

- Add support for the MobilePay individual app.
- Redirect to the payment page by default if the merchant has only one active terminal.
- Implement Content Security Policy frame-ancestors directive to avoid clickjacking.

## [app-1.1.2]

- Use redis for queues to make Shopify payment statuses update jobs more robust.

## [app-1.1.1]

- Fix: Make Shopify payment statuses update jobs more reliable and remove delays.
 
## [app-1.1.0]

- Fix: Allow checkout when any address field is missing from Shopify end.

## [app-1.0.9]

- Fix: Capture payments if auto-capture is enabled & payment is still in capturable state.

## [app-1.0.8]
- Fix: Increase masked pan length to prevent data loss for capture operations
- Update AltaPay PHP SDK version to support API changes from 20221026

## [app-1.0.7]
- Fix: Checkout custom HTML change doesn't affect the checkout page
- Fix: Checkout "Other payment methods" heading is showing when only the credit card is enabled

## [app-1.0.6]
- Add Shopify store order **Payment ID** as reconciliation identifier in AltaPay Gateway

## [app-1.0.5]
- Fix: Auto release payments issue

## [app-1.0.4]
- Fix: Handle duplicate transactions against same order id

## [app-1.0.3]
- Fix: Do not create pending order on payment failure
- Show error message on payment failure

## [app-1.0.2]
- Fix: Translation issue for payment form
- Fix: Payment capture issue in case of previous declined status

## [app-1.0.1]
- Fix: Payment capture status discrepancy in case of iDEAL when capture is set to manual in Shopify store

## [app-1.0.0]
- First release of app using the new Payments Apps Platform
https://shopify.dev/apps/payments

- **Supported Features:**
    - Payment Page Redirect
    - Auto-Expand Credit Card Form
    - Configuration of payment methods
    - Payment Methods and Payment Form pages styling option
    - Switching between production and test environments
    - Multilingual Support

# HPSDK Payment App [deprecated]

## [2.2.4]
- Add option to display credit card form by default on terminal selection page
## [2.2.3]
- Support mobile rendering for payment selection page
## [2.2.2]
- Redesigned payment selection page
## [2.2.1]
- Fail gracefully when the callback's result is unknown
## [2.2.0]
- Added icons for Sofort, Swish, and Vipps terminal
- Updated icon for Klarna
- Updated the list for payment statuses
## [2.1.9]
- Support host query parameter for OAuth
- Fix: Alignment of credit card form fields
## [2.1.8]
- Fix: Gift card issue on the checkout page
## [2.1.7]
- Fix: Price mismatch with the order lines
- Fix: Styling issue on the payment page
- Fix: Capture and Refund with new Klarna implementations
## [2.1.6]
- Fix: Login issue in account configuration page
## [2.1.5]
- Re-branding from Valitor to Altapay
- API access token now supports 250 characters
- Fix: Unable to decode characters for some locales
## [2.1.0]
- Added the possibility of customizing the select payment method and payment form pages
- Multiple small fixtures
## [2.0.0]
- Multiple fixtures and improvements
## [1.0.0]
- First release of the plugin
