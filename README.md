# Pet-Store-API

<div align="left">
    <a href="https://speakeasyapi.dev/"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://github.com/speakeasy-sdks/Plunk-sample-sdk.git/actions"><img src="https://img.shields.io/github/actions/workflow/status/speakeasy-sdks/Plunk-sample-sdk/speakeasy_sdk_generation.yml?style=for-the-badge" /></a>
    
</div>


## 🏗 **Welcome to your new SDK!** 🏗

It has been generated successfully based on your OpenAPI spec. However, it is not yet ready for production use. Here are some next steps:
- [ ] 🛠 Make your SDK feel handcrafted by [customizing it](https://www.speakeasyapi.dev/docs/customize-sdks)
- [ ] ♻️ Refine your SDK quickly by iterating locally with the [Speakeasy CLI](https://github.com/speakeasy-api/speakeasy)
- [ ] 🎁 Publish your SDK to package managers by [configuring automatic publishing](https://www.speakeasyapi.dev/docs/productionize-sdks/publish-sdks)
- [ ] ✨ When ready to productionize, delete this section from the README
<!-- Start SDK Installation [installation] -->
## SDK Installation

### NPM

```bash
npm add https://github.com/speakeasy-sdks/Plunk-sample-sdk
```

### Yarn

```bash
yarn add https://github.com/speakeasy-sdks/Plunk-sample-sdk
```
<!-- End SDK Installation [installation] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

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

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

### [PetStoreAPI SDK](docs/sdks/petstoreapi/README.md)

* [deletePetsId](docs/sdks/petstoreapi/README.md#deletepetsid) - Delete a pet by ID
* [getPets](docs/sdks/petstoreapi/README.md#getpets) - List all pets
* [getPetsId](docs/sdks/petstoreapi/README.md#getpetsid) - Get a pet by ID
* [postPets](docs/sdks/petstoreapi/README.md#postpets) - Add a new pet
* [putPetsId](docs/sdks/petstoreapi/README.md#putpetsid) - Update a pet by ID
<!-- End Available Resources and Operations [operations] -->

<!-- Start Error Handling [errors] -->
## Error Handling

Handling errors in this SDK should largely match your expectations.  All operations return a response object or throw an error.  If Error objects are specified in your OpenAPI Spec, the SDK will throw the appropriate Error type.

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 400-600         | */*             |

Example

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
    const sdk = new PetStoreAPI();

    let res;
    try {
        res = await sdk.deletePetsId({
            id: 623531,
        });
    } catch (err) {
        if (err instanceof errors.SDKError) {
            console.error(err); // handle exception
            throw err;
        }
    }

    if (res.statusCode == 200) {
        // handle response
    }
}

run();

```
<!-- End Error Handling [errors] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The Typescript SDK makes API calls using the [axios](https://axios-http.com/docs/intro) HTTP library.  In order to provide a convenient way to configure timeouts, cookies, proxies, custom headers, and other low-level configuration, you can initialize the SDK client with a custom `AxiosInstance` object.

For example, you could specify a header for every request that your sdk makes as follows:

```typescript
import { Pet-Store-API } from "PetStoreAPI";
import axios from "axios";

const httpClient = axios.create({
    headers: {'x-custom-header': 'someValue'}
})

const sdk = new PetStoreAPI({defaultClient: httpClient});
```
<!-- End Custom HTTP Client [http-client] -->



<!-- Start Server Selection [server] -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `serverIdx: number` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| # | Server | Variables |
| - | ------ | --------- |
| 0 | `https://api.petstore.com/v1` | None |

#### Example

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
    const sdk = new PetStoreAPI({
        serverIdx: 0,
    });

    const res = await sdk.deletePetsId({
        id: 623531,
    });

    if (res.statusCode == 200) {
        // handle response
    }
}

run();

```


### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `serverURL: str` optional parameter when initializing the SDK client instance. For example:
```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
    const sdk = new PetStoreAPI({
        serverURL: "https://api.petstore.com/v1",
    });

    const res = await sdk.deletePetsId({
        id: 623531,
    });

    if (res.statusCode == 200) {
        // handle response
    }
}

run();

```
<!-- End Server Selection [server] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
