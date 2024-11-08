# Video Source Component

This is a component specifies which video source to use


## Elements

| Element                                      | Description                                                                                                                                                                                                                                                                                                                                |
| :------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `source` <br/> _‌[Video Source](./Source.md)_ | Specify the source of the video component. <br/><br/> _Only once source can be set a time, if multiple are set the first one is the one that is going to be accepted._ </br> </br>_Possible values: <br> [Local Video Source](./LocalSource.md), [TikTok Video Source](./TikTokSource.md), [Instagram Video Source](./InstagramSource.md)_ |

## Example

```xml
<components>
  <video>
    <source>
      <file src="bundle://video-example.mp4"/>
    </source>
  </video>
  <video>
    <source>
      <instagram id="CoxIGcuK7c9" type="post"/>
    </source>
  </video>
  <video>
    <source>
      <tiktok id="7224911609645354266" username="rose3brown"/>
    </source>
  </video>
</components>
```