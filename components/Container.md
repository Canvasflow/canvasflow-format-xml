# Container

This is a component that is used to group other components.

## Attributes

| Attribute                  | Description                                                                                                                                                                                                                                                                                                |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id` <br/> _string_        | Id of the component                                                                                                                                                                                                                                                                                        |
| `direction` <br/> _string_ | This is the direction in which the components are going to be displayed. </br></br> Values: <ul><li>`vertical` _(Default)_: Components will appear on top of each other.</li><li>`horizontal`: Components will appear next to each other</li></ul>                                         |
| `bleed` <br/> _boolean_    | This is a value that expresses whether the component should bleed in the document. _Bleed is only valid at the root level, bleed will be set to `false` if the component is inside a `column`._<br><br> **CAUTION: This is supported in the specification but is not supported in the editor.** |


## Elements

| Element                                                 | Description                                                                                                                                                  |
| :------------------------------------------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `device` <br/>_[Device](../format/DeviceDescriptor.md)_ | Controls in which devices the component should be displayed. <br><br> **CAUTION: This is supported in the specification but is not supported in the editor.** |


## Example

```xml
<components>
	<container bleed="true" direction="vertical">
		<device mobile="false" tablet="false" desktop="true" />
		<text type="body">
			<p>This is a text</p>
		</text>
		<text type="body">
			<p>This is a another text</p>
		</text>
	</container>
</components>
```
