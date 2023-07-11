# Gallery Item Component

This component is used to display image in the [Gallery Component](../Gallery.md)

## Attributes

| Attribute               | Description                                                                                                                                                                                                        |
| :---------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_     | Id of the component                                                                                                                                                                                                |
| `role` <br/> _string_   | Role of the image </br> </br>_Possible values: `image`, `photo`, `figure`, `portrait`, `logo`, `thumbnail`_                                                                                                        |
| `width` <br/> _number_  | Width of the item in the gallery                                                                                                                                                                                   |
| `height` <br/> _number_ | Height of the item in the gallery                                                                                                                                                                                  |
| `src` <br/> _uri_       | **(Required)** The URL of the image file </br></br> Image URL can begin with `http://`, `https://` or `bundle://`. If the image begin with `bundle://`, the image reference must be relative to the `assets` path. |


## Properties
| Property                                                      | Description                                             |
| :------------------------------------------------------------ | :------------------------------------------------------ |
| `caption` <br/>_[Caption](../../format/CaptionDescriptor.md)_ | Control if a caption should be displayed in the content |
| `credit` <br/>_[Credit](../../format/CreditDescriptor.md)_    | Control if a credit should be displayed in the content  |

_If the image is inside a gallery component the properties `animation` and `device` are going to be ignored_

## Example
```xml
<components>
	<gallery>
		<items>
			<item src="bundle://images/item-1.jpg"/>
			<item src="bundle://images/item-2.jpg" width="500"/>
			<item src="bundle://images/item-3.jpg">
				<caption>This is an image</caption>
			</item>
			<item src="bundle://images/item-4.jpg">
				<credit>This is an image</credit>
			</item>
		</items>
		<animation type="bounceIn" speed="slow" repeat="1"/>
		<device mobile="true" tablet="true" desktop="true"/>
		<caption> Thunderstorm </caption>
	</gallery>
</components>
```