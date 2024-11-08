# Advert

This component is used to display an image in the article.

## Attributes

| Attribute                      | Description                                                                                                                                                                                                          |
| :----------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_            | Id of the component                                                                                                                                                                                                  |
| `src` <br/> _uri_              | **(Required)** The URL of the image file </br></br> Advert URL can begin with `http://`, `https://` or `bundle://`. If the image begins with `bundle://`, the image reference must be relative to the `assets` path. |
| `href` <br/> _uri_             | The URL to which the advert targets</br></br>The URL can begin with `http://` or `https://`                                                                                                                          |
| `bleed` <br/> _boolean_        | This is a value that expresses whether a component should bleed in the document. _Bleed is only valid at the root level, bleed will automatically be turned to `false` if the component is inside a `column`._       |
| `unselectable` <br/> _boolean_ | Value that expresses whether the image can be selected.                                                                                                                                                              |


## Elements

| Element                                                           | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `animation` <br/> _[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |

## Example

```xml
<components>
  <advert 
    id="CF-12345667"
    src="bundle://images/canvasflow.jpg"
    href="https://canvasflow.io"
    bleed="false" 
    unselectable="false" >
      <animation type="bounceIn" speed="slow" repeat="1"/>
      <device mobile="true" tablet="true" desktop="true"/>
  </advert>
</components>
```
