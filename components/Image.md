# Image

This component is used to display an image in the article.

## Attributes

| Attribute                      | Description                                                                                                                                                                                                        |
| :----------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_            | Id of the component                                                                                                                                                                                                |
| `role` <br/> _string_          | Role of the image </br> </br>_Possible values: `image`, `photo`, `figure`, `portrait`, `logo`, `thumbnail`_                                                                                                        |
| `width` <br/> _number_         | Width of the image in the article                                                                                                                                                                                  |
| `height` <br/> _number_        | Height of the image in the article                                                                                                                                                                                 |
| `src` <br/> _uri_              | **(Required)** The URL of the image file </br></br> Image URL can begin with `http://`, `https://` or `bundle://`. If the image begins with `bundle://`, the image reference must be relative to the `assets` path. |
| `bleed` <br/> _boolean_        | This is a value that expresses whether a component should bleed in the document. _Bleed is only valid at the root level, bleed will automatically be turned to `false` if the component is inside a `column`._         |
| `unselectable` <br/> _boolean_ | Value that expresses whether the image can be selected.                                                                                                                                                                   |


## Elements

| Element                                                           | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `animation` <br/> _[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Controls if a `caption` should be displayed in the content   |
| `credit` <br/>_[Credit](../format/CreditDescriptor.md)_           | Controls if a `credit` should be displayed in the content    |

_If the image is inside a gallery component the properties `animation` and `device` are ignored_

## Example

```xml
<components>
  <image 
    role="image" 
    bleed="false" 
    unselectable="false" 
    src="bundle://images/lighting.jpg">
      <animation type="bounceIn" speed="slow" repeat="1"/>
      <device mobile="true" tablet="true" desktop="true"/>
      <caption> Thunderstorm </caption>
      <credit> Nicholas Tesla </credit>
  </image>
</components>
```
