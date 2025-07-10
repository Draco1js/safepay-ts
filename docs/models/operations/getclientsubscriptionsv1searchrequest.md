# GetClientSubscriptionsV1SearchRequest

## Example Usage

```typescript
import { GetClientSubscriptionsV1SearchRequest } from "@dhaba/safepay-ts/models/operations";

let value: GetClientSubscriptionsV1SearchRequest = {};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `tokens`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Filter by subscription IDs                                     |
| `planIds`                                                      | *string*                                                       | :heavy_minus_sign:                                             | Filter by plan IDs                                             |
| `userIds`                                                      | *string*                                                       | :heavy_minus_sign:                                             | Filter by User IDs                                             |
| `statuses`                                                     | *string*                                                       | :heavy_minus_sign:                                             | Filter by statuses                                             |
| `limit`                                                        | *string*                                                       | :heavy_minus_sign:                                             | Limit search results to a value                                |
| `page`                                                         | *string*                                                       | :heavy_minus_sign:                                             | Paginate search results                                        |
| `sortBy`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Sort by specifies the field use to sort data e.g. `created_at` |
| `direction`                                                    | *string*                                                       | :heavy_minus_sign:                                             | Direction specifies the data sort order either ASC or DESC     |