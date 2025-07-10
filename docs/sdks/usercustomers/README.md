# UserCustomers
(*userCustomers*)

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
  const result = await safepay.userCustomers.deletePaymentMethod();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { userCustomersDeletePaymentMethod } from "@dhaba/safepay-ts/funcs/userCustomersDeletePaymentMethod.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await userCustomersDeletePaymentMethod(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("userCustomersDeletePaymentMethod failed:", res.error);
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