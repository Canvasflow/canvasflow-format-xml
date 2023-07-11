# Credit Descriptor

Text component that describes who was the author of the 
[Image](../components/Image.md), [Gallery](../components/Gallery.md),
[GalleryItem](../components/gallery/GalleryItem.md) and 
[Video](../components/Video.md) components. It uses the `<credit>` tag which 
the content inside the text component uses `HTML` syntax.

## Attribute

| Properties                      | Description                                                                              |
| :------------------------------ | :--------------------------------------------------------------------------------------- |
| `only-lightbox` <br/> _boolean_ | Attributes that express if the credit should only be displayed when is inside a lightbox |

## Example
```xml
<components>
  <image src="bundle://images/image.jpg">
    <credit only-lightbox="true"> J.J. Adams </credit>
  </image>
</components>
```