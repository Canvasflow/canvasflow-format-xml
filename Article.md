# Article

**Article Format** is in XML format that enables the user to express an article 
in a format that is understandable for Canvasflow.

An article that is created in a Canvasflow Format support text, image, audio, 
video, galleries and the content can be enhance with animation.

The article is created by wrapping the content of the article in a 
`<article>` tag and saved in the file `article.xml`

## Structure

The format constitutes of a `.zip` file with the extension `.article` and 
this file consists on two parts, both are required and both must live in the 
root of the file.

|               |                                                                                                                  |
| :------------ | :--------------------------------------------------------------------------------------------------------------- |
| `article.xml` | This is the entry point, and in here we are going to describe all the information that is related to the article |
| `assets`      | This is the directory where all the media assets that are required by the article are going to live.             |

This is an example of how the content of a `.article` file looks like

```
example.article
  article.xml
  assets/
    image1.jpg
```

### Bundle Protocol

Along the entire format you will have reference for the protocol `bundle://`, 
this refers to the path for the `assets` directory.

For example let’s say that we have the following structure.

```
example.article
  article.xml
  assets/
    thumb.jpg
    image.jpg
```

The file `bundle://thumb.jpg` is referencing the path `assets/thumb.jpg`. 

You can use the `bundle://` protocol in all the places that required the 
reference to any media file.

## Attributes

| Attribute                   | Description                                                                                                 |
| :-------------------------- | :---------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_         | Id of the article                                                                                           |
| `lang` <br/> _string_       | Language of the article                                                                                     |
| `slug` <br/> _string_       | Slug of the article                                                                                         |
| `role` <br/> _string_       | Defines the role of the article </br> </br>Values: <ul><li>`article` _(Default)_</li><li>`‌advert`</li></ul> |
| `featured` <br/> _boolean_  | Mark if an article is a feature article                                                                     |
| `sponsored` <br/> _boolean_ | Mark if an article is sponsored                                                                             |
| `thumbnail` <br/> _string_  | Reference to the image that is going to be used as a thumbnail                                              |

## Elements

| Element                                                   | Description               |
| :-------------------------------------------------------- | :------------------------ |
| `metadata` <br/>_[Metadata](./article/Metadata.md)_       | Metadata of article       |
| `components` <br/>[_[Component](./article/Component.md)_] | Components of the article |


## Example

```xml
<?xml version='1.0' encoding='utf-8'?>
<article
  lang="en"
  slug="example" 
  role="article" 
  featured="true"
  sponsored="true"
  thumbnail="bundle://thumb.jpg">
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

