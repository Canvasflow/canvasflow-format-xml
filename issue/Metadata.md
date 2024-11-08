# Issue Metadata

Describe what is the metadata for the canvasflow issue

## Elements

| Element                     | Description                                                                                                                                                                                                                                                                                                                  |
| :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `title` <br/> _string_      | Title of the issue                                                                                                                                                                                                                                                                                                           |
| `description` <br/>_string_ | Description of the issue                                                                                                                                                                                                                                                                                                     |
| `date` <br/> _string_       | Describe date information for the issue. The date must have the format `YYYY-MM-DD`. <br/><br/> Their possible `type` attributes are: <ul><li>`creation`: When the article was created.</li><li>`release`: When the article is supposed to be publish.</li></ul><br/> _If the date is not set is going to use today’s date._ |

## Example

```xml
<issue>
  <metadata>
    <title></title>
    <description></description>
    <date type="creation">2007-01-09</date>
    <date type="release">2007-01-09</date>
  </metadata>
</issue>
``` 
