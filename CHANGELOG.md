# Changelog
All notable changes to this project will be documented in this file.

## [app-1.0.6]
- Fix: Add Shopify store order **Payment ID** as reconciliation identifier in AltaPay Gateway

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
