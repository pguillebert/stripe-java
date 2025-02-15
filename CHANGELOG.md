# Changelog

## 5.26.0 - 2017-12-18
* [#436](https://github.com/stripe/stripe-java/pull/436) Fix bug where `options` were not being plumbed through in an account delete method
* [#436](https://github.com/stripe/stripe-java/pull/436) Add the proper set of overloads for account reject method

## 5.25.0 - 2017-12-06
* [#432](https://github.com/stripe/stripe-java/pull/432) Make charge on `Dispute` expandable

## 5.24.0 - 2017-11-28
* [#421](https://github.com/stripe/stripe-java/pull/421) Expose response objects 
* [#427](https://github.com/stripe/stripe-java/pull/427) Add `automatic` property on `Payout` model

## 5.23.1 - 2017-11-09
* [#423](https://github.com/stripe/stripe-java/pull/423) Fix JSON encoding for expandable fields by adding customer encoder

## 5.23.0 - 2017-10-31
* [#419](https://github.com/stripe/stripe-java/pull/419) Support for exchange rate APIs

## 5.22.1 - 2017-10-27
* [#418](https://github.com/stripe/stripe-java/pull/418) Move build and release system from Maven to Gradle

## 5.22.0 - 2017-10-27
* [#417](https://github.com/stripe/stripe-java/pull/417) Support for listing source transactions

## 5.21.0 - 2017-10-09
* [#410](https://github.com/stripe/stripe-java/pull/410) Rename "verification" to "code verification" for sources (should have been unused up to this point)
* [#412](https://github.com/stripe/stripe-java/pull/412) Add support for detaching sources from customers
* Note that some minor versions (5.11 through 5.20) were accidentally skipped for this release. I'm leaving as is to minimize churn, but please don't be alarmed!

## 5.10.0 - 2017-10-04
* Add `failure_reason` field to the source redirect flow model

## 5.9.1 - 2017-10-03
* No longer clobber global value of DNS cache TTL if it has not been set

## 5.9.0 - 2017-09-25
* Support Java 9 (just involves upgrading a few Maven plugins)

## 5.8.0 - 2017-08-31
* Add support for all OAuth actions

## 5.7.1 - 2017-07-11
* Force UTF-8 encoding for webhook signature verification

## 5.7.0 - 2017-07-11
* Use standard library comparison for webhook signature verification

## 5.6.0 - 2017-06-27
* `pay` on invoice can now take parameters

## 5.5.0 - 2017-06-23
* Add support for alternate statement descriptors on charge

## 5.4.0 - 2017-06-19
* Add support for ephemeral keys

## 5.3.0 - 2017-06-14
* Add missing expandable fields on every model

## 5.2.0 - 2017-06-09
* Support for expandable sources in balance transactions

## 5.1.0 - 2017-06-07
* Add `account` field to the event model

## 5.0.0 - 2017-05-31
* Clarify tolerance parameter for webhook signatures is in seconds
* Support expanded request in `Event` model (now with idempotency key)

## 4.9.1 - 2017-05-30
* This release should have been 5.0.0, see notes for that

## 4.9.0 - 2017-05-25
* This release should have been 5.0.0, see notes for that

## 4.8.0 - 2017-05-25
* Add support for account login links

## 4.7.0 - 2017-05-02
* Add `three_d_secure` accessors to `Card` model

## 4.6.0 - 2017-04-28
* Support for checking webhook signatures

## 4.5.0 - 2017-04-28
* Make connect and read timeouts configurable (see README for details)

## 4.4.0 - 2017-04-24
* Add payout properties to `Account` model

## 4.3.0 - 2017-04-12
* Add support for `available_payout_methods` to `Card` model

## 4.2.0 - 2017-04-06
* Add support for payouts; see: https://stripe.com/docs/upgrades#2017-04-06

## 4.1.0 - 2017-04-04
* Make `rule` under `ChargeOutcome` expandable

## 4.0.0 - 2017-03-13
* Dispute on charge becomes expandable field (not expanded by default)
* Charge on order becomes expandable field (not expanded by default)
* Customer on order becomes expandable field (not expanded by default)
* Add missing fields on order: `amountReturned`, `returns`, and `upstreamId`
* Fix type of `OrderReturnCollection` (now actually an order return)

## 3.11.0 - 2017-02-22
* Add new parameters for invoices and subscriptions

## 3.10.2 - 2017-02-21
* Add missing API resources to object deserializer

## 3.10.1 - 2017-02-21
* This release was inadvertently empty. See 3.10.2 for changes.

## 3.10.0 - 2017-02-13
* Deprecated sourced transfers under balance transactions

## 3.9.0 - 2017-02-02
* Add variant of account `delete` that doesn't require parameters

## 3.8.0 - 2017-01-23
* Add `ChargeOutcomeRule` to `ChargeOutcome`

## 3.7.0 - 2017-01-06
* Add `getObject`/`setObject` to a number of models where it was missing
* Add `toJson` method to `StripeObject`

## 3.6.0 - 2017-01-03
* Add non-public `network_reason_code` to `Dispute` model

## 3.5.0 - 2016-12-08
* Add expandable Charge to Invoice

## 3.3.0 - 2016-11-22
* Add retrieve method for 3-D Secure resources

## 3.2.0 - 2016-10-18
* Add `risk_level` attribute to `ChargeOutcome` model

## 3.1.0 - 2016-10-18
* Support for 403 status codes (permission denied)

## 3.0.0 - 2016-10-17
* Change representations of money (e.g. "amounts" or "balances") from `Integer` to `Long`

## 2.10.2 - 2016-10-13
* Fix NullPointerException in SourceDeserializer for bitcoin receivers, and refactor tests.

## 2.10.1 - 2016-10-06
* Fix bug where the Transfer transactions method wasn't using requestCollection

## 2.10.0 - 2016-09-16
* Add support for Apple Pay domains

## 2.9.0 - 2016-09-07
* Add `description`, `iin`, and `issuer` attributes to `Card` model

## 2.8.0 - 2016-08-05
* Add `Source` model (prototype)

## 2.7.0 - 2016-07-12
* Add `ThreeDSecure` model for 3-D secure payments

## 2.6.1 - 2016-06-13
* Fix serialization of `businessURL` and `supportURL` in `Account` model

## 2.6.0 - 2016-05-25
* Add support for returning Relay orders

## 2.5.1 - 2016-05-23
* Give all collection classes access to auto-paginating helpers that work beyond first page

## 2.5.0 - 2016-05-04
* Add `retrieve`, `update`, `create`, `all`, and `delete` methods to the Subscription class

## 2.4.0 - 2016-04-21
* Add many missing fields to many models (see #285 for details)

## 2.3.0 - 2016-04-18
* Add source types to `Money` model under the `Balance` model

## 2.2.0 - 2016-04-12
* Add `Outcome` to the `Charge` model

## 2.1.0 - 2016-04-12
* Deprecate `getUser` and `setUser` on `ApplicationFee`
* Deprecate `getCard` and `setCard` on `Charge`
* Deprecate `getAccount` and `setAccount` on `Transfer`
* Deprecate `getOtherTransfers` and `setOtherTransfers` on `Transfer`
* Deprecate `getSummary` and `setSummary` on `Transfer`

## 2.0.0 - 2016-04-08
* Change `getBusinessUrl` to `getBusinessURL` in `Account` model
* Change `getSupportUrl` to `getSupportURL` in `Account` model
* Change `getUrl` to `getURL` in `Product` model
* Change `setUrl` to `setURL` in `Product` model
* Change `getUrl` to `getURL` in `StripeCollection` model
* Change `setUrl` to `setURL` in `StripeCollection` model
* Remove previously-deprecated `getUrl` in `StripeCollectionAPIResource` model
* Change `getUrl` to `getURL` in `StripeCollectionInterface`

## 1.48.0 - 2016-03-29
* Add accessors for `default_currency` to `CountrySpec` model

## 1.47.0 - 2016-03-21
* Allow request params and options to be overridden for `autoPagingIterable`

## 1.46.0 - 2016-03-15
* Expose creating bank accounts on customer
* Add `reject` action on account

## 1.45.0 - 2016-02-18
* Add `CountrySpec` model for looking up country payment information

## 1.44.0 - 2016-02-11
* Add `businessTaxIdProvided` to `LegalEntity`

## 1.43.0 - 2016-01-26
* Add support for deleting Relay SKUs and products

## 1.42.0 - 2016-01-21
* Add `details_code` to `LegalEntity`
* Add `disabled_reason` to `Verification`

## 1.41.1 - 2016-01-15
* Fix serialization bug in `LegalEntity`'s `ssnLast4Provided`

## 1.41.0 - 2016-01-13
* Add lots of missing fields to Account, Event, and Refund

## 1.40.1 - 2016-01-07
* Fix casting of newer objects to *typed* models

## 1.40.0 - 2015-12-03
* Add missing `ShippingDetails` to `Customer` model

## 1.39.0 - 2015-12-01
* Add a verification routine for external accounts

## 1.38.1 - 2015-11-30
* Fix bug when using lazy-paging collection across multiple pages

## 1.38.0 - 2015-10-27
* Add pagination through the use of calling `AutoPagingIterable()` for a page
* Fix bug where arrays were not being properly encoded when sent to the API
* Fix bug where setting a `List` to `null` wasn't encoding to an empty string (which is required to unset an array)

## 1.37.1 - 2015-10-07
* Bugfix `setTransfer` on `Reversal`

## 1.37.0 - 2015-09-14
* Products, SKUs, and Orders -- https://stripe.com/relay

## 1.36.0 - 2015-09-11
* Add support for new rate limiting responses.

## 1.35.0 - 2015-08-31
* Add `bankAccount` to `Token`

## 1.34.0 - 2015-08-17
* Added `retrieve`, `all`, `update`, `create` methods to `Refund`

## 1.33.0 - 2015-08-03
* Added `retrieve`, `all`, `update` and `close` methods to `Dispute`
* Added `delete` method to managed `Account`s

## 1.32.1 - 2015-07-24
* Added `account` to `ApplicationFee`.

## 1.32.0 - 2015-07-06
* Added `getRequestId` method to `StripeException`.

## 1.31.0 - 2015-06-01
* `ConcretePaymentSource` and the `PaymentSource` interface have been combined into one `ExternalAccount` class
* `PaymentSourceCollection` was renamed `ExternalAccountCollection`
* `Account` now supports `getExternalAccounts`, which allows both `BankAccount` and `Card` attachment.
* `BankAccount`s can now be deleted from `Customer`s (private beta feature) and `Account`s

## 1.30.0 - 2015-05-28
* Add decline_code, charge to CardException

## 1.29.0 - 2015-05-21
* Added tax percent field to subscriptions
* Added tax and tax percent fields to invoices

## 1.28.0 - 2015-05-08
* Added support for Alipay accounts
* Added default source when type is unknown
* Added support dynamicLast4 on Card for Apple Pay integrations

## 1.27.1 - 2015-03-30
* Charge objects now support status

## 1.27.0 - 2015-02-19
* Added support for transfer reversals
* Added support for account creation/updating/retrieval by ID
* Customer objects now support currency
* Added STRIPE-ACCOUNT header options in RequestOptions

## 1.26.0 - 2015-02-19
* Added Update and Delete for Bitcoin Receivers
* Support new API version (2015-02-18) by providing source type properties
  on Customer and Charge in addition to card type properties

## 1.25.1 - 2015-01-23
* Test of new stripe-java release process.

## 1.25.0 - 2015-01-21
* Support making bitcoin charges through BitcoinReceiver source object

## 1.24.1 - 2015-01-05
* Support for fraud reporting methods was added

## 1.24.0 - 2014-12-18
* The ability to post multipart/form-data was added
* Requests can now hit different base endpoints, by passing in `apiBase` when creating URLs
* Support for the file upload endpoints was added. Documentation is available at https://stripe.com/docs/api#file_uploads
* Support for fraud reporting (marking charges as safe or fraudulent) was added

## 1.23.0 - 2014-12-08
* Java 1.5 support dropped. We strongly suggest using newer versions of Java due to runtime, VM, language, and syntax improvements
* Dispute Evidence has been updated to reflect the new version of Dispute evidence format introduced as part of api version 2014-12-08. See https://stripe.com/docs/upgrades#2014-12-08 for details

## 1.22.0 - 2014-12-03
* Convention is to call methods with a RequestOptions object, instead of an API Key directly
* Support setting the stripe version on a per-request level, via the RequestOptions object
* Add shipping and address to the charge object

### Deprecation

* All requests that involve passing the apiKey directly to the method are now deprecated in favor of using RequestOptions instead. Use RequestOptions as follows:

    RequestOptions.builder().setApiKey(apiKey).build()

## 1.21.0 - 2014-11-14
* Created Charge.receiptEmail field
* Created Charge.receiptNumber field

## 1.20.0 - 2014-11-06
* Change chargeEnabled to chargesEnabled
* Change transferEnabled to transfersEnabled
* Add id, currency, status, fingerprint, and defaultForCurrency to BankAccount

## 1.19.1 - 2014-10-02
* Add back explict autoboxing for Google App Engine reflected HTTP method (fixes issue #106)

## 1.19.0 - 2014-09-30
* Add statementDescription field to transfer
* A few non-breaking general cleanups

## 1.18.0 - 2014-08-25
* Added isChargeRefundable and balanceTransactions to Dispute https://stripe.com/docs/upgrades#2014-08-20

## 1.17.0 - 2014-08-19
* Added metadata to Coupons

## 1.16.0 - 2014-07-26
* Application Fee refunds now a list instead of array

## 1.15.1 - 2014-06-25
* Added brand and funding to Card

## 1.15.0 - 2014-06-17
* Added metadata to Refund
* Added metadata to Dispute
* Fixed incorrect return types for certain collection resources

## 1.14.1 - 2014-06-04
* Added metadata to Subscription

## 1.14.0 - 2014-05-28
* Add support for canceling transfers

## 1.13.1 - 2014-05-23
* Fix bug with retrieving lines of upcoming invoice.

## 1.13.0 - 2014-05-21
* Support cards for recipients.

## 1.12.0 - 2014-04-09
* Test SSL certificate against blacklist

## 1.11.0 - 2014-04-07
* Upgrade customer, charge, and coupon collections to new pagination style
* Add missing fields to Account object

## 1.10.0 - 2014-03-28
* Support for newstyle pagination API (https://groups.google.com/a/lists.stripe.com/forum/#!topic/api-announce/29sLxmICA9E)

## 1.9.0 - 2014-03-17
* Support for dynamic statement descriptions
* Preserve original 'threaqd null ids through to requests' behavior

## 1.8.0 - 2014-03-12
* Upgrade Google GSON to 2.2.4
* URL-encode object ids (fixes #62)

## 1.7.2 - 2014-02-27
* Add 'valid' field to coupon

## 1.7.1 - 2014-01-31
* Fix Subscription cancel method call
* Miscellaneous field fixups
    * Discount on Subscription is an expanded Discount, not string
    * Add missing application_fee_percent field on Subscription
    * Add missing application_fee field on Invoice

## 1.7.0 - 2014-01-29
* Add support for multiple subscriptions per customer

## 1.6.5 - 2014-01-22
* Fixed url to refund application fees (fixes #60)
* DRY'd some of the application fee urls

## 1.6.4 - 2014-01-16
* Added metadata to InvoiceItem and InvoiceLineItem (fixes #59)

## 1.6.3 - 2014-01-13
* Support overriding base url (for testing) (user request)
* Add default currency to Account object (fixes #46)
* Add metadata to plan object (thanks, desirable-objects)
* Remove plan from Customer (fixes #42)
* Style improvements (see #30) (thanks, steve-nester-uk)

## 1.6.2 - 2014-01-08
* Fix return type of Coupon.getRedeemBy

## 1.6.1 - 2013-12-02
* Add ApplicationFee API resource

## 1.5.1 - 2013-10-17
* Added field transfer_enabled to Account API object (thanks, kurguzov)

## 1.5.0 - 2013-10-01
* Add support for metadata API

## 1.4.2 - 2013-09-18
* Add support for closing disputes

## 1.4.1 - 2013-09-04
* Fix return type of CustomerCardCollection.retrieve

## 1.4.0 - 2013-09-03
* Tweak card create to align it with docs

## 1.3.2 - 2013-08-30
* Add missing `retrieve` method to `BalanceTransaction`
* Add missing fields to `BalanceTransaction`
    * `id`
    * `fee`
    * `fee_details`
    * `description`
* Add `id` field to `Subscription`

## 1.3.1 - 2013-08-21
* Patch release with missing field, added tests

## 1.3.0 - 2013-08-19
* Add BalanceTransaction API resource
* Add Refund resource
* Resource updates
    * Remove `fee`, `feeDetails` from Transfer and Charge resources
    * Add `balanceTransaction` to Transfer, Charge, and Dispute resources
    * Add `refunds` to Charge resource

## 1.2.8 - 2013-08-12
* Add support for unsetting attributes by updating with a null value. Setting properties to a blank string is now an error.

## 1.2.7 - 2013-07-31
* Enable createCard() to use a token

## 1.2.6 - 2013-07-30
* Add 'createCard' to Customer
* Update card collections bindings
* Parse card objects when receiving customer.card.created events

## 1.2.5 - 2013-07-15
* Add support for new cards API.
    * You will probably need to upgrade the Stripe API version on your account to 2013-07-05 or explicitly specify an API version with com.stripe.Stripe.apiVersion when you switch to this release of the bindings. More information about the relevant changes can be found at https://stripe.com/docs/upgrades#2013-07-05 and http://bit.ly/13miHM8
* Add a StripeRawJsonObject type for deserializing webhook events we don't recognize
* Add a Money class for representing account balances in individual currencies

## 1.2.4 - 2013-06-21
* Add more Balance API resource, and add to deserializer.

## 1.2.3 - 2013-05-7
* Rename BankAccount property `valid` to `validated`

## 1.2.2 - 2013-04-25
* Add more objects to Deserializer

## 1.2.1 - 2013-04-20
* Fix TransferTransaction fee retrieval

## 1.2.0 - 2013-04-11
* Allow Transfers to be creatable
* Add new Recipient resource

## 1.1.18 - 2013-03-19
* Add support for charge capture.

## 1.1.17 - 2013-02-18
* Add ability to deserialize account-related events.
* Add user ID to Event object.

## 1.1.16 - 2013-02-15
* Fix off-by-one error in deserializing events (github issue #27).

## 1.1.15 - 2013-02-01
* List all checked exceptions throws by methods.
* Add support for plan interval count.

## 1.1.14 - 2013-01-15
* Add support for setting Stripe API version override.

## 1.1.13 - 2012-12-29
* Add address_city to card
* Upgrade Google GSON to 2.2.2

## 1.1.12 - 2012-12-24
* Add option to provide custom URL handler

## 1.1.11 - 2012-11-17
* Explict cast to javax.net.ssl.HttpsURLConnection to prevent issues with user imports

## 1.1.10 - 2012-11-15
* Add currency to Invoice resource
* Add amountOff and currency to Coupon resource

## 1.1.9 - 2012-11-08
* Add new Dispute resource
* Add support for updating charge disputes

## 1.1.8 - 2012-10-30
* Add support for creating invoices
* Add support for new Invoice.lines return format

## 1.1.7 - 2012-10-15
* Add quantity to Subscription

## 1.1.6 - 2012-10-15
* Add Fee API resource, add feeDetails to Charge API resource.

## 1.1.5 - 2012-09-26
* Pass query parameters to DELETE-based methods when using Google App Engine (github issue #17)

## 1.1.4 - 2012-08-31
* Add update and pay methods for Invoice resource

## 1.1.3 - 2012-08-15
* Add the Account API resource

## 1.1.2 - 2012-08-06
* Allow specification of API key at the API call level

## 1.1.1 - 2012-05-24
* Use String.length() == 0 instead of String.isEmpty() for compatibility with JDK 1.5 (needed for Android 2.2)

## 1.1.0 - 2012-05-16
* Change type of cvcCheck, addressZipCheck, and addressLine1Check attributes on com.stripe.model.Card; values of those fields will be "pass", "fail", "unchecked", or null (github issue #11)
* Remove code and percentOff attributes from com.stripe.model.Discount. Stripe never returned these values for Discount objects, so they would previously always be null
* Add missing fields to Charge, Coupon, Discount, Event, and Invoice models (github issue #12)
* Include parameters passed to any object's delete method in actual API requests (github issue #10)
* Add new deleteDiscount method to com.stripe.model.Customer
* Switch from using HTTP Basic auth to Bearer auth. (Note: Stripe will support Basic auth for the indefinite future, but recommends Bearer auth when possible going forward)
* Numerous test suite improvements
