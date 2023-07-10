# Spacer

This is a component that is used to add a space between components.

## Attributes

| Attribute             | Description                                                                                                        |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------- |
| `size` <br/> _string_ | Size of the spacer. </br> </br>_Possible values: `very-small`, `small`, `medium` (Default), `large`, `very-large`_ |

## Properties
| Property                                                | Description                                                 |
| :------------------------------------------------------ | :---------------------------------------------------------- |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which device the component should be displayed. |

## Example

```xml
<components>
	<spacer size="very-small" bleed="true"/>
	<spacer>
		<device mobile="true" tablet="true" desktop="true"/>
	</spacer>
</components>
```