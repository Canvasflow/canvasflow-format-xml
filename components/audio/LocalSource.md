# Local Audio Source Component

This is a component that specifies which file is going to be used to load the 
audio component, it can be a local file like an `.mp3` or a remote address to 
a file.

## Attributes
| Attribute         | Description                                                                                                                                                                                                        |
| :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `src` <br/> _uri_ | **(Required)** The URL of the audio file </br></br> Audio URL can begin with `http://`, `https://` or `bundle://`. If the video begin with `bundle://`, the audio reference must be relative to the `assets` path. |

## Example
```xml
<components>
	<audio>
		<source>
			<file src="bundle://audio-sample.mp3"/>
		</source>
	</audio>
</components>
```