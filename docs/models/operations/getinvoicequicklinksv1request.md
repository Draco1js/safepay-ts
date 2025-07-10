# GetInvoiceQuickLinksV1Request

## Example Usage

```typescript
import { GetInvoiceQuickLinksV1Request } from "@dhaba/safepay-ts/models/operations";

let value: GetInvoiceQuickLinksV1Request = {
  page: 1,
  limit: 10,
  workflow: "MANUAL",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            | Example                                                                                |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `page`                                                                                 | *number*                                                                               | :heavy_minus_sign:                                                                     | The page to search for. Page serves as an offset counter starting with 1               | 1                                                                                      |
| `limit`                                                                                | *number*                                                                               | :heavy_minus_sign:                                                                     | How many results to return per page. A limit of 10 will return 10 Quick Links per page | 10                                                                                     |
| `workflow`                                                                             | *string*                                                                               | :heavy_minus_sign:                                                                     | One of EMAIL or MANUAL                                                                 | MANUAL                                                                                 |