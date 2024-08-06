# Audio Component

This component enables the user to add an audio component to the article.

## Attributes

| Attribute               | Description                                                                                                                                                                                                |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_     | Id of the component                                                                                                                                                                                        |
| `bleed` <br/> _boolean_ | This is a value that expresses whether the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |


## Elements

| Element                                                           | Description                                                       |
| :---------------------------------------------------------------- | :---------------------------------------------------------------- |
| `source` <br/> _‌[Audio Source](./audio/Source.md)_                | **(Required)** Applies the source of the audio component          |
| `animation` <br/> _‌[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                                |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which devices the component should be displayed.      |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Controls whether a `caption` should be displayed in the content   |
| `credit` <br/>_[Credit](../format/CreditDescriptor.md)_           | Controls whether a `credit` should be displayed in the content    |

_If the image is inside a gallery component the properties `animation` and `device` are ignored_

## Example

```xml
<components>
  <audio>
    <source>
      <file src="bundle://audio-sample.mp3"/>
    </source>
    <animation type="bounceIn" speed="slow" repeat="1"/>
    <device mobile="true" tablet="true" desktop="true"/>
    <caption> Rain </caption>
    <credit> Nick Eudovicii </credit>
  </audio>
</components>
```
