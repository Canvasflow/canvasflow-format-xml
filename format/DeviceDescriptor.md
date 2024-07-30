# Device

Property that specify if the component should be displayed in a particular device.

## Attribute

| Properties                | Description                                                                                                                                  |
| :------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------- |
| `mobile` <br/> _boolean_  | Should this component be display in a `mobile` device, if the attribute is missing is going to assume that the element should be displayed.  |
| `tablet` <br/> _boolean_  | Should this component be display in a `tablet` device, if the attribute is missing is going to assume that the element should be displayed.  |
| `desktop` <br/> _boolean_ | Should this component be display in a `desktop` device, if the attribute is missing is going to assume that the element should be displayed. |

## Example

```xml
<components>
  <image src="bundle://images/image.jpg">
    <device mobile="true" tablet="true" desktop="true"/>
  </image>
</components>
```