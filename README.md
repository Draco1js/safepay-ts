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
  const result = await safepay.auth.createMerchantJwt({});

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

### [clientTransactions](docs/sdks/clienttransactions/README.md)

* [search](docs/sdks/clienttransactions/README.md#search) - Search Transactions

### [company](docs/sdks/company/README.md)

* [login](docs/sdks/company/README.md#login) - Login Company

### [customers](docs/sdks/customers/README.md)

* [create](docs/sdks/customers/README.md#create) - Create Customer
* [list](docs/sdks/customers/README.md#list) - List Customers

### [invoices](docs/sdks/invoices/README.md)

* [createQuickLink](docs/sdks/invoices/README.md#createquicklink) - Create

### [meta](docs/sdks/meta/README.md)

* [getCountry](docs/sdks/meta/README.md#getcountry) - Country
* [listCountries](docs/sdks/meta/README.md#listcountries) - Countries

### [orderPayments](docs/sdks/orderpayments/README.md)

* [create](docs/sdks/orderpayments/README.md#create) - Payment

### [passport](docs/sdks/passport/README.md)

* [generateToken](docs/sdks/passport/README.md#generatetoken) - Generate Time-Based Token

### [payments](docs/sdks/payments/README.md)

* [search](docs/sdks/payments/README.md#search) - Search Payments

### [plans](docs/sdks/plans/README.md)

* [create](docs/sdks/plans/README.md#create) - Create Plan
* [search](docs/sdks/plans/README.md#search) - Search Plans

### [quickLinks](docs/sdks/quicklinks/README.md)

* [create](docs/sdks/quicklinks/README.md#create) - Create Quick Link
* [search](docs/sdks/quicklinks/README.md#search) - Search Quick Links


### [shoppers](docs/sdks/shoppers/README.md)

* [createSafepay](docs/sdks/shoppers/README.md#createsafepay) - Create Safepay Shopper

### [subscriptions](docs/sdks/subscriptions/README.md)

* [search](docs/sdks/subscriptions/README.md#search) - Search Subscriptions

### [users](docs/sdks/users/README.md)

* [createGuestJwt](docs/sdks/users/README.md#createguestjwt) - Create Guest JWT
* [exists](docs/sdks/users/README.md#exists) - Safepay Shopper Exists
* [findSafepayShopper](docs/sdks/users/README.md#findsafepayshopper) - Find Safepay Shopper

### [userWallets](docs/sdks/userwallets/README.md)

* [listPaymentMethods](docs/sdks/userwallets/README.md#listpaymentmethods) - List Payment Methods

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
- [`clientTransactionsSearch`](docs/sdks/clienttransactions/README.md#search) - Search Transactions
- [`companyLogin`](docs/sdks/company/README.md#login) - Login Company
- [`customersCreate`](docs/sdks/customers/README.md#create) - Create Customer
- [`customersList`](docs/sdks/customers/README.md#list) - List Customers
- [`invoicesCreateQuickLink`](docs/sdks/invoices/README.md#createquicklink) - Create
- [`metaGetCountry`](docs/sdks/meta/README.md#getcountry) - Country
- [`metaListCountries`](docs/sdks/meta/README.md#listcountries) - Countries
- [`orderPaymentsCreate`](docs/sdks/orderpayments/README.md#create) - Payment
- [`passportGenerateToken`](docs/sdks/passport/README.md#generatetoken) - Generate Time-Based Token
- [`paymentsSearch`](docs/sdks/payments/README.md#search) - Search Payments
- [`plansCreate`](docs/sdks/plans/README.md#create) - Create Plan
- [`plansSearch`](docs/sdks/plans/README.md#search) - Search Plans
- [`quickLinksCreate`](docs/sdks/quicklinks/README.md#create) - Create Quick Link
- [`quickLinksSearch`](docs/sdks/quicklinks/README.md#search) - Search Quick Links
- [`shoppersCreateSafepay`](docs/sdks/shoppers/README.md#createsafepay) - Create Safepay Shopper
- [`subscriptionsSearch`](docs/sdks/subscriptions/README.md#search) - Search Subscriptions
- [`usersCreateGuestJwt`](docs/sdks/users/README.md#createguestjwt) - Create Guest JWT
- [`usersExists`](docs/sdks/users/README.md#exists) - Safepay Shopper Exists
- [`usersFindSafepayShopper`](docs/sdks/users/README.md#findsafepayshopper) - Find Safepay Shopper
- [`userWalletsListPaymentMethods`](docs/sdks/userwallets/README.md#listpaymentmethods) - List Payment Methods
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
  const result = await safepay.auth.createMerchantJwt({}, {
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
  const result = await safepay.auth.createMerchantJwt({});

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
    const result = await safepay.auth.createMerchantJwt({});

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
        console.log(error.data$.status); // models.Status
      }
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`SafepayError`](./src/models/errors/safepayerror.ts): The base class for HTTP error responses.

<details><summary>Less common errors (19)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`SafepayError`](./src/models/errors/safepayerror.ts)**:
* [`PostAuthV1CompanyAuthenticateUnauthorizedError`](./src/models/errors/postauthv1companyauthenticateunauthorizederror.ts): 401. Status code `401`. Applicable to 16 of 27 methods.*
* [`PostClientApiSettingsV1BadRequestError`](./src/models/errors/postclientapisettingsv1badrequesterror.ts): 400. Status code `400`. Applicable to 5 of 27 methods.*
* [`ErrorT`](./src/models/errors/errort.ts): Applicable to 5 of 27 methods.*
* [`ExpectationFailedError`](./src/models/errors/expectationfailederror.ts): 417. Status code `417`. Applicable to 4 of 27 methods.*
* [`PostClientPlansV1BadRequestError`](./src/models/errors/postclientplansv1badrequesterror.ts): 400. Status code `400`. Applicable to 2 of 27 methods.*
* [`PostAuthV2UserLoginUnauthorizedError`](./src/models/errors/postauthv2userloginunauthorizederror.ts): 401. Status code `401`. Applicable to 2 of 27 methods.*
* [`PostAuthV2UserLoginBadRequestError`](./src/models/errors/postauthv2userloginbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 27 methods.*
* [`PostClientHooksV2TestBadRequestError`](./src/models/errors/postclienthooksv2testbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 27 methods.*
* [`GetUserV2ExistsBadRequestError`](./src/models/errors/getuserv2existsbadrequesterror.ts): 400. Status code `400`. Applicable to 1 of 27 methods.*
* [`NotFoundError`](./src/models/errors/notfounderror.ts): 404. Status code `404`. Applicable to 1 of 27 methods.*
* [`ConflictError`](./src/models/errors/conflicterror.ts): 409. Status code `409`. Applicable to 1 of 27 methods.*
* [`PostClientPlansV1InternalServerError`](./src/models/errors/postclientplansv1internalservererror.ts): 500. Status code `500`. Applicable to 1 of 27 methods.*
* [`PostOrderPaymentsV3InternalServerError`](./src/models/errors/postorderpaymentsv3internalservererror.ts): 500. Status code `500`. Applicable to 1 of 27 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `serverIdx: number` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| #   | Server                            | Description            |
| --- | --------------------------------- | ---------------------- |
| 0   | `https://api.sandbox.safepay.com` | Sandbox environment    |
| 1   | `https://api.safepay.com`         | Production environment |

#### Example

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay({
  serverIdx: 1,
});

async function run() {
  const result = await safepay.auth.createMerchantJwt({});

  console.log(result);
}

run();

```

### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay({
  serverURL: "https://api.safepay.com",
});

async function run() {
  const result = await safepay.auth.createMerchantJwt({});

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
