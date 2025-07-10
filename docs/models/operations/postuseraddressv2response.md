# PostUserAddressV2Response

## Example Usage

```typescript
import { PostUserAddressV2Response } from "@dhaba/safepay-ts/models/operations";

let value: PostUserAddressV2Response = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
    ],
    "key1": [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  result: {},
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `headers`                                                                                            | Record<string, *string*[]>                                                                           | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `result`                                                                                             | [operations.PostUserAddressV2ResponseBody](../../models/operations/postuseraddressv2responsebody.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |