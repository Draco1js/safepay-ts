# Wallets
(*wallets*)

## Overview

### Available Operations

* [deletePaymentMethod](#deletepaymentmethod) - Delete Payment Method

## deletePaymentMethod

Delete Payment Method

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.wallets.deletePaymentMethod();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { walletsDeletePaymentMethod } from "@dhaba/safepay-ts/funcs/walletsDeletePaymentMethod.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await walletsDeletePaymentMethod(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("walletsDeletePaymentMethod failed:", res.error);
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