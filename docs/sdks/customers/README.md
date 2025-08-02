# Customers
(*customers*)

## Overview

### Available Operations

* [create](#create) - Create Customer
* [list](#list) - List Customers

## create

Create Customer

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/user/customers/v1" method="post" path="/user/customers/v1" -->
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.customers.create({});

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
  const res = await customersCreate(safepay, {});
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostClientApiSettingsV1BadRequestError         | 400                                                   | application/json                                      |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |

## list

List Customers

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/user/customers/v1" method="get" path="/user/customers/v1" -->
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostClientApiSettingsV1BadRequestError         | 400                                                   | application/json                                      |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |