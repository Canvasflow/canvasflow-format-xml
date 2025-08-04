# Meta

This element is used to represent metadata that cannot be represented by other meta-related elements like `title`, `description`, `author`, etc.

> This tag is a direct child of the `<metadata>` element.

## Attributes

This element relies on two required attributes, `name` and `content`.

> The `name` value must be unique across the different `<meta>` elements.
> If a `name` is repeated, the latest value is the one that is going to be assigned.

Below is a list of all supported attribute elements:

| Attribute                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name` <br/> _string_    | **(Required)** Name of the custom metadata                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `content` <br/> _string_ | **(Required)** Value that is going to be stored                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| `type` <br/> _string_    | Type that specifies how the value should be treated </br> </br>_Possible values: <ul><li>`text`: Process the content as a string.</li><li>`number`: Transform the content into a number; it gets ignored if the value is invalid.</li><li>`list`: Tries to transform comma-separated values into a list.</li><li>`json`: It should treat the content as a JSON object.</li><li>`html`: Is going to treat the content as an HTML text.</li><li>`date`: Tries to transform the content into an ISO 8601 date, which is going to be ignored if invalid.</li><li>`datetime`: Tries to transform the content into an ISO 8601 date time, which is going to be ignored if invalid.</li></ul>_ |

> If a `content` is not set, the custom metadata is going to be ignored.

> If a `type` is not specified, it will use `text` as the default.

```xml
<metadata>
  <meta name="company" content="ACME">
  <meta name="created" content="2007-01-09" type="date"/>
  <meta name="modified" content="2025-08-04T00:55:31.820Z" type="datetime">
</metadata>
```