<!-- Start SDK Example Usage [usage] -->
```typescript
import { Safepay } from "@dhaba/safepay-ts";

const safepay = new Safepay();

async function run() {
  const result = await safepay.auth.createMerchantJwt({});

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->