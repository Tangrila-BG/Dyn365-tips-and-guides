# The table control

## Updating table cell(s)

As of July 3th, the **update()** method doesn't work. When you want to update all the cells in your table you should loop over every cell and call the **updateCell()** method on it.