# Meta

This element is used to represents metadata that cannot be represented by other meta-related elements like `title`, `description`, `author`, etc.

> This tags is a direct child of the `<metadata>` element

## Attributes

This relement relies on two required attributes `name` and `content`.

> The `name` value must be unique across the different `<meta>` element.
> If a `name` is repeated the latest value is the one that is going to be assigned.

Below is a list of all supported component types:

| Attribute                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :----------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name` <br/> _string_    | **(Required)** Name of the custom metadata                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| `content` <br/> _string_ | **(Required)** Value that is going to be stored                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| `type` <br/> _string_    | Type that specify how the value should be treated </br> </br>_Possible values: <ul><li>`text`: Process the content as a string.</li><li>`number`: Transform the content into a number, it get's ignored if the value is invalid.</li><li>`list`: Tries to transform comma separated values into a list.</li><li>`json`: It should treat the content as a json object.</li><li>`html`: Is going to treat the content as an html text.</li><li>`date`: Tries to transform the content into a ISO 8601 date, is going to be ignored if invalid.</li><li>`datetime`: Tries to transform the content into a ISO 8601 date time, is going to be ignored if invalid.</li></ul>_ |

> If a `content` is not set the custom metadata is going to be ignored
> If a `type` is not specified is going to use `text` as default