# Audio Source Component

This is a component specifies which audio source to use


## Properties
| Property                                     | Description                                                                                                                                                                                                                                  |
| :------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `source` <br/> _‌[Audio Source](./Source.md)_ | Specify the source of the audio component. <br><br> _Only once source can be set a time, if multiple are set the first one is the one that is going to be accepted._ </br> </br>_Possible values: <br> [Local Audio Source](LocalSource.md)_ |

## Example
```xml
<components>
	<video>
		<source>
			<file src="bundle://video-example.mp4"/>
		</source>
</components>
```