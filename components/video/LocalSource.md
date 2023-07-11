# Local Video Source Component

This is a component that specifies which file is going to be used to load the video component, it can be a local file like an `.mp4` or a remote address to a file.

## Attributes
| Attribute         | Description                                                                                                                                                                                                       |
| :---------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `src` <br/> _uri_ | **(Required)** The URL of the video file </br></br> Video URL can begin with `http://`, `https://` or `bundle://`. If the vide begin with `bundle://`, the video reference must be relative to the `assets` path. |

## Example
```xml
<components>
  <video>
    <source>
      <file src="bundle://video-example.mp4"/>
    </source>
  </video>
</components>
```