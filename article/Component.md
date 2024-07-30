# Article Component

Components are the main object that you use to build your article, and are 
wrap in the `<components>` element.

This are all the components that are supported:

| Component                                 | Description                                     |
| :---------------------------------------- | :---------------------------------------------- |
| [Text](./../components/Text.md)           | Used to display text content                    |
| [Image](./../components/Image.md)         | Used to display images                          |
| [Video](./../components/Video.md)         | Used to display videos                          |
| [Gallery](./../components/Gallery.md)     | Used to display group of images                 |
| [Audio](./../components/Audio.md)         | Used to display audio                           |
| [Divider](./../components/Divider.md)     | Used to display divider between components      |
| [Spacer](./../components/Spacer.md)       | Used to display space between components        |
| [Map](./../components/Map.md)             | Used to display maps                            |
| [Columns](./../components/Columns.md)     | Used to display columns that group components   |
| [Container](./../components/Container.md) | Used to display container that group components |
| Button                                    | Used to display buttons                         |

## Example

```xml
<components>
  <text type="headline">
    <p>Headline<p/>
  </text>
  <text>
    <p>This is the body of the article</p>
  </text>
</components>
``` 
