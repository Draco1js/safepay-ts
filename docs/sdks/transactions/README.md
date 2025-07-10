# Transactions
(*transactions*)

## Overview

### Available Operations

* [refund](#refund) - Refund Transaction

## refund

Refund Transaction

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.transactions.refund();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { transactionsRefund } from "@dhaba/safepay-ts/funcs/transactionsRefund.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await transactionsRefund(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionsRefund failed:", res.error);
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