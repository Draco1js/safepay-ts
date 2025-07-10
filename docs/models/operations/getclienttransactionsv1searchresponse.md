# GetClientTransactionsV1SearchResponse

## Example Usage

```typescript
import { GetClientTransactionsV1SearchResponse } from "@dhaba/safepay-ts/models/operations";

let value: GetClientTransactionsV1SearchResponse = {
  headers: {
    "key": [
      "<value 1>",
    ],
    "key1": [
      "<value 1>",
    ],
    "key2": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: {},
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `headers`                                                                                                                    | Record<string, *string*[]>                                                                                                   | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |
| `result`                                                                                                                     | [operations.GetClientTransactionsV1SearchResponseBody](../../models/operations/getclienttransactionsv1searchresponsebody.md) | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |