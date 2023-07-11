# Text Component

This is a component that is used to display text content. The content inside the text component use `HTML` syntax and should be wrapped in `<p>` tags.

## Attributes

| Attribute                 | Description                                                                                                                                                                                                                                                     |
| :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_       | Id of the component                                                                                                                                                                                                                                             |
| `type` <br/> _string_     | Is the type of the component that is going to be used. If not set is going to be used the value `body` as default. </br> </br>_Possible values: `headline`, `title`, `subtitle`, `intro`, `crosshead`, `byline`, `blockquote`, `footer`, `body`, `text{1-60}`._ |
| `dropcap` <br/> _boolean_ | This is a value that express if the component should use a drop cap                                                                                                                                                                                             |
| `bleed` <br/> _boolean_   | This is a value that express if the component should bleed in the document. _Bleed is only valid at the root level, bleed will be automatically be turn to `false` if the component is inside a `column`._                                                      |

## Properties
| Property                                                          | Description                                                 |
| :---------------------------------------------------------------- | :---------------------------------------------------------- |
| `animation` <br/> _[Animation](../format/AnimationDescriptor.md)_ | Applies animation to the component                          |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_           | Controls in which device the component should be displayed. |


## Example
```xml
<article>
  <components>
    <text type="crosshead" bleed="true">
      <device mobile="false" tablet="false" desktop="true" />
      <p>Crosshead that only display in desktop</p>
    </text>
    <text type="headline">
      <p>This is a headline</p>
    </text>
    <text type="body">
      <animation type="bounceIn" speed="slow" repeat="1" />
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing
        elit. Praesent a augue et nulla vehicula tempor vel
        ultrices sem. Duis cursus diam id mi pharetra, sit
        amet aliquam sem luctus. Aliquam erat volutpat. In
        ullamcorper bibendum erat ut gravida. Nunc sit amet
        fringilla arcu. Etiam commodo ultricies tellus vitae
        consequat. Nulla sed ipsum ac elit egestas auctor
        a ut tellus.
      </p>
      <p>
        <ul>
          <li>Item 1</li>
          <li>Item 2</li>
        </ul>
      </p>
    </text>
    <text type="footer">
      <animation type="bounceIn" speed="slow" repeat="1" />
      <p>Footer with animation</p>
    </text>
  </components>
</article>
```