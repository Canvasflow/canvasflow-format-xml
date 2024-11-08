# Columns

This component is used to group components into columns.

## Attributes

| Attribute                 | Description                                                                                                                                                                                                                                                                       |
| :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_       | Id of the component                                                                                                                                                                                                                                                               |
| `split` <br/> _string_    | Is the representation of the split in the columns, this values must be split using `-`. The values are a representation of the weight of each columns. _The amount of weights must be equal to the amount of columns._                                                            |
| `bleed` <br/> _boolean_   | This is a value that expresses whether the component should bleed in the document. _Bleed is only valid at the root level, bleed will be set to `false` if the component is inside a `column`._                                                                        |
| `align` <br/> _string_    | Set the alignment of the columns. </br> </br>Values: <ul><li>`center` _(Default)_</li><li>`left`</li><li>`right`</li></ul>                                                                                                                                                        |
| `collapse` <br/> _string_ | Controls when the columns should collapse onto each other. </br> </br>Values: <ul><li>`responsive` _(Default)_: The columns collapse when they are in a mobile device.</li><li>`tablet`: The columns collapse when they are in a tablet size or smaller.</li><li>`rigid`</li></ul> |

## Elements

| Element                                                 | Description                                                                         |
| :------------------------------------------------------ | :---------------------------------------------------------------------------------- |
| `column`                                                | **(Required)** Represents a column that is going to contain a group of components.  |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which devices the component should be displayed.                        |

## Example

```xml
<components>
	<columns
		bleed="true"
		split="1-1"
		align="left"
		collapse="never">
		<device mobile="false" tablet="false" desktop="true" />
		<column>
			<text type="crosshead">
				<p>This is a text in the first column</p>
			</text>
		</column>
		<column>
			<text type="body">
				<p>This is a text in the second column</p>
			</text>
		</column>
	</columns>
</components>
```
