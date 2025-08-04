# Meta

This element is used to represent metadata that cannot be represented by other meta-related elements, eg. `title`, `description`, `author`, etc.

> This tag is a direct child of the `<metadata>` element.

## Attributes

This element relies on two required attributes, `name` & `content`.

> The `name` value must be unique across the different `<meta>` elements.
> If `name` is repeated the latest value will be assigned.

Below is a list of all supported attribute elements:

| Attribute                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name` <br/> _string_    | **(Required)** Name of the custom metadata                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `content` <br/> _string_ | **(Required)** Value that will be stored                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| `type` <br/> _string_    | specifies how the value should be treated </br> </br>_Possible values: <ul><li>`text`: Processes the content as a string.</li><li>`number`: Transforms the content into a number (ignored if the value is invalid).</li><li>`list`: Transforms comma-separated values into a list.</li><li>`json`: Treats content as a JSON object.</li><li>`html`: Treats the content as an HTML text.</li><li>`date`: Transforms the content into an ISO 8601 date (ignored if invalid).</li><li>`datetime`: Transforms the content into an ISO 8601 date time (ignored if invalid).</li></ul>_ |

> If `content` is not defined the custom metadata will be ignored.

> If `type` is not specified the service will default to `text`.

```xml
<metadata>
  <meta name="company" content="ACME">
  <meta name="created" content="2007-01-09" type="date"/>
  <meta name="modified" content="2025-08-04T00:55:31.820Z" type="datetime">
</metadata>
```