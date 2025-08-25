# Shoppers
(*shoppers*)

## Overview

### Available Operations

* [createSafepay](#createsafepay) - Create Safepay Shopper

## createSafepay

Create Safepay Shopper

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/user/v2" method="post" path="/user/v2" -->
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.shoppers.createSafepay({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { shoppersCreateSafepay } from "@dhaba/safepay-ts/funcs/shoppersCreateSafepay.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await shoppersCreateSafepay(safepay, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("shoppersCreateSafepay failed:", res.error);
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

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.ConflictError       | 409                        | application/json           |
| errors.SafepayDefaultError | 4XX, 5XX                   | \*/\*                      |