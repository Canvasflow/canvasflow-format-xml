# Gallery

This is a component that is used to group images together.

## Attributes

| Attribute                  | Description                                                                                                                                                                                                |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `role` <br/> _string_      | Role of the image </br> </br>_Possible values: `gallery`, `mosaic`_                                                                                                                                        |
| `bleed` <br/> _boolean_    | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |
| `direction` <br/> _string_ | Direction on which the gallery is going to move. </br> </br>_Possible values: `vertical`, `horizontal` (Default)._                                                                                         |

## Properties
| Property                                                          | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `items` <br/> \[[Image](Image.md)\]                               | **(Required)** List of images that appear in the gallery.   |
| `animation` <br/> _‌[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Control if a caption should be displayed in the content     |

## Example
```xml
<components>
	<gallery>
		<items>
			<image src="bundle://images/item-1.jpg"/>
			<image src="bundle://images/item-2.jpg"/>
			<image src="bundle://images/item-3.jpg"/>
		</items>
		<animation type="bounceIn" speed="slow" repeat="1"/>
		<device mobile="true" tablet="true" desktop="true"/>
		<caption> Thunderstorm </caption>
	</gallery>
</components>
```