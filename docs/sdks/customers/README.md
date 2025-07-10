# Customers
(*customers*)

## Overview

### Available Operations

* [create](#create) - Create Customer
* [list](#list) - List Customers
* [update](#update) - Update Customer
* [get](#get) - Find Customer
* [delete](#delete) - Delete Customer
* [getPaymentMethod](#getpaymentmethod) - Find Payment Method
* [listPaymentMethods](#listpaymentmethods) - List Payment Methods

## create

Create Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.create();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { customersCreate } from "@dhaba/safepay-ts/funcs/customersCreate.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersCreate(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersCreate failed:", res.error);
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

## list

List Customers

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.list({
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
import { customersList } from "@dhaba/safepay-ts/funcs/customersList.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersList(safepay, {
    limit: 20,
    page: 1,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersList failed:", res.error);
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

## update

Update Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.update();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { customersUpdate } from "@dhaba/safepay-ts/funcs/customersUpdate.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersUpdate(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersUpdate failed:", res.error);
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

## get

Find Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.get();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { customersGet } from "@dhaba/safepay-ts/funcs/customersGet.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersGet(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersGet failed:", res.error);
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

## delete

Delete Customer

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.delete();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { customersDelete } from "@dhaba/safepay-ts/funcs/customersDelete.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersDelete(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersDelete failed:", res.error);
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

## getPaymentMethod

Find Payment Method

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.getPaymentMethod();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { customersGetPaymentMethod } from "@dhaba/safepay-ts/funcs/customersGetPaymentMethod.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersGetPaymentMethod(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersGetPaymentMethod failed:", res.error);
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

## listPaymentMethods

List Payment Methods

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.listPaymentMethods({
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
import { customersListPaymentMethods } from "@dhaba/safepay-ts/funcs/customersListPaymentMethods.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await customersListPaymentMethods(safepay, {
    limit: 20,
    page: 1,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("customersListPaymentMethods failed:", res.error);
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