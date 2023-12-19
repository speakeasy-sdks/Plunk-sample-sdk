# PetStoreAPI SDK


## Overview

Pet Store API: A simple API for managing a pet store.

### Available Operations

* [deletePetsId](#deletepetsid) - Delete a pet by ID
* [getPets](#getpets) - List all pets
* [getPetsId](#getpetsid) - Get a pet by ID
* [postPets](#postpets) - Add a new pet
* [putPetsId](#putpetsid) - Update a pet by ID

## deletePetsId

Delete a pet by ID

### Example Usage

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

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `request`                                                                            | [operations.DeletePetsIdRequest](../../sdk/models/operations/deletepetsidrequest.md) | :heavy_check_mark:                                                                   | The request object to use for the request.                                           |
| `config`                                                                             | [AxiosRequestConfig](https://axios-http.com/docs/req_config)                         | :heavy_minus_sign:                                                                   | Available config options for making requests.                                        |


### Response

**Promise<[operations.DeletePetsIdResponse](../../sdk/models/operations/deletepetsidresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |

## getPets

List all pets

### Example Usage

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
  const sdk = new PetStoreAPI();

  const res = await sdk.getPets();

  if (res.statusCode == 200) {
    // handle response
  }
}

run();
```

### Parameters

| Parameter                                                    | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `config`                                                     | [AxiosRequestConfig](https://axios-http.com/docs/req_config) | :heavy_minus_sign:                                           | Available config options for making requests.                |


### Response

**Promise<[operations.GetPetsResponse](../../sdk/models/operations/getpetsresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |

## getPetsId

Get a pet by ID

### Example Usage

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
  const sdk = new PetStoreAPI();

  const res = await sdk.getPetsId({
    id: 524896,
  });

  if (res.statusCode == 200) {
    // handle response
  }
}

run();
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `request`                                                                      | [operations.GetPetsIdRequest](../../sdk/models/operations/getpetsidrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |
| `config`                                                                       | [AxiosRequestConfig](https://axios-http.com/docs/req_config)                   | :heavy_minus_sign:                                                             | Available config options for making requests.                                  |


### Response

**Promise<[operations.GetPetsIdResponse](../../sdk/models/operations/getpetsidresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |

## postPets

Add a new pet

### Example Usage

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
  const sdk = new PetStoreAPI();

  const res = await sdk.postPets(new TextEncoder().encode("0xc1C582a00e"));

  if (res.statusCode == 200) {
    // handle response
  }
}

run();
```

### Parameters

| Parameter                                                    | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `request`                                                    | [Uint8Array](../../models/.md)                               | :heavy_check_mark:                                           | The request object to use for the request.                   |
| `config`                                                     | [AxiosRequestConfig](https://axios-http.com/docs/req_config) | :heavy_minus_sign:                                           | Available config options for making requests.                |


### Response

**Promise<[operations.PostPetsResponse](../../sdk/models/operations/postpetsresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |

## putPetsId

Update a pet by ID

### Example Usage

```typescript
import { PetStoreAPI } from "Pet-Store-API";

async function run() {
  const sdk = new PetStoreAPI();

  const res = await sdk.putPetsId({
    requestBody: new TextEncoder().encode("0xf7Bd28fFAB"),
    id: 418284,
  });

  if (res.statusCode == 200) {
    // handle response
  }
}

run();
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `request`                                                                      | [operations.PutPetsIdRequest](../../sdk/models/operations/putpetsidrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |
| `config`                                                                       | [AxiosRequestConfig](https://axios-http.com/docs/req_config)                   | :heavy_minus_sign:                                                             | Available config options for making requests.                                  |


### Response

**Promise<[operations.PutPetsIdResponse](../../sdk/models/operations/putpetsidresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |
