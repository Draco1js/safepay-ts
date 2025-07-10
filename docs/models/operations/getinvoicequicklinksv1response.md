# GetInvoiceQuickLinksV1Response

## Example Usage

```typescript
import { GetInvoiceQuickLinksV1Response } from "@dhaba/safepay-ts/models/operations";

let value: GetInvoiceQuickLinksV1Response = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
    ],
    "key1": [
      "<value 1>",
      "<value 2>",
    ],
    "key2": [],
  },
  result: {},
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `headers`                                                                                                      | Record<string, *string*[]>                                                                                     | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `result`                                                                                                       | [operations.GetInvoiceQuickLinksV1ResponseBody](../../models/operations/getinvoicequicklinksv1responsebody.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |