# Webhooks
(*webhooks*)

## Overview

### Available Operations

* [test](#test) - Test Webhook

## test

Test Webhook

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.webhooks.test({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { webhooksTest } from "@dhaba/safepay-ts/funcs/webhooksTest.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await webhooksTest(safepay, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksTest failed:", res.error);
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

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.PostClientHooksV2TestBadRequestError           | 400                                                   | application/json                                      |
| errors.PostAuthV1CompanyAuthenticateUnauthorizedError | 401                                                   | application/json                                      |
| errors.ErrorT                                         | 404                                                   | application/json                                      |
| errors.ErrorT                                         | 500                                                   | application/json                                      |
| errors.SafepayDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |