# Divider

This component is used to add a divider between components.

## Attributes

| Attribute               | Description                                                                                                                                                                                                |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_     | Id of the component                                                                                                                                                                                        |
| `bleed` <br/> _boolean_ | This is a value that expresses whether the component should bleed in the document. _Bleed is only valid at the root level, bleed will be set to `false` if the component is inside a `column`._ |

## Elements

| Element                                                 | Description                                                  |
| :------------------------------------------------------ | :----------------------------------------------------------- |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which devices the component should be displayed. |

## Example

```xml
<components>
  <divider bleed="true"/>
  <divider>
    <device mobile="true" tablet="true" desktop="true"/>
  </divider>
</components>
```
