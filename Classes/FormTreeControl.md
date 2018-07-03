# The FormTreeControl

## Drag-and-drop

As of July 3th, the drag-and-drop functionality doesn't work. If you want similar functionality you can use buttons to copy/cut and paste elements.

## Multi-select

### Looping through selected tree items

As of July 3th, the **getNextSelected()**, used to loop through the selected tree items doesn't work. If you want similar functionality you can use a grid control, hidden or preferably visible, along with your Tree control. A tree item should carry a RecId, in its **data()** method, which corresponds to an entry in the grid. On a tree item click the correpsonding item in the grid can be marked and later you can loop through all the marked elements in the grid.