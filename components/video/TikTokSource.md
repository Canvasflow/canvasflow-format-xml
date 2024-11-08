# TikTok Video Source Component

This is a component that renders a TikTok video.


## Attributes

| Attribute              | Description                                                      |
| :--------------------- | :--------------------------------------------------------------- |
| `id` <br/> _uri_       | **(Required)** This the `id` of the TikTok video.                |
| `username` <br/> _uri_ | **(Required)** This is the `username` of the TikTok video author |

## Example

```xml
<components>
  <video>
    <source>
      <tiktok id="7224911609645354266" username="rose3brown"/>
    </source>
  </video>
</components>
```