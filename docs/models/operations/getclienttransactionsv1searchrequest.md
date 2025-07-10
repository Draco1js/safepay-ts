# GetClientTransactionsV1SearchRequest

## Example Usage

```typescript
import { GetClientTransactionsV1SearchRequest } from "@dhaba/safepay-ts/models/operations";

let value: GetClientTransactionsV1SearchRequest = {};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `tokens`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Filter by transaction IDs                                      |
| `states`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Filter by transaction states                                   |
| `currencies`                                                   | *string*                                                       | :heavy_minus_sign:                                             | Filter by currencies                                           |
| `instrumentIds`                                                | *string*                                                       | :heavy_minus_sign:                                             | Filter by instrument IDs                                       |
| `subscriptionIds`                                              | *string*                                                       | :heavy_minus_sign:                                             | Filter by subscription IDs                                     |
| `userIds`                                                      | *string*                                                       | :heavy_minus_sign:                                             | Filter by User IDs                                             |
| `limit`                                                        | *string*                                                       | :heavy_minus_sign:                                             | Limit search results                                           |
| `page`                                                         | *string*                                                       | :heavy_minus_sign:                                             | Paginate search results                                        |
| `sortBy`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Sort by specifies the field use to sort data e.g. `created_at` |
| `direction`                                                    | *string*                                                       | :heavy_minus_sign:                                             | Direction specifies the data sort order either ASC or DESC     |