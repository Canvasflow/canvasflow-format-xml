# Canvasflow Article Format

The Canvasflow Article Format is in `XML` format that enables the user to express 
an article in a format that is understandable for Canvasflow.

An article that is created in a Canvasflow format support text, image, audio, 
video, galleries and the content can be enhance with animation.

The article is created by wrapping the content of the article in a `<article>` 
tag, a language can be specified by using the `lang` attribute.

```xml
<?xml version='1.0' encoding='utf-8'?>
<article lang="en">
</article>
``` 

The article is divide in two big sections:
- `metadata` 
- `components`

## Metadata 

In the metadata section the user describe all the information that is related 
to the article but do not required to be rendered. 

```xml
<?xml version='1.0' encoding='utf-8'?>
<article lang="en">
  <metadata>
    <title>This is an example of the title</title>
    <description> Description of the article </description>
  </metadata>
</article>
``` 

| Element       | Description                                                              |
| :------------ | :----------------------------------------------------------------------- |
| `title`       | Describes what is the title of the article that is going to be processed |
| `description` | It describes the content of the article                                  |


## Components

Components are the main object that you use to build your article, and 
are wrap in the `<components>` element.

| Component                          | Description                                   |
| :--------------------------------- | :-------------------------------------------- |
| [Text](./components/Text.md)       | Used to display text content                  |
| [Image](./components/Image.md)     | Used to display images                        |
| [Video](./components/Video.md)     | Used to display videos                        |
| [Gallery](./components/Gallery.md) | Used to display group of images               |
| [Audio](./components/Audio.md)     | Used to display audio                         |
| [Divider](./components/Divider.md) | Used to display divider between components    |
| [Spacer](./components/Spacer.md)   | Used to display space between components      |
| [Map](./components/Map.md)         | Used to display maps                          |
| Button                             | Used to display buttons                       |
| Columns                            | Used to display columns that group components |


### Example

```xml
<?xml version='1.0' encoding='utf-8'?>
<article lang="en">
  <metadata>
    <title>This is an example of the title</title>
    <description> Description of the article </description>
  </metadata>
  <components>
    <text type="headline">
      <p>Headline<p/>
    </text>
    <text>
      <p>This is the body of the article</p>
    </text>
  </components>
</article>
``` 

