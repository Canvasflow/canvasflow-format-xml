# TOC Item

Describe the items in the table of content

## Attributes

| Attribute             | Description                                                                                          |
| :-------------------- | :--------------------------------------------------------------------------------------------------- |
| `href` <br/> _string_ | **(Required)** Reference where the article is located. It must begin with the `article://` protocol. |

## Elements

| Element                             | Description                                         |
| :---------------------------------- | :-------------------------------------------------- |
| `pages` <br/> [_[Page](./Page.md)_] | List all the pages that are related to the article. |

## Example

```xml
<issue lang="en">
  <toc>
    <item href="article://article-1.xml">
      <pages>
        <page src="bundle://pages/1.jpg" />
      </pages>
    </item>
  </toc>
</issue>
``` 
