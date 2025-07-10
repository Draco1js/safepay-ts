# GetUserV2Response

## Example Usage

```typescript
import { GetUserV2Response } from "@dhaba/safepay-ts/models/operations";

let value: GetUserV2Response = {
  headers: {
    "key": [],
    "key1": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: {},
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `headers`                                                                            | Record<string, *string*[]>                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `result`                                                                             | [operations.GetUserV2ResponseBody](../../models/operations/getuserv2responsebody.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |