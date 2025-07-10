# Safepay SDK

## Overview

Safepay: Safepay is a regulated payments service provider that enables developers to orchestrate money movement between customers and businesses with ease and speed. The Safepay API makes it simple for businesses and financial platforms to create payment sessions, manage subscriptions, issue invoices and exchange value by sending and receiving money. Our API is based upon REST principles, returns JSON responses, and uses standard HTTP response codes.

Safepay offers two environments to developers - `production` and `sandbox` . Any transaction performed in our `sandbox` environment will not have any financial impact. We also provide test credentials for payment instruments that can be used while integrating.

To begin integrating, we recommend you sign up for our sandbox account - its free to do so and will give you access to all of Safepay's APIs. Once you've completed your integration, please reach out to a member of our team who will guide you on how to create a production account and complete our onboarding process.

### Available Operations

* [postV1CompanyLogin](#postv1companylogin) - Login Company
* [postAuthV1CompanyAuthenticate](#postauthv1companyauthenticate) - Create Merchant JWT
* [postAuthV2UserLogin](#postauthv2userlogin) - Create Shopper JWT Using Password
* [postUserV1Guest](#postuserv1guest) - Create Guest JWT
* [postClientApiSettingsV1](#postclientapisettingsv1) - Create API Key
* [getClientApiSettingsV1](#getclientapisettingsv1) - Find Api Key
* [putClientApiSettingsV1](#putclientapisettingsv1) - Update Api Key
* [postClientPassportV1Token](#postclientpassportv1token) - Generate Time-Based Token
* [postUserCustomersV1](#postusercustomersv1) - Create Customer
* [getUserCustomersV1](#getusercustomersv1) - List Customers
* [putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa](#putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aa) - Update Customer
* [getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67](#getusercustomersv1cus11db365b4d86494bacca79d6e09efa67) - Find Customer
* [deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52](#deleteusercustomersv1cus17febb02b2cd4cf8b2997a447530ef52) - Delete Customer
* [getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89](#getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89) - Find Payment Method
* [deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89](#deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89) - Delete Payment Method
* [getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet](#getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawallet) - List Payment Methods
* [postUserAddressV2](#postuseraddressv2) - Create Address
* [putUserAddressV2Address5ce54f87A8234da689907b26d048ce00](#putuseraddressv2address5ce54f87a8234da689907b26d048ce00) - Update Address
* [getUserAddressV2Address5ce54f87A8234da689907b26d048ce00](#getuseraddressv2address5ce54f87a8234da689907b26d048ce00) - Find Address
* [postOrderPaymentsV3](#postorderpaymentsv3) - Payment
* [postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d](#postorderpaymentsv3track7233ed61fe5048368a84c5e17ae90f4d) - Generate Capture Context
* [postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44](#postorderpaymentsv3trackdccdef16008e4fae81cc1b7d81bf6c44) - Process Transient Token
* [postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6](#postorderpaymentsv3tracka6f9b00c8a254cbf95f9cd6bc440eca6) - Payer Authentication Setup
* [postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372](#postorderpaymentsv3trackf3adbae6640247fe948bee82244ac372) - Enrollment
* [postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7](#postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7) - Capture
* [putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be](#putorderpaymentsv3trackaefeaefec21a4678ab1e181bfe2920be) - Reset
* [postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata](#postorderpaymentsv3trackaa38d5b7a3a245c5bed8586b0bae8d06metadata) - Add Metadata
* [postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal](#postorderpaymentsv3track9d765b77608f46bc84d25f4392753ca3reversal) - Reverse
* [postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund](#postorderpaymentsv3track70fdbb06bbf744e1b50a672d9f1d8b26refund) - Refund
* [postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void](#postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7void) - Void
* [getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc](#getreporterapiv1paymentstrackf865abdd3a61484280001cffa38f1fbc) - Fetch Payment
* [getReporterApiV1Payments](#getreporterapiv1payments) - Search Payments
* [getUserMetaV2Countries](#getusermetav2countries) - Countries
* [getUserMetaV2Country](#getusermetav2country) - Country
* [postClientHooksV2Test](#postclienthooksv2test) - Test Webhook
* [postClientPlansV1](#postclientplansv1) - Create Plan
* [getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd](#getclientplansv1pland4869a7800364d6697bd6afeb5282bcd) - Find Plan
* [putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd](#putclientplansv1pland4869a7800364d6697bd6afeb5282bcd) - Update Plan
* [deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd](#deleteclientplansv1pland4869a7800364d6697bd6afeb5282bcd) - Archive Plan
* [getClientPlansV1Search](#getclientplansv1search) - Search Plans
* [getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541](#getclientsubscriptionsv1subc841ea40613c41a389847cb11f66d541) - Find Subscription
* [getClientSubscriptionsV1Search](#getclientsubscriptionsv1search) - Search Subscriptions
* [putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3](#putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3) - Update Subscription
* [putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption](#putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumption) - Resume Subscription
* [postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel](#postclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b2cancel) - Cancel Subscription
* [getClientTransactionsV1Search](#getclienttransactionsv1search) - Search Transactions
* [getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1](#getclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1) - Find Transaction
* [postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund](#postclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1refund) - Refund Transaction
* [postInvoiceQuickLinksV2](#postinvoicequicklinksv2) - Create
* [getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31](#getinvoicequicklinksv2link291208afef954b7db171aaaa16998d31) - Find
* [postInvoiceQuickLinksV1](#postinvoicequicklinksv1) - Create Quick Link
* [getInvoiceQuickLinksV1](#getinvoicequicklinksv1) - Search Quick Links
* [getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c](#getinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890c) - Find Quick Link
* [putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c](#putinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890c) - Update Quick Link
* [deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c](#deleteinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890c) - Delete Quick Link
* [postUserV2](#postuserv2) - Create Safepay Shopper
* [getUserV2](#getuserv2) - Find Safepay Shopper
* [getUserV2Exists](#getuserv2exists) - Safepay Shopper Exists
* [getUserWalletsV1](#getuserwalletsv1) - List Payment Methods
* [deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448](#deleteuserwalletsv1inst8ed5e401ab7b442c8473dee137827448) - Delete Payment Method

## postV1CompanyLogin

Login Company

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postV1CompanyLogin();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postV1CompanyLogin } from "@dhaba/safepay-ts/funcs/postV1CompanyLogin.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postV1CompanyLogin(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postV1CompanyLogin failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostV1CompanyLoginResponse](../../models/operations/postv1companyloginresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## postAuthV1CompanyAuthenticate

Create Merchant JWT

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postAuthV1CompanyAuthenticate();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postAuthV1CompanyAuthenticate } from "@dhaba/safepay-ts/funcs/postAuthV1CompanyAuthenticate.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postAuthV1CompanyAuthenticate(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postAuthV1CompanyAuthenticate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostAuthV1CompanyAuthenticateRequest](../../models/operations/postauthv1companyauthenticaterequest.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostAuthV1CompanyAuthenticateResponse](../../models/operations/postauthv1companyauthenticateresponse.md)\>**

### Errors

| Error Type                                                 | Status Code                                                | Content Type                                               |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError      | 401                                                        | application/json                                           |
| errors.PostAuthV1CompanyAuthenticateExpectationFailedError | 417                                                        | application/json                                           |
| errors.SafepayDefaultError                                 | 4XX, 5XX                                                   | \*/\*                                                      |

## postAuthV2UserLogin

Create Shopper JWT Using Password

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postAuthV2UserLogin();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postAuthV2UserLogin } from "@dhaba/safepay-ts/funcs/postAuthV2UserLogin.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postAuthV2UserLogin(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postAuthV2UserLogin failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostAuthV2UserLoginRequest](../../models/operations/postauthv2userloginrequest.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostAuthV2UserLoginResponse](../../models/operations/postauthv2userloginresponse.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.PostAuthV2UserLoginBadRequestError   | 400                                         | application/json                            |
| errors.PostAuthV2UserLoginUnauthorizedError | 401                                         | application/json                            |
| errors.SafepayDefaultError                  | 4XX, 5XX                                    | \*/\*                                       |

## postUserV1Guest

Create Guest JWT

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postUserV1Guest();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postUserV1Guest } from "@dhaba/safepay-ts/funcs/postUserV1Guest.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postUserV1Guest(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postUserV1Guest failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostUserV1GuestRequest](../../models/operations/postuserv1guestrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostUserV1GuestResponse](../../models/operations/postuserv1guestresponse.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.PostUserV1GuestExpectationFailedError | 417                                          | application/json                             |
| errors.SafepayDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## postClientApiSettingsV1

Create API Key

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientApiSettingsV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientApiSettingsV1 } from "@dhaba/safepay-ts/funcs/postClientApiSettingsV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientApiSettingsV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientApiSettingsV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostClientApiSettingsV1Response](../../models/operations/postclientapisettingsv1response.md)\>**

### Errors

| Error Type                                      | Status Code                                     | Content Type                                    |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| errors.PostClientApiSettingsV1BadRequestError   | 400                                             | application/json                                |
| errors.PostClientApiSettingsV1UnauthorizedError | 401                                             | application/json                                |
| errors.SafepayDefaultError                      | 4XX, 5XX                                        | \*/\*                                           |

## getClientApiSettingsV1

Find Api Key

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientApiSettingsV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientApiSettingsV1 } from "@dhaba/safepay-ts/funcs/getClientApiSettingsV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientApiSettingsV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientApiSettingsV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientApiSettingsV1Response](../../models/operations/getclientapisettingsv1response.md)\>**

### Errors

| Error Type                                     | Status Code                                    | Content Type                                   |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| errors.GetClientApiSettingsV1UnauthorizedError | 401                                            | application/json                               |
| errors.SafepayDefaultError                     | 4XX, 5XX                                       | \*/\*                                          |

## putClientApiSettingsV1

Update Api Key

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putClientApiSettingsV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putClientApiSettingsV1 } from "@dhaba/safepay-ts/funcs/putClientApiSettingsV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putClientApiSettingsV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putClientApiSettingsV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutClientApiSettingsV1Response](../../models/operations/putclientapisettingsv1response.md)\>**

### Errors

| Error Type                                     | Status Code                                    | Content Type                                   |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| errors.PutClientApiSettingsV1UnauthorizedError | 401                                            | application/json                               |
| errors.SafepayDefaultError                     | 4XX, 5XX                                       | \*/\*                                          |

## postClientPassportV1Token

Generate Time-Based Token

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientPassportV1Token();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientPassportV1Token } from "@dhaba/safepay-ts/funcs/postClientPassportV1Token.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientPassportV1Token(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientPassportV1Token failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostClientPassportV1TokenResponse](../../models/operations/postclientpassportv1tokenresponse.md)\>**

### Errors

| Error Type                                        | Status Code                                       | Content Type                                      |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| errors.PostClientPassportV1TokenUnauthorizedError | 401                                               | application/json                                  |
| errors.SafepayDefaultError                        | 4XX, 5XX                                          | \*/\*                                             |

## postUserCustomersV1

Create Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postUserCustomersV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postUserCustomersV1 } from "@dhaba/safepay-ts/funcs/postUserCustomersV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postUserCustomersV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postUserCustomersV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostUserCustomersV1Request](../../models/operations/postusercustomersv1request.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostUserCustomersV1Response](../../models/operations/postusercustomersv1response.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.PostUserCustomersV1BadRequestError   | 400                                         | application/json                            |
| errors.PostUserCustomersV1UnauthorizedError | 401                                         | application/json                            |
| errors.SafepayDefaultError                  | 4XX, 5XX                                    | \*/\*                                       |

## getUserCustomersV1

List Customers

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserCustomersV1({
    limit: 20,
    page: 1,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserCustomersV1 } from "@dhaba/safepay-ts/funcs/getUserCustomersV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserCustomersV1(safepay, {
    limit: 20,
    page: 1,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserCustomersV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUserCustomersV1Request](../../models/operations/getusercustomersv1request.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserCustomersV1Response](../../models/operations/getusercustomersv1response.md)\>**

### Errors

| Error Type                                 | Status Code                                | Content Type                               |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| errors.GetUserCustomersV1BadRequestError   | 400                                        | application/json                           |
| errors.GetUserCustomersV1UnauthorizedError | 401                                        | application/json                           |
| errors.SafepayDefaultError                 | 4XX, 5XX                                   | \*/\*                                      |

## putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa

Update Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa } from "@dhaba/safepay-ts/funcs/putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aa failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaRequest](../../models/operations/putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aarequest.md)             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaResponse](../../models/operations/putusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aaresponse.md)\>**

### Errors

| Error Type                                                                    | Status Code                                                                   | Content Type                                                                  |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| errors.PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaBadRequestError   | 400                                                                           | application/json                                                              |
| errors.PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaUnauthorizedError | 401                                                                           | application/json                                                              |
| errors.PutUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaNotFoundError     | 404                                                                           | application/json                                                              |
| errors.SafepayDefaultError                                                    | 4XX, 5XX                                                                      | \*/\*                                                                         |

## getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67

Find Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67 } from "@dhaba/safepay-ts/funcs/getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67Response](../../models/operations/getusercustomersv1cus11db365b4d86494bacca79d6e09efa67response.md)\>**

### Errors

| Error Type                                                                    | Status Code                                                                   | Content Type                                                                  |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| errors.GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67BadRequestError   | 400                                                                           | application/json                                                              |
| errors.GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67UnauthorizedError | 401                                                                           | application/json                                                              |
| errors.GetUserCustomersV1Cus11db365b4d86494bAcca79d6e09efa67NotFoundError     | 404                                                                           | application/json                                                              |
| errors.SafepayDefaultError                                                    | 4XX, 5XX                                                                      | \*/\*                                                                         |

## deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52

Delete Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52 } from "@dhaba/safepay-ts/funcs/deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("deleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52Response](../../models/operations/deleteusercustomersv1cus17febb02b2cd4cf8b2997a447530ef52response.md)\>**

### Errors

| Error Type                                                                       | Status Code                                                                      | Content Type                                                                     |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| errors.DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52BadRequestError   | 400                                                                              | application/json                                                                 |
| errors.DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52UnauthorizedError | 401                                                                              | application/json                                                                 |
| errors.DeleteUserCustomersV1Cus17febb02B2cd4cf8B2997a447530ef52NotFoundError     | 404                                                                              | application/json                                                                 |
| errors.SafepayDefaultError                                                       | 4XX, 5XX                                                                         | \*/\*                                                                            |

## getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89

Find Payment Method

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import {
  getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89,
} from "@dhaba/safepay-ts/funcs/getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89Response](../../models/operations/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89response.md)\>**

### Errors

| Error Type                                                                                                            | Status Code                                                                                                           | Content Type                                                                                                          |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89BadRequestError   | 400                                                                                                                   | application/json                                                                                                      |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89UnauthorizedError | 401                                                                                                                   | application/json                                                                                                      |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89ForbiddenError    | 403                                                                                                                   | application/json                                                                                                      |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89NotFoundError     | 404                                                                                                                   | application/json                                                                                                      |
| errors.SafepayDefaultError                                                                                            | 4XX, 5XX                                                                                                              | \*/\*                                                                                                                 |

## deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89

Delete Payment Method

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import {
  deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89,
} from "@dhaba/safepay-ts/funcs/deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("deleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89Response](../../models/operations/deleteusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletpmbea0077422ba44ce82c53cdd1a342e89response.md)\>**

### Errors

| Error Type                                                                                                               | Status Code                                                                                                              | Content Type                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| errors.DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89BadRequestError   | 400                                                                                                                      | application/json                                                                                                         |
| errors.DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89UnauthorizedError | 401                                                                                                                      | application/json                                                                                                         |
| errors.DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89ForbiddenError    | 403                                                                                                                      | application/json                                                                                                         |
| errors.DeleteUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletPmBea0077422ba44ce82c53cdd1a342e89NotFoundError     | 404                                                                                                                      | application/json                                                                                                         |
| errors.SafepayDefaultError                                                                                               | 4XX, 5XX                                                                                                                 | \*/\*                                                                                                                    |

## getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet

List Payment Methods

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet({
    limit: 20,
    page: 1,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet } from "@dhaba/safepay-ts/funcs/getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet(safepay, {
    limit: 20,
    page: 1,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWallet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletRequest](../../models/operations/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletrequest.md) | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletResponse](../../models/operations/getusercustomersv1cus2fc20245e0f8447faf75fa651cfd54aawalletresponse.md)\>**

### Errors

| Error Type                                                                          | Status Code                                                                         | Content Type                                                                        |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletBadRequestError   | 400                                                                                 | application/json                                                                    |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletUnauthorizedError | 401                                                                                 | application/json                                                                    |
| errors.GetUserCustomersV1Cus2fc20245E0f8447fAf75Fa651cfd54aaWalletNotFoundError     | 404                                                                                 | application/json                                                                    |
| errors.SafepayDefaultError                                                          | 4XX, 5XX                                                                            | \*/\*                                                                               |

## postUserAddressV2

Create Address

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postUserAddressV2();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postUserAddressV2 } from "@dhaba/safepay-ts/funcs/postUserAddressV2.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postUserAddressV2(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postUserAddressV2 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostUserAddressV2Request](../../models/operations/postuseraddressv2request.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostUserAddressV2Response](../../models/operations/postuseraddressv2response.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.PostUserAddressV2BadRequestError   | 400                                       | application/json                          |
| errors.PostUserAddressV2UnauthorizedError | 401                                       | application/json                          |
| errors.SafepayDefaultError                | 4XX, 5XX                                  | \*/\*                                     |

## putUserAddressV2Address5ce54f87A8234da689907b26d048ce00

Update Address

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putUserAddressV2Address5ce54f87A8234da689907b26d048ce00();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putUserAddressV2Address5ce54f87A8234da689907b26d048ce00 } from "@dhaba/safepay-ts/funcs/putUserAddressV2Address5ce54f87A8234da689907b26d048ce00.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putUserAddressV2Address5ce54f87A8234da689907b26d048ce00(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putUserAddressV2Address5ce54f87A8234da689907b26d048ce00 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00Request](../../models/operations/putuseraddressv2address5ce54f87a8234da689907b26d048ce00request.md)         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00Response](../../models/operations/putuseraddressv2address5ce54f87a8234da689907b26d048ce00response.md)\>**

### Errors

| Error Type                                                                      | Status Code                                                                     | Content Type                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| errors.PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00BadRequestError   | 400                                                                             | application/json                                                                |
| errors.PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00UnauthorizedError | 401                                                                             | application/json                                                                |
| errors.PutUserAddressV2Address5ce54f87A8234da689907b26d048ce00NotFoundError     | 404                                                                             | application/json                                                                |
| errors.SafepayDefaultError                                                      | 4XX, 5XX                                                                        | \*/\*                                                                           |

## getUserAddressV2Address5ce54f87A8234da689907b26d048ce00

Find Address

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserAddressV2Address5ce54f87A8234da689907b26d048ce00();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserAddressV2Address5ce54f87A8234da689907b26d048ce00 } from "@dhaba/safepay-ts/funcs/getUserAddressV2Address5ce54f87A8234da689907b26d048ce00.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserAddressV2Address5ce54f87A8234da689907b26d048ce00(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserAddressV2Address5ce54f87A8234da689907b26d048ce00 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00Response](../../models/operations/getuseraddressv2address5ce54f87a8234da689907b26d048ce00response.md)\>**

### Errors

| Error Type                                                                      | Status Code                                                                     | Content Type                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| errors.GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00BadRequestError   | 400                                                                             | application/json                                                                |
| errors.GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00UnauthorizedError | 401                                                                             | application/json                                                                |
| errors.GetUserAddressV2Address5ce54f87A8234da689907b26d048ce00NotFoundError     | 404                                                                             | application/json                                                                |
| errors.SafepayDefaultError                                                      | 4XX, 5XX                                                                        | \*/\*                                                                           |

## postOrderPaymentsV3

Payment

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3 } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3Request](../../models/operations/postorderpaymentsv3request.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3Response](../../models/operations/postorderpaymentsv3response.md)\>**

### Errors

| Error Type                                    | Status Code                                   | Content Type                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| errors.PostOrderPaymentsV3BadRequestError     | 400                                           | application/json                              |
| errors.PostOrderPaymentsV3NotFoundError       | 404                                           | application/json                              |
| errors.PostOrderPaymentsV3InternalServerError | 500                                           | application/json                              |
| errors.SafepayDefaultError                    | 4XX, 5XX                                      | \*/\*                                         |

## postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d

Generate Capture Context

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4d failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dRequest](../../models/operations/postorderpaymentsv3track7233ed61fe5048368a84c5e17ae90f4drequest.md)       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dResponse](../../models/operations/postorderpaymentsv3track7233ed61fe5048368a84c5e17ae90f4dresponse.md)\>**

### Errors

| Error Type                                                                     | Status Code                                                                    | Content Type                                                                   |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| errors.PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dBadRequestError | 400                                                                            | application/json                                                               |
| errors.PostOrderPaymentsV3Track7233ed61Fe5048368a84C5e17ae90f4dForbiddenError  | 403                                                                            | application/json                                                               |
| errors.SafepayDefaultError                                                     | 4XX, 5XX                                                                       | \*/\*                                                                          |

## postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44

Process Transient Token

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44 } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44Request](../../models/operations/postorderpaymentsv3trackdccdef16008e4fae81cc1b7d81bf6c44request.md)       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44Response](../../models/operations/postorderpaymentsv3trackdccdef16008e4fae81cc1b7d81bf6c44response.md)\>**

### Errors

| Error Type                                                                    | Status Code                                                                   | Content Type                                                                  |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| errors.PostOrderPaymentsV3TrackDccdef16008e4fae81cc1b7d81bf6c44ForbiddenError | 403                                                                           | application/json                                                              |
| errors.SafepayDefaultError                                                    | 4XX, 5XX                                                                      | \*/\*                                                                         |

## postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6

Payer Authentication Setup

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6 } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6Request](../../models/operations/postorderpaymentsv3tracka6f9b00c8a254cbf95f9cd6bc440eca6request.md)       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6Response](../../models/operations/postorderpaymentsv3tracka6f9b00c8a254cbf95f9cd6bc440eca6response.md)\>**

### Errors

| Error Type                                                                       | Status Code                                                                      | Content Type                                                                     |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| errors.PostOrderPaymentsV3TrackA6f9b00c8a254cbf95f9Cd6bc440eca6UnauthorizedError | 401                                                                              | application/json                                                                 |
| errors.SafepayDefaultError                                                       | 4XX, 5XX                                                                         | \*/\*                                                                            |

## postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372

Enrollment

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372 } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372Request](../../models/operations/postorderpaymentsv3trackf3adbae6640247fe948bee82244ac372request.md)       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3TrackF3adbae6640247fe948bEe82244ac372Response](../../models/operations/postorderpaymentsv3trackf3adbae6640247fe948bee82244ac372response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7

Capture

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7 } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Request](../../models/operations/postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7request.md)       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Response](../../models/operations/postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be

Reset

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be } from "@dhaba/safepay-ts/funcs/putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920be failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920beResponse](../../models/operations/putorderpaymentsv3trackaefeaefec21a4678ab1e181bfe2920beresponse.md)\>**

### Errors

| Error Type                                                                    | Status Code                                                                   | Content Type                                                                  |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| errors.PutOrderPaymentsV3TrackAefeaefeC21a4678Ab1e181bfe2920beBadRequestError | 400                                                                           | application/json                                                              |
| errors.SafepayDefaultError                                                    | 4XX, 5XX                                                                      | \*/\*                                                                         |

## postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata

Add Metadata

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06Metadata failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                                | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                                | [operations.PostOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06MetadataRequest](../../models/operations/postorderpaymentsv3trackaa38d5b7a3a245c5bed8586b0bae8d06metadatarequest.md) | :heavy_check_mark:                                                                                                                                                                       | The request object to use for the request.                                                                                                                                               |
| `options`                                                                                                                                                                                | RequestOptions                                                                                                                                                                           | :heavy_minus_sign:                                                                                                                                                                       | Used to set various options for making HTTP requests.                                                                                                                                    |
| `options.fetchOptions`                                                                                                                                                                   | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                                  | :heavy_minus_sign:                                                                                                                                                                       | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.           |
| `options.retries`                                                                                                                                                                        | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                       | Enables retrying HTTP requests under certain failure conditions.                                                                                                                         |

### Response

**Promise\<[operations.PostOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06MetadataResponse](../../models/operations/postorderpaymentsv3trackaa38d5b7a3a245c5bed8586b0bae8d06metadataresponse.md)\>**

### Errors

| Error Type                                                                             | Status Code                                                                            | Content Type                                                                           |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| errors.PostOrderPaymentsV3TrackAa38d5b7A3a245c5Bed8586b0bae8d06MetadataBadRequestError | 400                                                                                    | application/json                                                                       |
| errors.SafepayDefaultError                                                             | 4XX, 5XX                                                                               | \*/\*                                                                                  |

## postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal

Reverse

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3Reversal failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                                | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                                | [operations.PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalRequest](../../models/operations/postorderpaymentsv3track9d765b77608f46bc84d25f4392753ca3reversalrequest.md) | :heavy_check_mark:                                                                                                                                                                       | The request object to use for the request.                                                                                                                                               |
| `options`                                                                                                                                                                                | RequestOptions                                                                                                                                                                           | :heavy_minus_sign:                                                                                                                                                                       | Used to set various options for making HTTP requests.                                                                                                                                    |
| `options.fetchOptions`                                                                                                                                                                   | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                                  | :heavy_minus_sign:                                                                                                                                                                       | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.           |
| `options.retries`                                                                                                                                                                        | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                       | Enables retrying HTTP requests under certain failure conditions.                                                                                                                         |

### Response

**Promise\<[operations.PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalResponse](../../models/operations/postorderpaymentsv3track9d765b77608f46bc84d25f4392753ca3reversalresponse.md)\>**

### Errors

| Error Type                                                                               | Status Code                                                                              | Content Type                                                                             |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| errors.PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalBadRequestError   | 400                                                                                      | application/json                                                                         |
| errors.PostOrderPaymentsV3Track9d765b77608f46bc84d25f4392753ca3ReversalUnauthorizedError | 401                                                                                      | application/json                                                                         |
| errors.SafepayDefaultError                                                               | 4XX, 5XX                                                                                 | \*/\*                                                                                    |

## postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund

Refund

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26Refund failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                            | Type                                                                                                                                                                                 | Required                                                                                                                                                                             | Description                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                            | [operations.PostOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26RefundRequest](../../models/operations/postorderpaymentsv3track70fdbb06bbf744e1b50a672d9f1d8b26refundrequest.md) | :heavy_check_mark:                                                                                                                                                                   | The request object to use for the request.                                                                                                                                           |
| `options`                                                                                                                                                                            | RequestOptions                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                   | Used to set various options for making HTTP requests.                                                                                                                                |
| `options.fetchOptions`                                                                                                                                                               | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                              | :heavy_minus_sign:                                                                                                                                                                   | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.       |
| `options.retries`                                                                                                                                                                    | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                        | :heavy_minus_sign:                                                                                                                                                                   | Enables retrying HTTP requests under certain failure conditions.                                                                                                                     |

### Response

**Promise\<[operations.PostOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26RefundResponse](../../models/operations/postorderpaymentsv3track70fdbb06bbf744e1b50a672d9f1d8b26refundresponse.md)\>**

### Errors

| Error Type                                                                           | Status Code                                                                          | Content Type                                                                         |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| errors.PostOrderPaymentsV3Track70fdbb06Bbf744e1B50a672d9f1d8b26RefundBadRequestError | 400                                                                                  | application/json                                                                     |
| errors.SafepayDefaultError                                                           | 4XX, 5XX                                                                             | \*/\*                                                                                |

## postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void

Void

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void } from "@dhaba/safepay-ts/funcs/postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7Void failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                        | Type                                                                                                                                                                             | Required                                                                                                                                                                         | Description                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                        | [operations.PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7VoidRequest](../../models/operations/postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7voidrequest.md) | :heavy_check_mark:                                                                                                                                                               | The request object to use for the request.                                                                                                                                       |
| `options`                                                                                                                                                                        | RequestOptions                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                               | Used to set various options for making HTTP requests.                                                                                                                            |
| `options.fetchOptions`                                                                                                                                                           | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                          | :heavy_minus_sign:                                                                                                                                                               | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.   |
| `options.retries`                                                                                                                                                                | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                               | Enables retrying HTTP requests under certain failure conditions.                                                                                                                 |

### Response

**Promise\<[operations.PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7VoidResponse](../../models/operations/postorderpaymentsv3track1a46dc7091f948928e250bb5205b69c7voidresponse.md)\>**

### Errors

| Error Type                                                                         | Status Code                                                                        | Content Type                                                                       |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| errors.PostOrderPaymentsV3Track1a46dc7091f948928e250bb5205b69c7VoidBadRequestError | 400                                                                                | application/json                                                                   |
| errors.SafepayDefaultError                                                         | 4XX, 5XX                                                                           | \*/\*                                                                              |

## getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc

Fetch Payment

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc } from "@dhaba/safepay-ts/funcs/getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbc failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbcResponse](../../models/operations/getreporterapiv1paymentstrackf865abdd3a61484280001cffa38f1fbcresponse.md)\>**

### Errors

| Error Type                                                                            | Status Code                                                                           | Content Type                                                                          |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| errors.GetReporterApiV1PaymentsTrackF865abdd3a61484280001cffa38f1fbcUnauthorizedError | 401                                                                                   | application/json                                                                      |
| errors.SafepayDefaultError                                                            | 4XX, 5XX                                                                              | \*/\*                                                                                 |

## getReporterApiV1Payments

Search Payments

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getReporterApiV1Payments({
    limit: 5,
    page: 1,
    sortBy: "created_at",
    direction: "DESC",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getReporterApiV1Payments } from "@dhaba/safepay-ts/funcs/getReporterApiV1Payments.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getReporterApiV1Payments(safepay, {
    limit: 5,
    page: 1,
    sortBy: "created_at",
    direction: "DESC",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getReporterApiV1Payments failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetReporterApiV1PaymentsRequest](../../models/operations/getreporterapiv1paymentsrequest.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetReporterApiV1PaymentsResponse](../../models/operations/getreporterapiv1paymentsresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## getUserMetaV2Countries

Countries

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserMetaV2Countries({
    lang: "en",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserMetaV2Countries } from "@dhaba/safepay-ts/funcs/getUserMetaV2Countries.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserMetaV2Countries(safepay, {
    lang: "en",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserMetaV2Countries failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUserMetaV2CountriesRequest](../../models/operations/getusermetav2countriesrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserMetaV2CountriesResponse](../../models/operations/getusermetav2countriesresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## getUserMetaV2Country

Country

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserMetaV2Country({
    cc: "AE",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserMetaV2Country } from "@dhaba/safepay-ts/funcs/getUserMetaV2Country.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserMetaV2Country(safepay, {
    cc: "AE",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserMetaV2Country failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUserMetaV2CountryRequest](../../models/operations/getusermetav2countryrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserMetaV2CountryResponse](../../models/operations/getusermetav2countryresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## postClientHooksV2Test

Test Webhook

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientHooksV2Test();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientHooksV2Test } from "@dhaba/safepay-ts/funcs/postClientHooksV2Test.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientHooksV2Test(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientHooksV2Test failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostClientHooksV2TestRequest](../../models/operations/postclienthooksv2testrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostClientHooksV2TestResponse](../../models/operations/postclienthooksv2testresponse.md)\>**

### Errors

| Error Type                                    | Status Code                                   | Content Type                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| errors.PostClientHooksV2TestBadRequestError   | 400                                           | application/json                              |
| errors.PostClientHooksV2TestUnauthorizedError | 401                                           | application/json                              |
| errors.SafepayDefaultError                    | 4XX, 5XX                                      | \*/\*                                         |

## postClientPlansV1

Create Plan

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientPlansV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientPlansV1 } from "@dhaba/safepay-ts/funcs/postClientPlansV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientPlansV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientPlansV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostClientPlansV1Request](../../models/operations/postclientplansv1request.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostClientPlansV1Response](../../models/operations/postclientplansv1response.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.PostClientPlansV1BadRequestError     | 400                                         | application/json                            |
| errors.PostClientPlansV1UnauthorizedError   | 401                                         | application/json                            |
| errors.PostClientPlansV1InternalServerError | 500                                         | application/json                            |
| errors.SafepayDefaultError                  | 4XX, 5XX                                    | \*/\*                                       |

## getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd

Find Plan

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd } from "@dhaba/safepay-ts/funcs/getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdResponse](../../models/operations/getclientplansv1pland4869a7800364d6697bd6afeb5282bcdresponse.md)\>**

### Errors

| Error Type                                                                   | Status Code                                                                  | Content Type                                                                 |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| errors.GetClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError | 401                                                                          | application/json                                                             |
| errors.GetClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError     | 404                                                                          | application/json                                                             |
| errors.SafepayDefaultError                                                   | 4XX, 5XX                                                                     | \*/\*                                                                        |

## putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd

Update Plan

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd } from "@dhaba/safepay-ts/funcs/putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdRequest](../../models/operations/putclientplansv1pland4869a7800364d6697bd6afeb5282bcdrequest.md)               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdResponse](../../models/operations/putclientplansv1pland4869a7800364d6697bd6afeb5282bcdresponse.md)\>**

### Errors

| Error Type                                                                   | Status Code                                                                  | Content Type                                                                 |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| errors.PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError | 401                                                                          | application/json                                                             |
| errors.PutClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError     | 404                                                                          | application/json                                                             |
| errors.SafepayDefaultError                                                   | 4XX, 5XX                                                                     | \*/\*                                                                        |

## deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd

Archive Plan

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd } from "@dhaba/safepay-ts/funcs/deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("deleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcd failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdResponse](../../models/operations/deleteclientplansv1pland4869a7800364d6697bd6afeb5282bcdresponse.md)\>**

### Errors

| Error Type                                                                      | Status Code                                                                     | Content Type                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| errors.DeleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdUnauthorizedError | 401                                                                             | application/json                                                                |
| errors.DeleteClientPlansV1PlanD4869a7800364d6697bd6afeb5282bcdNotFoundError     | 404                                                                             | application/json                                                                |
| errors.SafepayDefaultError                                                      | 4XX, 5XX                                                                        | \*/\*                                                                           |

## getClientPlansV1Search

Search Plans

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientPlansV1Search({
    currencies: "PKR",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientPlansV1Search } from "@dhaba/safepay-ts/funcs/getClientPlansV1Search.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientPlansV1Search(safepay, {
    currencies: "PKR",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientPlansV1Search failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetClientPlansV1SearchRequest](../../models/operations/getclientplansv1searchrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientPlansV1SearchResponse](../../models/operations/getclientplansv1searchresponse.md)\>**

### Errors

| Error Type                                     | Status Code                                    | Content Type                                   |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| errors.GetClientPlansV1SearchBadRequestError   | 400                                            | application/json                               |
| errors.GetClientPlansV1SearchUnauthorizedError | 401                                            | application/json                               |
| errors.SafepayDefaultError                     | 4XX, 5XX                                       | \*/\*                                          |

## getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541

Find Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541 } from "@dhaba/safepay-ts/funcs/getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541Response](../../models/operations/getclientsubscriptionsv1subc841ea40613c41a389847cb11f66d541response.md)\>**

### Errors

| Error Type                                                                          | Status Code                                                                         | Content Type                                                                        |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| errors.GetClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541UnauthorizedError | 401                                                                                 | application/json                                                                    |
| errors.GetClientSubscriptionsV1SubC841ea40613c41a389847cb11f66d541NotFoundError     | 404                                                                                 | application/json                                                                    |
| errors.SafepayDefaultError                                                          | 4XX, 5XX                                                                            | \*/\*                                                                               |

## getClientSubscriptionsV1Search

Search Subscriptions

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientSubscriptionsV1Search();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientSubscriptionsV1Search } from "@dhaba/safepay-ts/funcs/getClientSubscriptionsV1Search.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientSubscriptionsV1Search(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientSubscriptionsV1Search failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetClientSubscriptionsV1SearchRequest](../../models/operations/getclientsubscriptionsv1searchrequest.md)                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientSubscriptionsV1SearchResponse](../../models/operations/getclientsubscriptionsv1searchresponse.md)\>**

### Errors

| Error Type                                             | Status Code                                            | Content Type                                           |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| errors.GetClientSubscriptionsV1SearchUnauthorizedError | 401                                                    | application/json                                       |
| errors.SafepayDefaultError                             | 4XX, 5XX                                               | \*/\*                                                  |

## putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3

Update Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3 } from "@dhaba/safepay-ts/funcs/putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3Request](../../models/operations/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3request.md) | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3Response](../../models/operations/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3response.md)\>**

### Errors

| Error Type                                                                          | Status Code                                                                         | Content Type                                                                        |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| errors.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3UnauthorizedError | 401                                                                                 | application/json                                                                    |
| errors.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3NotFoundError     | 404                                                                                 | application/json                                                                    |
| errors.SafepayDefaultError                                                          | 4XX, 5XX                                                                            | \*/\*                                                                               |

## putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption

Resume Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption } from "@dhaba/safepay-ts/funcs/putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumption failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                                          | Type                                                                                                                                                                                               | Required                                                                                                                                                                                           | Description                                                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                                          | [operations.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionRequest](../../models/operations/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionrequest.md) | :heavy_check_mark:                                                                                                                                                                                 | The request object to use for the request.                                                                                                                                                         |
| `options`                                                                                                                                                                                          | RequestOptions                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                 | Used to set various options for making HTTP requests.                                                                                                                                              |
| `options.fetchOptions`                                                                                                                                                                             | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                                            | :heavy_minus_sign:                                                                                                                                                                                 | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.                     |
| `options.retries`                                                                                                                                                                                  | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                 | Enables retrying HTTP requests under certain failure conditions.                                                                                                                                   |

### Response

**Promise\<[operations.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionResponse](../../models/operations/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionresponse.md)\>**

### Errors

| Error Type                                                                                      | Status Code                                                                                     | Content Type                                                                                    |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionUnauthorizedError   | 401                                                                                             | application/json                                                                                |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionNotFoundError       | 404                                                                                             | application/json                                                                                |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionInternalServerError | 500                                                                                             | application/json                                                                                |
| errors.SafepayDefaultError                                                                      | 4XX, 5XX                                                                                        | \*/\*                                                                                           |

## postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel

Cancel Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel } from "@dhaba/safepay-ts/funcs/postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2Cancel failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                                    | Type                                                                                                                                                                                         | Required                                                                                                                                                                                     | Description                                                                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                                    | [operations.PostClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2CancelRequest](../../models/operations/postclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b2cancelrequest.md) | :heavy_check_mark:                                                                                                                                                                           | The request object to use for the request.                                                                                                                                                   |
| `options`                                                                                                                                                                                    | RequestOptions                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                           | Used to set various options for making HTTP requests.                                                                                                                                        |
| `options.fetchOptions`                                                                                                                                                                       | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                                      | :heavy_minus_sign:                                                                                                                                                                           | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.               |
| `options.retries`                                                                                                                                                                            | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                                | :heavy_minus_sign:                                                                                                                                                                           | Enables retrying HTTP requests under certain failure conditions.                                                                                                                             |

### Response

**Promise\<[operations.PostClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2CancelResponse](../../models/operations/postclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b2cancelresponse.md)\>**

### Errors

| Error Type                                                                                   | Status Code                                                                                  | Content Type                                                                                 |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| errors.NotAcceptableError                                                                    | 406                                                                                          | application/json                                                                             |
| errors.PostClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b2CancelInternalServerError | 500                                                                                          | application/json                                                                             |
| errors.SafepayDefaultError                                                                   | 4XX, 5XX                                                                                     | \*/\*                                                                                        |

## getClientTransactionsV1Search

Search Transactions

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientTransactionsV1Search();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientTransactionsV1Search } from "@dhaba/safepay-ts/funcs/getClientTransactionsV1Search.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientTransactionsV1Search(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientTransactionsV1Search failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetClientTransactionsV1SearchRequest](../../models/operations/getclienttransactionsv1searchrequest.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientTransactionsV1SearchResponse](../../models/operations/getclienttransactionsv1searchresponse.md)\>**

### Errors

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.GetClientTransactionsV1SearchUnauthorizedError | 401                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |

## getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1

Find Transaction

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1 } from "@dhaba/safepay-ts/funcs/getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Response](../../models/operations/getclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1response.md)\>**

### Errors

| Error Type                                                                         | Status Code                                                                        | Content Type                                                                       |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| errors.GetClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1UnauthorizedError | 401                                                                                | application/json                                                                   |
| errors.GetClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1NotFoundError     | 404                                                                                | application/json                                                                   |
| errors.SafepayDefaultError                                                         | 4XX, 5XX                                                                           | \*/\*                                                                              |

## postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund

Refund Transaction

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund } from "@dhaba/safepay-ts/funcs/postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1Refund failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundResponse](../../models/operations/postclienttransactionsv1txn17553398b91d41e9ae47165e194d06a1refundresponse.md)\>**

### Errors

| Error Type                                                                                | Status Code                                                                               | Content Type                                                                              |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| errors.PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundUnauthorizedError | 401                                                                                       | application/json                                                                          |
| errors.PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundNotFoundError     | 404                                                                                       | application/json                                                                          |
| errors.PostClientTransactionsV1Txn17553398B91d41e9Ae47165e194d06a1RefundConflictError     | 409                                                                                       | application/json                                                                          |
| errors.SafepayDefaultError                                                                | 4XX, 5XX                                                                                  | \*/\*                                                                                     |

## postInvoiceQuickLinksV2

Create

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  await safepay.postInvoiceQuickLinksV2();


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postInvoiceQuickLinksV2 } from "@dhaba/safepay-ts/funcs/postInvoiceQuickLinksV2.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postInvoiceQuickLinksV2(safepay);
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("postInvoiceQuickLinksV2 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostInvoiceQuickLinksV2Request](../../models/operations/postinvoicequicklinksv2request.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31

Find

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  await safepay.getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31();


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31 } from "@dhaba/safepay-ts/funcs/getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31(safepay);
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("getInvoiceQuickLinksV2Link291208afEf954b7dB171Aaaa16998d31 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |

## postInvoiceQuickLinksV1

Create Quick Link

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postInvoiceQuickLinksV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postInvoiceQuickLinksV1 } from "@dhaba/safepay-ts/funcs/postInvoiceQuickLinksV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postInvoiceQuickLinksV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postInvoiceQuickLinksV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostInvoiceQuickLinksV1Request](../../models/operations/postinvoicequicklinksv1request.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostInvoiceQuickLinksV1Response](../../models/operations/postinvoicequicklinksv1response.md)\>**

### Errors

| Error Type                                           | Status Code                                          | Content Type                                         |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| errors.PostInvoiceQuickLinksV1UnauthorizedError      | 401                                                  | application/json                                     |
| errors.PostInvoiceQuickLinksV1ExpectationFailedError | 417                                                  | application/json                                     |
| errors.SafepayDefaultError                           | 4XX, 5XX                                             | \*/\*                                                |

## getInvoiceQuickLinksV1

Search Quick Links

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getInvoiceQuickLinksV1({
    page: 1,
    limit: 10,
    workflow: "MANUAL",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getInvoiceQuickLinksV1 } from "@dhaba/safepay-ts/funcs/getInvoiceQuickLinksV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getInvoiceQuickLinksV1(safepay, {
    page: 1,
    limit: 10,
    workflow: "MANUAL",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getInvoiceQuickLinksV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetInvoiceQuickLinksV1Request](../../models/operations/getinvoicequicklinksv1request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetInvoiceQuickLinksV1Response](../../models/operations/getinvoicequicklinksv1response.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.GetInvoiceQuickLinksV1UnauthorizedError      | 401                                                 | application/json                                    |
| errors.GetInvoiceQuickLinksV1ExpectationFailedError | 417                                                 | application/json                                    |
| errors.SafepayDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |

## getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c

Find Quick Link

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c } from "@dhaba/safepay-ts/funcs/getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cResponse](../../models/operations/getinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cresponse.md)\>**

### Errors

| Error Type                                                                     | Status Code                                                                    | Content Type                                                                   |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| errors.GetInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cNotFoundError | 404                                                                            | application/json                                                               |
| errors.SafepayDefaultError                                                     | 4XX, 5XX                                                                       | \*/\*                                                                          |

## putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c

Update Quick Link

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c } from "@dhaba/safepay-ts/funcs/putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("putInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cRequest](../../models/operations/putinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890crequest.md)   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cResponse](../../models/operations/putinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cresponse.md)\>**

### Errors

| Error Type                                                                           | Status Code                                                                          | Content Type                                                                         |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| errors.PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cUnauthorizedError   | 401                                                                                  | application/json                                                                     |
| errors.PutInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cInternalServerError | 500                                                                                  | application/json                                                                     |
| errors.SafepayDefaultError                                                           | 4XX, 5XX                                                                             | \*/\*                                                                                |

## deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c

Delete Quick Link

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c } from "@dhaba/safepay-ts/funcs/deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("deleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890c failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cResponse](../../models/operations/deleteinvoicequicklinksv1link297bfa4bf61c4c7280a4368d731e890cresponse.md)\>**

### Errors

| Error Type                                                                              | Status Code                                                                             | Content Type                                                                            |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| errors.DeleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cUnauthorizedError   | 401                                                                                     | application/json                                                                        |
| errors.DeleteInvoiceQuickLinksV1Link297bfa4bF61c4c7280a4368d731e890cInternalServerError | 500                                                                                     | application/json                                                                        |
| errors.SafepayDefaultError                                                              | 4XX, 5XX                                                                                | \*/\*                                                                                   |

## postUserV2

Create Safepay Shopper

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.postUserV2();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { postUserV2 } from "@dhaba/safepay-ts/funcs/postUserV2.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await postUserV2(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("postUserV2 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostUserV2Request](../../models/operations/postuserv2request.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostUserV2Response](../../models/operations/postuserv2response.md)\>**

### Errors

| Error Type                     | Status Code                    | Content Type                   |
| ------------------------------ | ------------------------------ | ------------------------------ |
| errors.PostUserV2ConflictError | 409                            | application/json               |
| errors.SafepayDefaultError     | 4XX, 5XX                       | \*/\*                          |

## getUserV2

Find Safepay Shopper

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserV2();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserV2 } from "@dhaba/safepay-ts/funcs/getUserV2.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserV2(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserV2 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserV2Response](../../models/operations/getuserv2response.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.GetUserV2UnauthorizedError | 401                               | application/json                  |
| errors.SafepayDefaultError        | 4XX, 5XX                          | \*/\*                             |

## getUserV2Exists

Safepay Shopper Exists

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserV2Exists({
    email: "hzaidi@getsafepay.com",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserV2Exists } from "@dhaba/safepay-ts/funcs/getUserV2Exists.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserV2Exists(safepay, {
    email: "hzaidi@getsafepay.com",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserV2Exists failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUserV2ExistsRequest](../../models/operations/getuserv2existsrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserV2ExistsResponse](../../models/operations/getuserv2existsresponse.md)\>**

### Errors

| Error Type                            | Status Code                           | Content Type                          |
| ------------------------------------- | ------------------------------------- | ------------------------------------- |
| errors.GetUserV2ExistsBadRequestError | 400                                   | application/json                      |
| errors.SafepayDefaultError            | 4XX, 5XX                              | \*/\*                                 |

## getUserWalletsV1

List Payment Methods

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.getUserWalletsV1();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { getUserWalletsV1 } from "@dhaba/safepay-ts/funcs/getUserWalletsV1.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await getUserWalletsV1(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("getUserWalletsV1 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUserWalletsV1Response](../../models/operations/getuserwalletsv1response.md)\>**

### Errors

| Error Type                               | Status Code                              | Content Type                             |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| errors.GetUserWalletsV1UnauthorizedError | 401                                      | application/json                         |
| errors.SafepayDefaultError               | 4XX, 5XX                                 | \*/\*                                    |

## deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448

Delete Payment Method

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448 } from "@dhaba/safepay-ts/funcs/deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("deleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448 failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.DeleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448Response](../../models/operations/deleteuserwalletsv1inst8ed5e401ab7b442c8473dee137827448response.md)\>**

### Errors

| Error Type                                                                      | Status Code                                                                     | Content Type                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| errors.DeleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448UnauthorizedError | 401                                                                             | application/json                                                                |
| errors.DeleteUserWalletsV1Inst8ed5e401Ab7b442c8473Dee137827448NotFoundError     | 404                                                                             | application/json                                                                |
| errors.SafepayDefaultError                                                      | 4XX, 5XX                                                                        | \*/\*                                                                           |