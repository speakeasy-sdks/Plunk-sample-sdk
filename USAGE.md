<!-- Start SDK Example Usage -->
```typescript
import { PetStoreAPI } from "Pet-Store-API";

(async () => {
    const sdk = new PetStoreAPI();

    const res = await sdk.deletePetsId({
        id: 623531,
    });

    if (res.statusCode == 200) {
        // handle response
    }
})();

```
<!-- End SDK Example Usage -->