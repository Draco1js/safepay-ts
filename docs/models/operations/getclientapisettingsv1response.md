# GetClientApiSettingsV1Response

## Example Usage

```typescript
import { GetClientApiSettingsV1Response } from "@dhaba/safepay-ts/models/operations";

let value: GetClientApiSettingsV1Response = {
  headers: {
    "key": [
      "<value 1>",
    ],
    "key1": [
      "<value 1>",
      "<value 2>",
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

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `headers`                                                                                                      | Record<string, *string*[]>                                                                                     | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `result`                                                                                                       | [operations.GetClientApiSettingsV1ResponseBody](../../models/operations/getclientapisettingsv1responsebody.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |