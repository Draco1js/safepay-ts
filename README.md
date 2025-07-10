# @dhaba/safepay-ts

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *@dhaba/safepay-ts* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=@dhaba/safepay-ts&utm_campaign=typescript"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/dhaba/safepay-api). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Safepay: Safepay is a regulated payments service provider that enables developers to orchestrate money movement between customers and businesses with ease and speed. The Safepay API makes it simple for businesses and financial platforms to create payment sessions, manage subscriptions, issue invoices and exchange value by sending and receiving money. Our API is based upon REST principles, returns JSON responses, and uses standard HTTP response codes.

Safepay offers two environments to developers - `production` and `sandbox` . Any transaction performed in our `sandbox` environment will not have any financial impact. We also provide test credentials for payment instruments that can be used while integrating.

To begin integrating, we recommend you sign up for our sandbox account - its free to do so and will give you access to all of Safepay's APIs. Once you've completed your integration, please reach out to a member of our team who will guide you on how to create a production account and complete our onboarding process.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [@dhaba/safepay-ts](#dhabasafepay-ts)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add @dhaba/safepay-ts
```

### PNPM

```bash
pnpm add @dhaba/safepay-ts
```

### Bun

```bash
bun add @dhaba/safepay-ts
```

### Yarn

```bash
yarn add @dhaba/safepay-ts zod

# Note that Yarn does not install peer dependencies automatically. You will need
# to install zod as shown above.
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.


### Model Context Protocol (MCP) Server

This SDK is also an installable MCP server where the various SDK methods are
exposed as tools that can be invoked by AI applications.

> Node.js v20 or greater is required to run the MCP server from npm.

<details>
<summary>Claude installation steps</summary>

Add the following server definition to your `claude_desktop_config.json` file:

```json
{
  "mcpServers": {
    "Safepay": {
      "command": "npx",
      "args": [
        "-y", "--package", "@dhaba/safepay-ts",
        "--",
        "mcp", "start"
      ]
    }
  }
}
```

</details>

<details>
<summary>Cursor installation steps</summary>

Create a `.cursor/mcp.json` file in your project root with the following content:

```json
{
  "mcpServers": {
    "Safepay": {
      "command": "npx",
      "args": [
        "-y", "--package", "@dhaba/safepay-ts",
        "--",
        "mcp", "start"
      ]
    }
  }
}
```

</details>

You can also run MCP servers as a standalone binary with no additional dependencies. You must pull these binaries from available Github releases:

```bash
curl -L -o mcp-server \
    https://github.com/{org}/{repo}/releases/download/{tag}/mcp-server-bun-darwin-arm64 && \
chmod +x mcp-server
```

If the repo is a private repo you must add your Github PAT to download a release `-H "Authorization: Bearer {GITHUB_PAT}"`.


```json
{
  "mcpServers": {
    "Todos": {
      "command": "./DOWNLOAD/PATH/mcp-server",
      "args": [
        "start"
      ]
    }
  }
}
```

For a full list of server arguments, run:

```sh
npx -y --package @dhaba/safepay-ts -- mcp start --help
```
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.company.login();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [addresses](docs/sdks/addresses/README.md)

* [create](docs/sdks/addresses/README.md#create) - Create Address

### [apiKeys](docs/sdks/apikeys/README.md)

* [create](docs/sdks/apikeys/README.md#create) - Create API Key

### [apiSettings](docs/sdks/apisettings/README.md)

* [getApiKey](docs/sdks/apisettings/README.md#getapikey) - Find Api Key
* [updateKey](docs/sdks/apisettings/README.md#updatekey) - Update Api Key

### [auth](docs/sdks/auth/README.md)

* [createMerchantJwt](docs/sdks/auth/README.md#createmerchantjwt) - Create Merchant JWT
* [login](docs/sdks/auth/README.md#login) - Create Shopper JWT Using Password

### [clientPlans](docs/sdks/clientplans/README.md)

* [deleteById](docs/sdks/clientplans/README.md#deletebyid) - Archive Plan

### [clientSubscriptions](docs/sdks/clientsubscriptions/README.md)

* [update](docs/sdks/clientsubscriptions/README.md#update) - Update Subscription
* [resume](docs/sdks/clientsubscriptions/README.md#resume) - Resume Subscription

### [clientTransactions](docs/sdks/clienttransactions/README.md)

* [search](docs/sdks/clienttransactions/README.md#search) - Search Transactions
* [findByTransactionId](docs/sdks/clienttransactions/README.md#findbytransactionid) - Find Transaction

### [company](docs/sdks/company/README.md)

* [login](docs/sdks/company/README.md#login) - Login Company

### [customers](docs/sdks/customers/README.md)

* [create](docs/sdks/customers/README.md#create) - Create Customer
* [list](docs/sdks/customers/README.md#list) - List Customers
* [update](docs/sdks/customers/README.md#update) - Update Customer
* [get](docs/sdks/customers/README.md#get) - Find Customer
* [delete](docs/sdks/customers/README.md#delete) - Delete Customer
* [getPaymentMethod](docs/sdks/customers/README.md#getpaymentmethod) - Find Payment Method
* [listPaymentMethods](docs/sdks/customers/README.md#listpaymentmethods) - List Payment Methods

### [invoices](docs/sdks/invoices/README.md)

* [createQuickLink](docs/sdks/invoices/README.md#createquicklink) - Create

### [links](docs/sdks/links/README.md)

* [get](docs/sdks/links/README.md#get) - Find

### [meta](docs/sdks/meta/README.md)

* [listCountries](docs/sdks/meta/README.md#listcountries) - Countries
* [getCountry](docs/sdks/meta/README.md#getcountry) - Country

### [orderPayments](docs/sdks/orderpayments/README.md)

* [create](docs/sdks/orderpayments/README.md#create) - Payment
* [resetTracking](docs/sdks/orderpayments/README.md#resettracking) - Reset

### [passport](docs/sdks/passport/README.md)

* [generateToken](docs/sdks/passport/README.md#generatetoken) - Generate Time-Based Token

### [payments](docs/sdks/payments/README.md)

* [generateCaptureContext](docs/sdks/payments/README.md#generatecapturecontext) - Generate Capture Context
* [processToken](docs/sdks/payments/README.md#processtoken) - Process Transient Token
* [authenticate](docs/sdks/payments/README.md#authenticate) - Payer Authentication Setup
* [enroll](docs/sdks/payments/README.md#enroll) - Enrollment
* [capture](docs/sdks/payments/README.md#capture) - Capture
* [addMetadata](docs/sdks/payments/README.md#addmetadata) - Add Metadata
* [reverse](docs/sdks/payments/README.md#reverse) - Reverse
* [refund](docs/sdks/payments/README.md#refund) - Refund
* [void](docs/sdks/payments/README.md#void) - Void
* [fetch](docs/sdks/payments/README.md#fetch) - Fetch Payment
* [search](docs/sdks/payments/README.md#search) - Search Payments

### [plans](docs/sdks/plans/README.md)

* [create](docs/sdks/plans/README.md#create) - Create Plan
* [get](docs/sdks/plans/README.md#get) - Find Plan
* [update](docs/sdks/plans/README.md#update) - Update Plan
* [search](docs/sdks/plans/README.md#search) - Search Plans

### [quickLinks](docs/sdks/quicklinks/README.md)

* [create](docs/sdks/quicklinks/README.md#create) - Create Quick Link
* [search](docs/sdks/quicklinks/README.md#search) - Search Quick Links
* [get](docs/sdks/quicklinks/README.md#get) - Find Quick Link
* [update](docs/sdks/quicklinks/README.md#update) - Update Quick Link
* [delete](docs/sdks/quicklinks/README.md#delete) - Delete Quick Link


### [shoppers](docs/sdks/shoppers/README.md)

* [createSafepay](docs/sdks/shoppers/README.md#createsafepay) - Create Safepay Shopper

### [subscriptions](docs/sdks/subscriptions/README.md)

* [get](docs/sdks/subscriptions/README.md#get) - Find Subscription
* [search](docs/sdks/subscriptions/README.md#search) - Search Subscriptions
* [cancel](docs/sdks/subscriptions/README.md#cancel) - Cancel Subscription

### [transactions](docs/sdks/transactions/README.md)

* [refund](docs/sdks/transactions/README.md#refund) - Refund Transaction

### [userAddresses](docs/sdks/useraddresses/README.md)

* [updateById](docs/sdks/useraddresses/README.md#updatebyid) - Update Address
* [findById](docs/sdks/useraddresses/README.md#findbyid) - Find Address

### [userCustomers](docs/sdks/usercustomers/README.md)

* [deletePaymentMethod](docs/sdks/usercustomers/README.md#deletepaymentmethod) - Delete Payment Method

### [users](docs/sdks/users/README.md)

* [createGuestJwt](docs/sdks/users/README.md#createguestjwt) - Create Guest JWT
* [findSafepayShopper](docs/sdks/users/README.md#findsafepayshopper) - Find Safepay Shopper
* [exists](docs/sdks/users/README.md#exists) - Safepay Shopper Exists

### [userWallets](docs/sdks/userwallets/README.md)

* [listPaymentMethods](docs/sdks/userwallets/README.md#listpaymentmethods) - List Payment Methods

### [wallets](docs/sdks/wallets/README.md)

* [deletePaymentMethod](docs/sdks/wallets/README.md#deletepaymentmethod) - Delete Payment Method

### [webhooks](docs/sdks/webhooks/README.md)

* [test](docs/sdks/webhooks/README.md#test) - Test Webhook

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`addressesCreate`](docs/sdks/addresses/README.md#create) - Create Address
- [`apiKeysCreate`](docs/sdks/apikeys/README.md#create) - Create API Key
- [`apiSettingsGetApiKey`](docs/sdks/apisettings/README.md#getapikey) - Find Api Key
- [`apiSettingsUpdateKey`](docs/sdks/apisettings/README.md#updatekey) - Update Api Key
- [`authCreateMerchantJwt`](docs/sdks/auth/README.md#createmerchantjwt) - Create Merchant JWT
- [`authLogin`](docs/sdks/auth/README.md#login) - Create Shopper JWT Using Password
- [`clientPlansDeleteById`](docs/sdks/clientplans/README.md#deletebyid) - Archive Plan
- [`clientSubscriptionsResume`](docs/sdks/clientsubscriptions/README.md#resume) - Resume Subscription
- [`clientSubscriptionsUpdate`](docs/sdks/clientsubscriptions/README.md#update) - Update Subscription
- [`clientTransactionsFindByTransactionId`](docs/sdks/clienttransactions/README.md#findbytransactionid) - Find Transaction
- [`clientTransactionsSearch`](docs/sdks/clienttransactions/README.md#search) - Search Transactions
- [`companyLogin`](docs/sdks/company/README.md#login) - Login Company
- [`customersCreate`](docs/sdks/customers/README.md#create) - Create Customer
- [`customersDelete`](docs/sdks/customers/README.md#delete) - Delete Customer
- [`customersGet`](docs/sdks/customers/README.md#get) - Find Customer
- [`customersGetPaymentMethod`](docs/sdks/customers/README.md#getpaymentmethod) - Find Payment Method
- [`customersList`](docs/sdks/customers/README.md#list) - List Customers
- [`customersListPaymentMethods`](docs/sdks/customers/README.md#listpaymentmethods) - List Payment Methods
- [`customersUpdate`](docs/sdks/customers/README.md#update) - Update Customer
- [`invoicesCreateQuickLink`](docs/sdks/invoices/README.md#createquicklink) - Create
- [`linksGet`](docs/sdks/links/README.md#get) - Find
- [`metaGetCountry`](docs/sdks/meta/README.md#getcountry) - Country
- [`metaListCountries`](docs/sdks/meta/README.md#listcountries) - Countries
- [`orderPaymentsCreate`](docs/sdks/orderpayments/README.md#create) - Payment
- [`orderPaymentsResetTracking`](docs/sdks/orderpayments/README.md#resettracking) - Reset
- [`passportGenerateToken`](docs/sdks/passport/README.md#generatetoken) - Generate Time-Based Token
- [`paymentsAddMetadata`](docs/sdks/payments/README.md#addmetadata) - Add Metadata
- [`paymentsAuthenticate`](docs/sdks/payments/README.md#authenticate) - Payer Authentication Setup
- [`paymentsCapture`](docs/sdks/payments/README.md#capture) - Capture
- [`paymentsEnroll`](docs/sdks/payments/README.md#enroll) - Enrollment
- [`paymentsFetch`](docs/sdks/payments/README.md#fetch) - Fetch Payment
- [`paymentsGenerateCaptureContext`](docs/sdks/payments/README.md#generatecapturecontext) - Generate Capture Context
- [`paymentsProcessToken`](docs/sdks/payments/README.md#processtoken) - Process Transient Token
- [`paymentsRefund`](docs/sdks/payments/README.md#refund) - Refund
- [`paymentsReverse`](docs/sdks/payments/README.md#reverse) - Reverse
- [`paymentsSearch`](docs/sdks/payments/README.md#search) - Search Payments
- [`paymentsVoid`](docs/sdks/payments/README.md#void) - Void
- [`plansCreate`](docs/sdks/plans/README.md#create) - Create Plan
- [`plansGet`](docs/sdks/plans/README.md#get) - Find Plan
- [`plansSearch`](docs/sdks/plans/README.md#search) - Search Plans
- [`plansUpdate`](docs/sdks/plans/README.md#update) - Update Plan
- [`quickLinksCreate`](docs/sdks/quicklinks/README.md#create) - Create Quick Link
- [`quickLinksDelete`](docs/sdks/quicklinks/README.md#delete) - Delete Quick Link
- [`quickLinksGet`](docs/sdks/quicklinks/README.md#get) - Find Quick Link
- [`quickLinksSearch`](docs/sdks/quicklinks/README.md#search) - Search Quick Links
- [`quickLinksUpdate`](docs/sdks/quicklinks/README.md#update) - Update Quick Link
- [`shoppersCreateSafepay`](docs/sdks/shoppers/README.md#createsafepay) - Create Safepay Shopper
- [`subscriptionsCancel`](docs/sdks/subscriptions/README.md#cancel) - Cancel Subscription
- [`subscriptionsGet`](docs/sdks/subscriptions/README.md#get) - Find Subscription
- [`subscriptionsSearch`](docs/sdks/subscriptions/README.md#search) - Search Subscriptions
- [`transactionsRefund`](docs/sdks/transactions/README.md#refund) - Refund Transaction
- [`userAddressesFindById`](docs/sdks/useraddresses/README.md#findbyid) - Find Address
- [`userAddressesUpdateById`](docs/sdks/useraddresses/README.md#updatebyid) - Update Address
- [`userCustomersDeletePaymentMethod`](docs/sdks/usercustomers/README.md#deletepaymentmethod) - Delete Payment Method
- [`usersCreateGuestJwt`](docs/sdks/users/README.md#createguestjwt) - Create Guest JWT
- [`usersExists`](docs/sdks/users/README.md#exists) - Safepay Shopper Exists
- [`usersFindSafepayShopper`](docs/sdks/users/README.md#findsafepayshopper) - Find Safepay Shopper
- [`userWalletsListPaymentMethods`](docs/sdks/userwallets/README.md#listpaymentmethods) - List Payment Methods
- [`walletsDeletePaymentMethod`](docs/sdks/wallets/README.md#deletepaymentmethod) - Delete Payment Method
- [`webhooksTest`](docs/sdks/webhooks/README.md#test) - Test Webhook

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.company.login({
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
});

async function run() {
  const result = await safepay.company.login();

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`SafepayError`](./src/models/errors/safepayerror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Safepay } from "@dhaba/safepay-ts";
import * as errors from "@dhaba/safepay-ts/models/errors";

const safepay = new Safepay();

async function run() {
  try {
    const result = await safepay.auth.createMerchantJwt();

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.SafepayError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (
        error instanceof errors.PostAuthV1CompanyAuthenticateUnauthorizedError
      ) {
        console.log(error.data$.data); // any
        console.log(error.data$.status); // operations.PostAuthV1CompanyAuthenticateUnauthorizedStatus
      }
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`SafepayError`](./src/models/errors/safepayerror.ts): The base class for HTTP error responses.

<details><summary>Less common errors (106)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`SafepayError`](./src/models/errors/safepayerror.ts)**:
* [`PostAuthV2UserLoginBadRequestError`](./src/models/errors/postauthv2userloginbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserV2ExistsBadRequestError`](./src/models/errors/getuserv2existsbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostClientApiSettingsV1BadRequestError`](./src/models/errors/postclientapisettingsv1badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostUserCustomersV1BadRequestError`](./src/models/errors/postusercustomersv1badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1BadRequestError`](./src/models/errors/getusercustomersv1badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaBadRequestError`](./src/models/errors/putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aabadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67BadRequestError`](./src/models/errors/getusercustomersv1cus11db365b4d86494bacca79d6e09efa67badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52BadRequestError`](./src/models/errors/deleteusercustomersv1cus17febb02b2cd4cf8b2997a447530ef52badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89BadRequestError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletBadRequestError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89BadRequestError`](./src/models/errors/deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostUserAddressV2BadRequestError`](./src/models/errors/postuseraddressv2badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00BadRequestError`](./src/models/errors/putuseraddressv2address5ce54f87a8234da689907b26d048ce00badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00BadRequestError`](./src/models/errors/getuseraddressv2address5ce54f87a8234da689907b26d048ce00badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3BadRequestError`](./src/models/errors/postorderpaymentsv3badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PutOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920beBadRequestError`](./src/models/errors/putorderpaymentsv3trackaefeaefec21a4678ab1e181bfe2920bebadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dBadRequestError`](./src/models/errors/postorderpaymentsv3track7233ed61fe5048368a84c5e17ae90f4dbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06MetadataBadRequestError`](./src/models/errors/postorderpaymentsv3trackaa38d5b7a3a245c5bed8586b0bae8d06metadatabadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalBadRequestError`](./src/models/errors/postorderpaymentsv3track9d765b77608f46bc84d25f4392753ca3reversalbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26RefundBadRequestError`](./src/models/errors/postorderpaymentsv3track70fdbb06bbf744e1b50a672d9f1d8b26refundbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7VoidBadRequestError`](./src/models/errors/postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7voidbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostClientHooksV2TestBadRequestError`](./src/models/errors/postclienthooksv2testbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostClientPlansV1BadRequestError`](./src/models/errors/postclientplansv1badrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`GetClientPlansV1SearchBadRequestError`](./src/models/errors/getclientplansv1searchbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 60 methods.*
* [`PostAuthV1CompanyAuthenticateUnauthorizedError`](./src/models/errors/postauthv1companyauthenticateunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostAuthV2UserLoginUnauthorizedError`](./src/models/errors/postauthv2userloginunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserV2UnauthorizedError`](./src/models/errors/getuserv2unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostClientApiSettingsV1UnauthorizedError`](./src/models/errors/postclientapisettingsv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientApiSettingsV1UnauthorizedError`](./src/models/errors/getclientapisettingsv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutClientApiSettingsV1UnauthorizedError`](./src/models/errors/putclientapisettingsv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostClientPassportV1TokenUnauthorizedError`](./src/models/errors/postclientpassportv1tokenunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostUserCustomersV1UnauthorizedError`](./src/models/errors/postusercustomersv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1UnauthorizedError`](./src/models/errors/getusercustomersv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaUnauthorizedError`](./src/models/errors/putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aaunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67UnauthorizedError`](./src/models/errors/getusercustomersv1cus11db365b4d86494bacca79d6e09efa67unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52UnauthorizedError`](./src/models/errors/deleteusercustomersv1cus17febb02b2cd4cf8b2997a447530ef52unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89UnauthorizedError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletUnauthorizedError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89UnauthorizedError`](./src/models/errors/deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostUserAddressV2UnauthorizedError`](./src/models/errors/postuseraddressv2unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00UnauthorizedError`](./src/models/errors/putuseraddressv2address5ce54f87a8234da689907b26d048ce00unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00UnauthorizedError`](./src/models/errors/getuseraddressv2address5ce54f87a8234da689907b26d048ce00unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6UnauthorizedError`](./src/models/errors/postorderpaymentsv3tracka6f9b00c8a254cbf95f9cd6bc440eca6unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalUnauthorizedError`](./src/models/errors/postorderpaymentsv3track9d765b77608f46bc84d25f4392753ca3reversalunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbcUnauthorizedError`](./src/models/errors/getreporterapiv1paymentstrackf865abdd3a61484280001cffa38f1fbcunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostClientHooksV2TestUnauthorizedError`](./src/models/errors/postclienthooksv2testunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostClientPlansV1UnauthorizedError`](./src/models/errors/postclientplansv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError`](./src/models/errors/getclientplansv1pland4869a7800364d6697bd6afeb5282bcdunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError`](./src/models/errors/putclientplansv1pland4869a7800364d6697bd6afeb5282bcdunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientPlansV1SearchUnauthorizedError`](./src/models/errors/getclientplansv1searchunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`DeleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError`](./src/models/errors/deleteclientplansv1pland4869a7800364d6697bd6afeb5282bcdunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541UnauthorizedError`](./src/models/errors/getclientsubscriptionsv1subc841ea40613c41a389847cb11f66d541unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientSubscriptionsV1SearchUnauthorizedError`](./src/models/errors/getclientsubscriptionsv1searchunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3UnauthorizedError`](./src/models/errors/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionUnauthorizedError`](./src/models/errors/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientTransactionsV1SearchUnauthorizedError`](./src/models/errors/getclienttransactionsv1searchunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1UnauthorizedError`](./src/models/errors/getclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundUnauthorizedError`](./src/models/errors/postclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1refundunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PostInvoiceQuickLinksV1UnauthorizedError`](./src/models/errors/postinvoicequicklinksv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetInvoiceQuickLinksV1UnauthorizedError`](./src/models/errors/getinvoicequicklinksv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cUnauthorizedError`](./src/models/errors/putinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`DeleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cUnauthorizedError`](./src/models/errors/deleteinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cunauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserWalletsV1UnauthorizedError`](./src/models/errors/getuserwalletsv1unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`DeleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448UnauthorizedError`](./src/models/errors/deleteuserwalletsv1inst8ed5e401ab7b442c8473dee137827448unauthorizederror.ts): 401. Status code `401`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89ForbiddenError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89forbiddenerror.ts): 403. Status code `403`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89ForbiddenError`](./src/models/errors/deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89forbiddenerror.ts): 403. Status code `403`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dForbiddenError`](./src/models/errors/postorderpaymentsv3track7233ed61fe5048368a84c5e17ae90f4dforbiddenerror.ts): 403. Status code `403`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44ForbiddenError`](./src/models/errors/postorderpaymentsv3trackdccdef16008e4fae81cc1b7d81bf6c44forbiddenerror.ts): 403. Status code `403`. Applicable to 1 of 60 methods.*
* [`PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaNotFoundError`](./src/models/errors/putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aanotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67NotFoundError`](./src/models/errors/getusercustomersv1cus11db365b4d86494bacca79d6e09efa67notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52NotFoundError`](./src/models/errors/deleteusercustomersv1cus17febb02b2cd4cf8b2997a447530ef52notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89NotFoundError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletNotFoundError`](./src/models/errors/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89NotFoundError`](./src/models/errors/deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00NotFoundError`](./src/models/errors/putuseraddressv2address5ce54f87a8234da689907b26d048ce00notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00NotFoundError`](./src/models/errors/getuseraddressv2address5ce54f87a8234da689907b26d048ce00notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3NotFoundError`](./src/models/errors/postorderpaymentsv3notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError`](./src/models/errors/getclientplansv1pland4869a7800364d6697bd6afeb5282bcdnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError`](./src/models/errors/putclientplansv1pland4869a7800364d6697bd6afeb5282bcdnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`DeleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError`](./src/models/errors/deleteclientplansv1pland4869a7800364d6697bd6afeb5282bcdnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541NotFoundError`](./src/models/errors/getclientsubscriptionsv1subc841ea40613c41a389847cb11f66d541notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3NotFoundError`](./src/models/errors/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionNotFoundError`](./src/models/errors/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1NotFoundError`](./src/models/errors/getclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundNotFoundError`](./src/models/errors/postclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1refundnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`GetInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cNotFoundError`](./src/models/errors/getinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cnotfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`DeleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448NotFoundError`](./src/models/errors/deleteuserwalletsv1inst8ed5e401ab7b442c8473dee137827448notfounderror.ts): 404. Status code `404`. Applicable to 1 of 60 methods.*
* [`NotAcceptableError`](./src/models/errors/notacceptableerror.ts): 406. Status code `406`. Applicable to 1 of 60 methods.*
* [`PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundConflictError`](./src/models/errors/postclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1refundconflicterror.ts): 409. Status code `409`. Applicable to 1 of 60 methods.*
* [`PostUserV2ConflictError`](./src/models/errors/postuserv2conflicterror.ts): 409. Status code `409`. Applicable to 1 of 60 methods.*
* [`PostAuthV1CompanyAuthenticateExpectationFailedError`](./src/models/errors/postauthv1companyauthenticateexpectationfailederror.ts): 417. Status code `417`. Applicable to 1 of 60 methods.*
* [`PostUserV1GuestExpectationFailedError`](./src/models/errors/postuserv1guestexpectationfailederror.ts): 417. Status code `417`. Applicable to 1 of 60 methods.*
* [`PostInvoiceQuickLinksV1ExpectationFailedError`](./src/models/errors/postinvoicequicklinksv1expectationfailederror.ts): 417. Status code `417`. Applicable to 1 of 60 methods.*
* [`GetInvoiceQuickLinksV1ExpectationFailedError`](./src/models/errors/getinvoicequicklinksv1expectationfailederror.ts): 417. Status code `417`. Applicable to 1 of 60 methods.*
* [`PostOrderPaymentsV3InternalServerError`](./src/models/errors/postorderpaymentsv3internalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`PostClientPlansV1InternalServerError`](./src/models/errors/postclientplansv1internalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`PostClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2CancelInternalServerError`](./src/models/errors/postclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b2cancelinternalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionInternalServerError`](./src/models/errors/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptioninternalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cInternalServerError`](./src/models/errors/putinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cinternalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`DeleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cInternalServerError`](./src/models/errors/deleteinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cinternalservererror.ts): 500. Status code `500`. Applicable to 1 of 60 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `serverIdx: number` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| #   | Server                         | Variables                 | Description |
| --- | ------------------------------ | ------------------------- | ----------- |
| 0   | `https://{baseUrl}{auth-port}` | `baseUrl`<br/>`auth-port` |             |
| 1   | `https://{sandbox-base-url}`   | `sandbox-base-url`        |             |

If the selected server has variables, you may override its default values through the additional parameters made available in the SDK constructor:

| Variable           | Parameter                | Default                             | Description |
| ------------------ | ------------------------ | ----------------------------------- | ----------- |
| `baseUrl`          | `baseUrl: string`        | `"https://api.safepay.com"`         |             |
| `auth-port`        | `authPort: string`       | `"/auth"`                           |             |
| `sandbox-base-url` | `sandboxBaseUrl: string` | `"https://api.sandbox.safepay.com"` |             |

#### Example

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay({
  baseUrl: "https://glaring-granny.org/",
  authPort: "<value>",
});

async function run() {
  const result = await safepay.company.login();

  console.log(result);
}

run();

```

### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay({
  serverURL: "https://https://api.sandbox.safepay.com",
});

async function run() {
  const result = await safepay.company.login();

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { Safepay } from "@dhaba/safepay-ts";
import { HTTPClient } from "@dhaba/safepay-ts/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Safepay({ httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const sdk = new Safepay({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `SAFEPAY_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=@dhaba/safepay-ts&utm_campaign=typescript)
