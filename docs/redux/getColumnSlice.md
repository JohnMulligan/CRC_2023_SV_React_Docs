# Redux Store: getColumnsSlice

This code snippet defines a Redux slice for managing columns in a table. 
It exports actions and a reducer for manipulating the state related to table columns.


## Dependencies
This code relies on the following dependencies:

- `@reduxjs/toolkit`: A Redux utility library that simplifies the process of creating Redux stores, actions, and reducers.

## Getting Started
To use this code in your Redux-based application, follow the steps below:

1) Import the necessary types and the JSON data file:
```jsx
import { InitialStateColumnProps, TableCellStructureProps } from '@/share/InterfaceTypesTable';
import jsonDataTable from '@/utils/flatfiles/voyage_table_cell_structure__updated21June.json';

```
2) Define the initial state of the columns:
```jsx
export const initialState: InitialStateColumnProps = {
    valueCells: jsonDataTable,
    visibleColumnCells: []
};

```
3) Create a Redux slice using createSlice:

```jsx
export const getColumnsSlice = createSlice({
    name: 'getColumns',
    initialState,
    reducers: {
        setColumnsSelectorTree: (state, action: PayloadAction<TableCellStructureProps>) => {
            state.valueCells = action.payload;
        },
        setVisibleColumn: (state, action: PayloadAction<string[]>) => {
            state.visibleColumnCells = action.payload;
        },
    },
});

```

4) Export the actions and reducer:
```jsx
export const { setVisibleColumn, setColumnsSelectorTree } = getColumnsSlice.actions;
export default getColumnsSlice.reducer;

```

## Actions
The following actions are available for manipulating the state related to table columns:

- `setColumnsSelectorTree`: Sets the column values in the state based on the provided payload of type `TableCellStructureProps`.
- `setVisibleColumn`: Sets the visible columns in the state based on the provided payload of type `string[]`.


## Reducer
The reducer returned by this code manages the state of columns. It handles the actions defined in the slice and updates the state accordingly.
```jsx
export default getColumnsSlice.reducer;

```

## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing table columns. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.