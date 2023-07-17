## Table Data Redux Slice
This code defines a Redux slice for managing table data and configuration. The slice is created using the `createSlice` function from the `@reduxjs/toolkit` library.

## Usage
To use this Redux slice, follow these steps:

1) Import the necessary modules and types:
```jsx 
import { createSlice, PayloadAction } from '@reduxjs/toolkit';
import { ColumnDef, StateRowData, VoyageOptionsGropProps } from '@/share/InterfaceTypesTable';
import { ColumnObjectProps } from '@/share/InterfaceTypes';

```
2) Define the initial state for the table data:
```jsx
const initialState: StateRowData = {
    data: [],
    rowData: [],
    columnDefs: [],
    tableOptions: {}
};

```
3) Create the Redux slice using the createSlice function:

```jsx
export const getTableSlice = createSlice({
    name: 'getTableData',
    initialState,
    reducers: {
        setData: (state, action: PayloadAction<VoyageOptionsGropProps[]>) => {
            state.data = action.payload;
        },
        setRowData: (state, action: PayloadAction<Record<string, any>[]>) => {
            state.rowData = action.payload;
        },
        setColumnDefs: (state, action: PayloadAction<ColumnDef[]>) => {
            state.columnDefs = action.payload;
        },
        setTableOptions: (state, action: PayloadAction<ColumnObjectProps>) => {
            state.tableOptions = action.payload;
        },
    },
});

```
4) Export the action creators and reducer from the slice:

```jsx
export const {
    setData,
    setRowData,
    setColumnDefs,
    setTableOptions
} = getTableSlice.actions;

export default getTableSlice.reducer;

```

## State Structure
The state structure of the table data slice is as follows:

- `data`: An array representing the table data.
- `rowData`: An array representing the row data.
- `columnDefs`: An array representing the column definitions for the table.
- `tableOptions`: An object representing the options and configuration for the table.


## Actions
This Redux slice defines several actions:

`setData`: Sets the table data.
`setRowData`: Sets the row data.
`setColumnDefs`: Sets the column definitions for the table.
`setTableOptions`: Sets the options and configuration for the table.

## Reducer
The reducer function in this slice updates the state with the payload received from the corresponding actions.

## Example Usage
To use this Redux slice in your application, you can dispatch the provided actions with the desired payloads:

```jsx
import { useDispatch } from 'react-redux';
import {
    setData,
    setRowData,
    setColumnDefs,
    setTableOptions
} from './path/to/getTableSlice';

// Inside a component or action creator
const dispatch = useDispatch();

// Dispatching actions with the desired payloads
dispatch(setData(tableData));
dispatch(setRowData(rowData));
dispatch(setColumnDefs(columnDefinitions));
dispatch(setTableOptions(tableOptions));

```

This will update the state with the new values and trigger any relevant Redux state updates or subscriptions.

Note: Make sure to adjust the import paths according to your project structure.