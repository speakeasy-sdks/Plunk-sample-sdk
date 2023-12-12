<!-- Start SDK Example Usage [usage] -->
```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
    const sdk = new PetStoreAPI();

    const res = await sdk.deletePetsId({
        id: 623531,
    });

    if (res.statusCode == 200) {
        // handle response
    }
}

run();

```
<!-- End SDK Example Usage [usage] -->