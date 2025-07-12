# Plans
(*plans*)

## Overview

### Available Operations

* [create](#create) - Create Plan
* [search](#search) - Search Plans

## create

Create Plan

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.plans.create({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { plansCreate } from "@dhaba/safepay-ts/funcs/plansCreate.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await plansCreate(safepay, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("plansCreate failed:", res.error);
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostClientPlansV1BadRequestError               | 400                                                   | application/json                                      |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.PostClientPlansV1InternalServerError           | 500                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |

## search

Search Plans

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.plans.search({
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
import { plansSearch } from "@dhaba/safepay-ts/funcs/plansSearch.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await plansSearch(safepay, {
    currencies: "PKR",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("plansSearch failed:", res.error);
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostClientPlansV1BadRequestError               | 400                                                   | application/json                                      |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |