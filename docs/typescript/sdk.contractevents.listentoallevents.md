---
slug: /sdk.contractevents.listentoallevents
title: ContractEvents.listenToAllEvents() method
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## ContractEvents.listenToAllEvents() method

Listen to all events emitted from this contract

**Signature:**

```typescript
listenToAllEvents(listener: (event: ContractEvent) => void): void;
```

## Parameters

| Parameter | Type                                                        | Description                                         |
| --------- | ----------------------------------------------------------- | --------------------------------------------------- |
| listener  | (event: [ContractEvent](./sdk.contractevent.md)) =&gt; void | the receiver that will be called on every new event |

**Returns:**

void

## Example

```javascript
contract.events.listenToAllEvents((event) => {
  console.log(event.eventName) // the name of the emitted event
  console.log(event.data) // event payload
}
```
