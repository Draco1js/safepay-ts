# GetClientPlansV1SearchRequest

## Example Usage

```typescript
import { GetClientPlansV1SearchRequest } from "@dhaba/safepay-ts/models/operations";

let value: GetClientPlansV1SearchRequest = {
  currencies: "PKR",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    | Example                                                        |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `planIds`                                                      | *string*                                                       | :heavy_minus_sign:                                             | Filter for specific Plan IDs                                   |                                                                |
| `intervals`                                                    | *string*                                                       | :heavy_minus_sign:                                             | Filter for specific intervals                                  |                                                                |
| `products`                                                     | *string*                                                       | :heavy_minus_sign:                                             | Filter for specific products                                   |                                                                |
| `currencies`                                                   | *string*                                                       | :heavy_minus_sign:                                             | Filter for specific currencies                                 | PKR                                                            |
| `limit`                                                        | *string*                                                       | :heavy_minus_sign:                                             | Limit search results to a value                                |                                                                |
| `page`                                                         | *string*                                                       | :heavy_minus_sign:                                             | Paginate search results                                        |                                                                |
| `sortBy`                                                       | *string*                                                       | :heavy_minus_sign:                                             | Sort by specifies the field use to sort data e.g. `created_at` |                                                                |
| `direction`                                                    | *string*                                                       | :heavy_minus_sign:                                             | Direction specifies the data sort order either ASC or DESC     |                                                                |