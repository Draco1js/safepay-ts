# GetReporterApiV1PaymentsRequest

## Example Usage

```typescript
import { GetReporterApiV1PaymentsRequest } from "@dhaba/safepay-ts/models/operations";

let value: GetReporterApiV1PaymentsRequest = {
  limit: 5,
  page: 1,
  sortBy: "created_at",
  direction: "DESC",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    | Example                                                        |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `limit`                                                        | *number*                                                       | :heavy_minus_sign:                                             | Limit search results to a value                                | 5                                                              |
| `page`                                                         | *number*                                                       | :heavy_minus_sign:                                             | Paginate search results                                        | 1                                                              |
| `sortBy`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Sort by specifies the field use to sort data e.g. `created_at` | created_at                                                     |
| `direction`                                                    | *string*                                                       | :heavy_minus_sign:                                             | Direction specifies the data sort order either ASC or DESC     | DESC                                                           |