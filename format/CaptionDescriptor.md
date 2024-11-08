# Caption Descriptor

Text component that describes what is shown in the 
[Image](../components/Image.md), [Gallery](../components/Gallery.md),
[GalleryItem](../components/gallery/GalleryItem.md) and
[Video](../components/Video.md) components. It uses the `<caption>` tag which 
the content inside the text component use `HTML` syntax.

## Attribute

| Properties                      | Description                                                                               |
| :------------------------------ | :---------------------------------------------------------------------------------------- |
| `only-lightbox` <br/> _boolean_ | Attributes that express if the caption should only be displayed when is inside a lightbox |

## Example

```xml
<components>
  <image src="bundle://images/image.jpg">
    <caption only-lightbox="true"> Into the sunset </caption>
  </image>
</components>
```