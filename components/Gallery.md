# Gallery

This is a component that is used to group images together.

## Attributes

| Attribute                  | Description                                                                                                                                                                                                |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_        | Id of the component                                                                                                                                                                                        |
| `role` <br/> _string_      | Role of the image </br> </br>_Possible values: `gallery`, `mosaic`_                                                                                                                                        |
| `bleed` <br/> _boolean_    | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |
| `direction` <br/> _string_ | Direction on which the gallery is going to move. </br> </br>_Possible values: `vertical`, `horizontal` (Default)._                                                                                         |

## Properties
| Property                                                          | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `items` <br/> _\[[GalleryItem](./gallery/GalleryItem.md)\]_       | **(Required)** List of images that appear in the gallery.   |
| `animation` <br/> _‌[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Control if a caption should be displayed in the content     |

## Example
```xml
<components>
	<gallery>
		<item src="bundle://images/item-1.jpg"/>
			<item src="bundle://images/item-2.jpg" width="500"/>
			<item src="bundle://images/item-3.jpg">
				<caption>This is an image</caption>
			</item>
			<item src="bundle://images/item-4.jpg">
				<credit>This is an image</credit>
			</item>
		<animation type="bounceIn" speed="slow" repeat="1"/>
		<device mobile="true" tablet="true" desktop="true"/>
		<caption> Thunderstorm </caption>
	</gallery>
</components>
```