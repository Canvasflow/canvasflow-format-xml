# Divider

This is a component that is used to add a divider between components.

## Attributes

| Attribute               | Description                                                                                                                                                                                                |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bleed` <br/> _boolean_ | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |

## Properties
| Property                                                | Description                                                 |
| :------------------------------------------------------ | :---------------------------------------------------------- |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which device the component should be displayed. |

## Example

```xml
<components>
	<divider bleed="true"/>
	<divider>
		<device mobile="true" tablet="true" desktop="true"/>
	</divider>
</components>
```