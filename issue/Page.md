# Page

Denotes where the issue page is located.

## Attributes

| Attribute            | Description                                                                      |
| :------------------- | :------------------------------------------------------------------------------- |
| `src` <br/> _string_ | **(Required)** Source of the image, it must begin with the `bundle://` protocol. |

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
