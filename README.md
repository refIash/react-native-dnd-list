# react-native-dnd-list

React Native DnD list sample implementation. It developed for my application and I am a bit lazy to create an npm module for it.

## Usage

Look into ```DnDTestScreen.js``` -- everything is in this file.

You should extract the ```DnDList``` class as a standalone component. The usage in a nutshell:

```javascript
<DnDList
	ref={(ref) => this.list1 = ref}
	rows={this.rows1}
	itemSize={this.itemSize1}
	deleteRow={this.deleteRow1}
	renderRow={this.renderRow}
	isDraggable={this.isDraggable}
	isDeletable={this.isDraggable}
	isAcceptItem={this.isAcceptItem}
	handleDrop={this.handleDrop1}
	horizontal={!true}
	noDragHandle={!true}
/>
```
## Properties ##
- **rows**:  
array of items in the list. 
- **itemSize**:  
callback function to get the size of the item. Parameter: item index. Returns the size of the given item (width if horizontal, height if vertical)
- **deleteRow**:  
callback function to delete a row. Parameter: item index. Returns the new item array (see ***rows***)
- **renderRow**:  
callback function to render a given item. Parameter: item. Returns the row component
- **isDraggabl**:  
callback function to decide if an item is draggable. Parameter: item. Returns true/false
- **isDeletable**:  
callback function to decide if an item is deletable. Parameter: item. Returns true/false
- **isAcceptItem**:  
callback function to decide if an item accepts another. Parameter: targetItem, draggedItem. Returns true/false
- **handleDrop**:  
callback function to handle the drop.
Parameters:from, to indexes. Returns the new item array (see ***rows***)
- **horizontal**:  
the list is horizontal or vertical. Default false
- **noDragHandle**:  
if true it will not draw a drag handle on list.edit true. Instead of the whole row can be draggable. Good for small items, for example horizontal image stripe.

## Instance Properties ##

- **editable**:  
boolean. Turns drag/delete handle

## In Action 
(click on the image to view the video)

<p align="center">
	<a href="https://www.youtube.com/watch?v=zENIPUrGgiA">
		<img src="https://img.youtube.com/vi/zENIPUrGgiA/0.jpg" alt="Image Editor">
	</a>
	<p align="center">
		Vertical/Horizontal DnD lists
	</p>
</p>
