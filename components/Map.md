# Map Component

This component is used to display a map in the article.

## Attributes

| Attribute                  | Description                                                                                                                                                                                                |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_        | Id of the component                                                                                                                                                                                        |
| `latitude` <br/> _number_  | **(Required)** The latitude of the map’s center.                                                                                                                                                           |
| `longitude` <br/> _number_ | **(Required)** The longitude of the map’s center.                                                                                                                                                          |
| `width` <br/> _number_     | Width of the map in the article                                                                                                                                                                            |
| `height` <br/> _number_    | Height of the map in the article                                                                                                                                                                           |
| `zoom` <br/> _number_      | Zoom level of the map. <br/><br/> _Possible values: Between 1-10_                                                                                                                                          |
| `bleed` <br/> _boolean_    | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._ |

## Properties
| Property                                                          | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `markers` <br/> _\[[MapMarker](./map/MapMarker.md)\]_             | List of markers that appear in the map.                     |
| `animation` <br/> _‌[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |
| `caption` <br/>_[Caption](../format/CaptionDescriptor.md)_        | Control if a caption should be displayed in the content     |

## Example
```xml
<components>
  <map zoom="5" latitude="48.85827830746261" longitude="2.2942667208178773">
    <markers>
      <marker latitude="48.85827830746261" longitude="2.2942667208178773">
        <caption>Eiffel Tower</caption>
      </marker>
      <marker latitude="48.85761477995638" longitude="2.2957902154025494"/>
    </markers>
    <caption>Eiffel Tower Paris</caption>
  </map>
</components>
```