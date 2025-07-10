# Charge

## Example Usage

```typescript
import { Charge } from "@dhaba/safepay-ts/models/operations";

let value: Charge = {};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `token`                                                                  | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `tracker`                                                                | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `client`                                                                 | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `user`                                                                   | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `amount`                                                                 | [operations.Amount](../../models/operations/amount.md)                   | :heavy_minus_sign:                                                       | N/A                                                                      |
| `fees`                                                                   | [operations.Fees](../../models/operations/fees.md)                       | :heavy_minus_sign:                                                       | N/A                                                                      |
| `tax`                                                                    | [operations.Tax](../../models/operations/tax.md)                         | :heavy_minus_sign:                                                       | N/A                                                                      |
| `net`                                                                    | [operations.Net](../../models/operations/net.md)                         | :heavy_minus_sign:                                                       | N/A                                                                      |
| `signature`                                                              | *string*                                                                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `capture`                                                                | [operations.ChargeCapture](../../models/operations/chargecapture.md)     | :heavy_minus_sign:                                                       | N/A                                                                      |
| `balance`                                                                | [operations.Balance](../../models/operations/balance.md)                 | :heavy_minus_sign:                                                       | N/A                                                                      |
| `createdAt`                                                              | [operations.ChargeCreatedAt](../../models/operations/chargecreatedat.md) | :heavy_minus_sign:                                                       | N/A                                                                      |
| `updatedAt`                                                              | [operations.ChargeUpdatedAt](../../models/operations/chargeupdatedat.md) | :heavy_minus_sign:                                                       | N/A                                                                      |