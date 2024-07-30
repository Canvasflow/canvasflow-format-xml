# Video Component

This is a component enables user to add video to the article.

## Attributes

| Attribute                  | Description                                                                                                                                                                                                |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_        | Id of the component                                                                                                                                                                                        |
| `web` <br/> _boolean_      | Declares if the video is from a web source or a local file.                                                                                                                                                |
| `autoplay` <br/> _boolean_ | Declares if the should start as soon is loaded                                                                                                                                                             |
| `loop` <br/> _boolean_     | Declares if the should be looped                                                                                                                                                                           |
| `controls` <br/> _boolean_ | Declares if the should enable the controls                                                                                                                                                                 |
| `width` <br/> _number_     | Width of the video in the article                                                                                                                                                                          |
| `height` <br/> _number_    | Height of the video in the article                                                                                                                                                                         |
| `bleed` <br/> _boolean_    | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |


## Elements

| Element                                                           | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `source` <br/> _‌[Video Source](./video/Source.md)_                | Applies the source of the video component                   |
| `animation` <br/> _‌[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Control if a `caption` should be displayed in the content   |
| `credit` <br/>_[Credit](../format/CreditDescriptor.md)_           | Control if a `credit` should be displayed in the content    |

_If the image is inside a gallery component the properties `animation` and `device` are going to be ignored_

## Example

```xml
<components>
  <video width="500">
    <source>
      <file src="bundle://video-example.mp4"/>
    </source>
    <animation type="bounceIn" speed="slow" repeat="1"/>
    <device mobile="true" tablet="true" desktop="true"/>
    <caption> Thunderstorm </caption>
    <credit> Nicholas Tesla </credit>
  </video>
</components>
```