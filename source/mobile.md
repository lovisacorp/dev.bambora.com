---
title: Mobile

toc_above:
  - <a href='index.html'>Getting Started</a>
  - <a href='mobile.html'>Mobile</a>

includes:
  - mobile/bnpayment-android
  - mobile/bnpayment-ios
  - mobile/how-to-capture-payments

toc_below:
  - <a href='online.html'>Online</a>
  - <a href='api.html'>API</a>
  - <a href='carts.html'>Shopping Carts</a>

search: true
---
# Overview

The `Native Payment` SDK from Bambora makes it simple to accept credit card payments in your app.

Specifically, by adding Native Payment to your project you can make it possible for the users of your app to:

* Register credit cards.

* Make purchases using registered credit cards.

The purpose of `Native Payment` is to save you time by providing you with an easy-to-use, up-to-date and actively maintained codebase for interacting with the Native Payment backend.

**[Click](https://github.com/bambora/dev.bambora.com/blob/master/source/mobile.md) to edit this section.**

## Platform support

`Native Payment` is currently available for [Android](mobile.html#native-payment-android) and [iOS](mobile.html#native-payment-ios).

## How it works

This is a brief overview of what Native Payment does. You can find implementation instructions with code samples in the guides for [Android](mobile.html#native-payment-android) and [iOS](mobile.html#native-payment-ios).

### Merchant registration

You need to sign up with Bambora to get an API token in order to use `Native Payment`. Please send an email to [sales.ecom@bambora.com](mailto:sales.ecom@bambora.com) if you want to sign up.

### Setup and authentication

Initially, the SDK connects to the SDK backend and sends in an API token. Based on that API token, the SDK backend identifies and authorizes the SDK. The SDK then registers itself with the SDK backend. After these steps, credit card registration and payment functionality is enabled in the app.

### Registering Credit cards

The user needs to register his/her credit card in the app in order to make a purchase. 

Credit card registration can be done in two ways:

* Through a secure and fully native credit card form that is displayed directly in the app. This option has the best user experience and is fully customizable.

* Through a secure web-based form, which we refer to as a Hosted Payment Page (HPP). The Native Payment SDK allows for customization of the areas surrounding the registration form and also slight customization of the form itself.

After a credit card has been registered using either of the above methods, a credit card token is returned to the Native Payment SDK. This token can then be used to make payments.

The SDK supports multiple credit card registrations.

### Payments

When a valid credit card that contains sufficient funds has been registered through the SDK, payments can be made.

This is done by making a call to the SDK backend that includes the amount, currency and credit card token.

**Note**: The amount should be expressed in cents (or equivalent). For example, to make a payment of 10 EUR you would write the amount as `amount=1000; currency='EUR'`, for 100 SEK you would write `amount=10000; currency='SEK'`, etc.

When an SDK payment is successful, the payment amount becomes reserved in the customer's bank account. It is then up to you as a merchant to capture/withdraw the payment from the customer's bank account (which can be done either through the merchant backend interface or by making an API integration with the Native Payment backend).

## License

The Native Payment SDK is available under the [MIT license](https://opensource.org/licenses/MIT).

## Contact info

We welcome questions and feedback - you can reach us by sending an e-mail to [native.support@bambora.com](mailto:native.support@bambora.com)
