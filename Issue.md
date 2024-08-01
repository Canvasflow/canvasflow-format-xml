# Issue

**Issue Format** is an XML format that enables the user to express an issue in a format that is understandable by Canvasflow.

This format enables user to group multiple articles, [Table of Content](./issue/TOC.md), article ordering and [Replica Pages](./issue/Page.md)

Each article inside the issue follows the [Canvasflow Format for Article](./Article.md).

## Structure

The format consists of a `.zip` file with the extension `.issue` and is made up of three parts.  All parts are required and must live in the root of the file.

|             |                                                                                                                                                                               |
| :---------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `issue.xml` | This is the entry point, and in here we are going to describe all the information required by the issue, the table of content and the article that are going to be processed. |
| `assets`    | This is the directory where all media assets required by the issue and articles live.                                                           |
| `articles`  | This is the directory where all the article references live.                                                                                                     |

Below is an example of how the contents of a `.issue` file looks:

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

For example, let’s assume we have the following structure:

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

The file `bundle://thumb.jpg` references the path `assets/thumb.jpg`. 

You can use the `bundle://` protocol in places that require the 
reference to a media file.

### Article Protocol

In the `issue.xml` file you need to reference articles by using the 
`article://` protocol, this refers to the `articles` directory which is located in the 
root of the file.

In the `articles` directory you can have any number of directories, but only article files
should be stored in this directory. 

> If you want to store any other type of assets, store them in 
> the `assets` directory


## Attributes

| Attribute                  | Description                                                                      |
| :------------------------- | :------------------------------------------------------------------------------- |
| `lang` <br/> _string_      | Language of the issue                                                            |
| `slug` <br/> _string_      | Slug of the issue                                                                |
| `thumbnail` <br/> _string_ | Describes the route of the image that will be used as the issue thumbnail |

## Elements

| Element                                            | Description                                                                                                  |
| :------------------------------------------------- | :----------------------------------------------------------------------------------------------------------- |
| `metadata` <br/> ‌[_Metadata_](./issue/Metadata.md) | Metadata of the issue                                                                                            |
| `toc` <br/> [_TOC_](./issue/TOC.md)                | Table of content which describes the articles that are going to be used and the pages that are linked to them. |

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

