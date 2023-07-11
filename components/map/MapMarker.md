---
title: "Canvasflow Map Marker Component"
alias: ["Canvasflow Map Marker Component"]
tags: "#canvasflow, #work, #spec"
last_reviewed: 2023-07-11
created_at: 2023-07-11
keywords:
  - canvasflow
  - specification
  - format
  - map
---

# Map Marker Component

This component is used to display a marker in the [Map Component](../Map.md).

## Attributes

| Attribute                  | Description                                 |
| :------------------------- | :------------------------------------------ |
| `latitude` <br/> _number_  | **(Required)** The latitude of the marker.  |
| `longitude` <br/> _number_ | **(Required)** The longitude of the marker. |


## Properties
| Property                                                      | Description                                             |
| :------------------------------------------------------------ | :------------------------------------------------------ |
| `caption` <br/>_[Caption](../../format/CaptionDescriptor.md)_ | Control if a caption should be displayed in the content |

## Example
```xml
<components>
  <map latitude="48.85827830746261" longitude="2.2942667208178773">
    <markers>
      <marker latitude="48.85761477995638" longitude="2.2957902154025494"/>
    </markers>
    <caption>Eiffel Tower Paris</caption>
  </map>
</components>
```