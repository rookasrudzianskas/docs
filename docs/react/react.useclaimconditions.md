---
slug: /react.useclaimconditions
title: useClaimConditions() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useClaimConditions() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.

Use this to get all claim conditons for ERC20, ERC721 or ERC1155 based contracts. They need to extend the `claimCondition` extension for this hook to work.

**Signature:**

```typescript
export declare function useClaimConditions<
  TContract extends NFTDrop | EditionDrop | TokenDrop,
>(
  ...[contract, tokenId]: ActiveClaimConditionParams<TContract>
): import("react-query").UseQueryResult<
  {
    snapshot?:
      | {
          address: string;
          maxClaimable: string;
        }[]
      | undefined;
    quantityLimitPerTransaction: string;
    startTime: Date;
    price: import("ethers").BigNumber;
    currencyAddress: string;
    maxQuantity: string;
    waitInSeconds: import("ethers").BigNumber;
    merkleRootHash: string | number[];
    availableSupply: string;
    currentMintSupply: string;
    currencyMetadata: {
      symbol: string;
      name: string;
      value: import("ethers").BigNumber;
      decimals: number;
      displayValue: string;
    };
  }[],
  unknown
>;
```

## Parameters

| Parameter             | Type                                        | Description |
| --------------------- | ------------------------------------------- | ----------- |
| \[contract, tokenId\] | ActiveClaimConditionParams&lt;TContract&gt; |             |

**Returns:**

import("react-query").UseQueryResult&lt;{ snapshot?: { address: string; maxClaimable: string; }\[\] \| undefined; quantityLimitPerTransaction: string; startTime: Date; price: import("ethers").BigNumber; currencyAddress: string; maxQuantity: string; waitInSeconds: import("ethers").BigNumber; merkleRootHash: string \| number\[\]; availableSupply: string; currentMintSupply: string; currencyMetadata: { symbol: string; name: string; value: import("ethers").BigNumber; decimals: number; displayValue: string; }; }\[\], unknown&gt;

a response object with the list of claim conditions

## Example 1

```javascript
const { data: claimConditions, isLoading, error } = useClaimConditions(<YourERC20ContractInstance>);
```

## Example 2

```javascript
const { data: claimConditions, isLoading, error } = useClaimConditions(<YourERC721ContractInstance>);
```

## Example 3

```javascript
const { data: claimConditions, isLoading, error } = useClaimConditions(<YourERC1155ContractInstance>, <tokenId>);
```
