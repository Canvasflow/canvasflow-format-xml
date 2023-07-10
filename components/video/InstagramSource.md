# Instagram Video Source Component

This is a component that renders a Instagram live tv, reel or post.


## Attributes
| Attribute             | Description                                                                              |
| :-------------------- | :--------------------------------------------------------------------------------------- |
| `id` <br/> _string_   | **(Required)** This the `id` of the TikTok resource.                                     |
| `type` <br/> _string_ | This the type of asset. </br> </br>_Possible values: <br> `post`(default), `reel`, `tv`_ |

## Example
```xml
<components>
	<video>
		<source>
			<instagram id="CoxIGcuK7c9" type="post"/>
		</source>
	</video>
</components>
```