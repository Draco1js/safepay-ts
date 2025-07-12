# Subscriptions
(*subscriptions*)

## Overview

### Available Operations

* [search](#search) - Search Subscriptions

## search

Search Subscriptions

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.subscriptions.search();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { subscriptionsSearch } from "@dhaba/safepay-ts/funcs/subscriptionsSearch.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await subscriptionsSearch(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionsSearch failed:", res.error);
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |