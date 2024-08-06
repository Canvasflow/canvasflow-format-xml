# Spacer

This component is used to add a space between components.

## Attributes

| Attribute             | Description                                                                                                        |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_   | Id of the component                                                                                                |
| `size` <br/> _string_ | Size of the spacer. </br> </br>_Possible values: `very-small`, `small`, `medium` (Default), `large`, `very-large`_ |

## Elements

| Element                                                 | Description                                                  |
| :------------------------------------------------------ | :----------------------------------------------------------- |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which devices the component should be displayed. |

## Example

```xml
<components>
  <spacer size="very-small" bleed="true"/>
  <spacer>
    <device mobile="true" tablet="true" desktop="true"/>
  </spacer>
</components>
```
