# Article Metadata

In the metadata section the user describe all the information that is related 
to the article but do not required to be rendered. 

## Elements

| Element                     | Description                         |
| :-------------------------- | :---------------------------------- |
| `title` <br/> _string_      | **(Required)** Title of the article |
| `description` <br/>_string_ | Description of the article          |
| `author` <br/>_string_      | Author of the article               |
| `canonical` <br/>_URL_      | Canonical URL for the article       |
| `note` <br/>_string_        | Notes regarding for the article     |

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
		<author>Jane Doe</author>
		<canonical>https://google.com</canonical>
		<note>Example of a note</note>
	</metadata>
</article>
``` 
