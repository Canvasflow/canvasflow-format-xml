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
  <map latitude="3.123123123" longitude="1.123123123">
    <markers>
      <marker latitude="1.1111" longitude="1.11111">
        <caption>Eiffel Tower</caption>
      </marker>
      <marker latitude="1.1111" longitude="1.11111"/>
    </markers>
  </map>
</components>
```