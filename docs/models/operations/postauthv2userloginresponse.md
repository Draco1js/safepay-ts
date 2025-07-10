# PostAuthV2UserLoginResponse

## Example Usage

```typescript
import { PostAuthV2UserLoginResponse } from "@dhaba/safepay-ts/models/operations";

let value: PostAuthV2UserLoginResponse = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
    ],
    "key1": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: {},
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `headers`                                                                                                | Record<string, *string*[]>                                                                               | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `result`                                                                                                 | [operations.PostAuthV2UserLoginResponseBody](../../models/operations/postauthv2userloginresponsebody.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |