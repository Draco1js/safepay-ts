# UserAddresses
(*userAddresses*)

## Overview

### Available Operations

* [updateById](#updatebyid) - Update Address
* [findById](#findbyid) - Find Address

## updateById

Update Address

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.userAddresses.updateById();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { userAddressesUpdateById } from "@dhaba/safepay-ts/funcs/userAddressesUpdateById.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await userAddressesUpdateById(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("userAddressesUpdateById failed:", res.error);
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

## findById

Find Address

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.userAddresses.findById();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { userAddressesFindById } from "@dhaba/safepay-ts/funcs/userAddressesFindById.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await userAddressesFindById(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("userAddressesFindById failed:", res.error);
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