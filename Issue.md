# Issue

The Canvasflow Format for Issue is in XML format that enables the user to 
express an issue in a format that is understandable by Canvasflow.

This format enable user to group multiple articles,
[Table of Content](./issue/TOC.md), article ordering and 
replica [pages](./issue/Page.md)

Each article inside the issue follows 
the [Canvasflow Format for Article](./Article.md).

## Structure

The format constitutes of a `.zip` file with the extension `.issue` and this 
file consists on three parts, all required and must live in the root of the file.

|             |                                                                                                                                                                               |
| :---------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `issue.xml` | This is the entry point, and in here we are going to describe all the information required by the issue, the table of content and the article that are going to be processed. |
| `assets`    | This is the directory where all the media assets that are required by the issue and the articles are going to live.                                                           |
| `articles`  | This is the directory where all the articles reference are going to live.                                                                                                     |

This is an example of how the content of a `.issue` file looks like

```
example.issue
  issue.xml
  assets/
    image1.jpg
    pages/
      page-1.jpg
      page-2.jpg
  articles/
    article-1.xml
    article-2.xml
```

### Bundle Protocol

Along the entire format you will have reference for the protocol `bundle://`, 
this refers to the path for the `assets` directory.

For example let’s say that we have the following structure.

```
example.issue
  issue.xml
  assets/
    thumb.jpg
    image1.jpg
    pages/
      page-1.jpg
      page-2.jpg
  articles/
    article-1.xml
    article-2.xml
```

The file `bundle://thumb.jpg` is referencing the path `assets/thumb.jpg`. 

You can use the `bundle://` protocol in all the places that required the 
reference to any media file.

### Article Protocol

In the `issue.xml` file you will need to reference articles by using the 
`article://` protocol, this refers to the `articles` directory located at the 
root of the file.

In the `articles` directory you can have any level of directories but the only 
files that are stored in this directory must be article files. 

> If you want to store any other type of assets, save them in 
> the `assets` directory


## Attributes

| Attribute                  | Description                                                                      |
| :------------------------- | :------------------------------------------------------------------------------- |
| `lang` <br/> _string_      | Language of the issue                                                            |
| `slug` <br/> _string_      | Slug of the issue                                                                |
| `thumbnail` <br/> _string_ | Describes the route of the image that is going to be used as the issue thumbnail |

## Elements

| Element                                            | Description                                                                                                  |
| :------------------------------------------------- | :----------------------------------------------------------------------------------------------------------- |
| `metadata` <br/> ‌[_Metadata_](./issue/Metadata.md) | Metadata of issue                                                                                            |
| `toc` <br/> [_TOC_](./issue/TOC.md)                | Table of content that describe the articles that are going to be used and the pages that are linked to them. |

## Example

```xml
<?xml version='1.0' encoding='utf-8'?>
<issue 
  lang="en" 
  slug="example" 
  thumbnail="bundle://thumbnail.jpg">
  <metadata>
    <title>Example</title>
    <description>This is a description</description>
    <date type="creation">2024-10-25</date>
    <date type="release">2024-10-25</date>
  </metadata>
  <toc>
    <item href="article://article-1.xml" />
    <item href="article://article-2.xml">
      <pages>
        <page src="bundle://gareth.jpg" />
        <page src="bundle://articles/2/2.jpg" />
      </pages>
    </item>
    <item href="article://article-3.xml" />
    <item href="article://article-4.xml" />
    <item href="article://article-5.xml" />
    <item href="article://article-6.xml">
      <pages>
        <page src="bundle://articles/6/1.jpg" />
        <page src="bundle://articles/6/2.jpg" />
      </pages>
    </item>
    <item href="article://article-7.xml" />
    <item href="article://article-8.xml" />
    <item href="article://article-9.xml" />
    <item href="article://article-10.xml" />
  </toc>
</issue>
``` 

