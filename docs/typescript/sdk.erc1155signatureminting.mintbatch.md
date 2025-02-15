---
slug: /sdk.erc1155signatureminting.mintbatch
title: Erc1155SignatureMinting.mintBatch() method
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## Erc1155SignatureMinting.mintBatch() method

Mint any number of dynamically generated NFT at once

**Signature:**

```typescript
mintBatch(signedPayloads: SignedPayload1155[]): Promise<TransactionResultWithId[]>;
```

## Parameters

| Parameter      | Type                                                | Description                          |
| -------------- | --------------------------------------------------- | ------------------------------------ |
| signedPayloads | [SignedPayload1155](./sdk.signedpayload1155.md)\[\] | the array of signed payloads to mint |

**Returns:**

Promise&lt;[TransactionResultWithId](./sdk.transactionresultwithid.md)\[\]&gt;

## Remarks

Mint multiple dynamic NFTs in one transaction. Note that this is only possible for free mints (cannot batch mints with a price attached to it for security reasons)
