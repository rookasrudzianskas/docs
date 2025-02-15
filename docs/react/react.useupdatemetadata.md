---
slug: /react.useupdatemetadata
title: useUpdateMetadata() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useUpdateMetadata() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.

Use this to update the metadata of your

**Signature:**

```typescript
export declare function useUpdateMetadata(
  contract: RequiredParam<SmartContract | ValidContractInstance>,
): import("react-query").UseMutationResult<
  {
    receipt: import("@ethersproject/abstract-provider").TransactionReceipt;
    data: () => Promise<any>;
  },
  unknown,
  {
    [x: string]: import("@thirdweb-dev/sdk/dist/browser").Json;
    description?: string | undefined;
    image?: any;
    external_link?: string | undefined;
    name: string;
  },
  unknown
>;
```

## Parameters

| Parameter | Type                                                                                        | Description      |
| --------- | ------------------------------------------------------------------------------------------- | ---------------- |
| contract  | [RequiredParam](./react.requiredparam.md)&lt;SmartContract &#124; ValidContractInstance&gt; | an instance of a |

**Returns:**

import("react-query").UseMutationResult&lt;{ receipt: import("@ethersproject/abstract-provider").TransactionReceipt; data: () =&gt; Promise&lt;any&gt;; }, unknown, { \[x: string\]: import("@thirdweb-dev/sdk/dist/browser").Json; description?: string \| undefined; image?: any; external_link?: string \| undefined; name: string; }, unknown&gt;

a mutation object that can be used to update the metadata

## Example

```jsx
const Component = () => {
  const {
    mutate: updateMetadata,
    isLoading,
    error,
  } = useUpdateMetadata(SmartContract);

  if (error) {
    console.error("failed to update metadata", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() =>
        updateMetadata({
          updatePayload: {
            name: "My Contract",
            description: "This is my contract",
          },
        })
      }
    >
      Update Metadata
    </button>
  );
};
```
