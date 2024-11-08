# TOC

Describes the table of content for the issue, which controls the article order and the replica pages.

## Elements

| Element                                | Description                               |
| :------------------------------------- | :---------------------------------------- |
| `item` <br/> _[Item](<./TOC Item.md>)_ | Describe the item in the table of content |

## Example

```xml
<issue lang="en">
  <toc>
    <item href="article://article-1.xml">
      <pages>
        <page src="bundle://pages/1.jpg" />
      </pages>
    </item>
    <item href="article://article-2.xml"/>
  </toc>
</issue>
``` 