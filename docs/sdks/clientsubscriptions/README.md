# ClientSubscriptions
(*clientSubscriptions*)

## Overview

### Available Operations

* [update](#update) - Update Subscription
* [resume](#resume) - Resume Subscription

## update

Update Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.clientSubscriptions.update();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { clientSubscriptionsUpdate } from "@dhaba/safepay-ts/funcs/clientSubscriptionsUpdate.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await clientSubscriptionsUpdate(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("clientSubscriptionsUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3Request](../../models/operations/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3request.md) | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3Response](../../models/operations/putclientsubscriptionsv1subee09b0f9974f4deeb1b34ad8dad2e7b3response.md)\>**

### Errors

| Error Type                                                                          | Status Code                                                                         | Content Type                                                                        |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| errors.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3UnauthorizedError | 401                                                                                 | application/json                                                                    |
| errors.PutClientSubscriptionsV1SubEe09b0f9974f4deeB1b34ad8dad2e7b3NotFoundError     | 404                                                                                 | application/json                                                                    |
| errors.SafepayDefaultError                                                          | 4XX, 5XX                                                                            | \*/\*                                                                               |

## resume

Resume Subscription

### Example Usage

```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.clientSubscriptions.resume();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SafepayCore } from "@dhaba/safepay-ts/core.js";
import { clientSubscriptionsResume } from "@dhaba/safepay-ts/funcs/clientSubscriptionsResume.js";

// Use `SafepayCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const safepay = new SafepayCore();

async function run() {
  const res = await clientSubscriptionsResume(safepay);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("clientSubscriptionsResume failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                                          | Type                                                                                                                                                                                               | Required                                                                                                                                                                                           | Description                                                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                                                                                                          | [operations.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionRequest](../../models/operations/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionrequest.md) | :heavy_check_mark:                                                                                                                                                                                 | The request object to use for the request.                                                                                                                                                         |
| `options`                                                                                                                                                                                          | RequestOptions                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                 | Used to set various options for making HTTP requests.                                                                                                                                              |
| `options.fetchOptions`                                                                                                                                                                             | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                                            | :heavy_minus_sign:                                                                                                                                                                                 | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed.                     |
| `options.retries`                                                                                                                                                                                  | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                 | Enables retrying HTTP requests under certain failure conditions.                                                                                                                                   |

### Response

**Promise\<[operations.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionResponse](../../models/operations/putclientsubscriptionsv1sub130aa5b290564c8eb9c99149e68f17ceresumptionresponse.md)\>**

### Errors

| Error Type                                                                                      | Status Code                                                                                     | Content Type                                                                                    |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionUnauthorizedError   | 401                                                                                             | application/json                                                                                |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionNotFoundError       | 404                                                                                             | application/json                                                                                |
| errors.PutClientSubscriptionsV1Sub130aa5b290564c8eB9c99149e68f17ceResumptionInternalServerError | 500                                                                                             | application/json                                                                                |
| errors.SafepayDefaultError                                                                      | 4XX, 5XX                                                                                        | \*/\*                                                                                           |