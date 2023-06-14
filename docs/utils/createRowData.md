# Create Row Data

This function, createRowData, is designed to generate row data for a table based on the provided data and tableOptions. It takes an array of VoyageOptionsGropProps objects as input and returns an array of RowData objects.

## Installation
No specific installation steps are required for this function.

## Usage
To use the createRowData function, follow these steps:


1) Import the required types:
```jsx
import { ColumnObjectProps, RowData } from "@/share/InterfaceTypes";
import { VoyageOptionsGropProps } from "@/share/InterfaceTypesTable";
```
2) Call the function by passing the data and tableOptions parameters:

```jsx
const rows = createRowData(data, tableOptions);
```
   - `data` (required): An array of VoyageOptionsGropProps objects containing the data for the table.
   - `tableOptions` (required): An object of type ColumnObjectProps that defines the table options.

3) The function will process the data and generate an array of RowData objects (rows).

## Function Details
The `createRowData` function iterates over each VoyageOptionsGropProps object in the provided `data` array. It creates a new `RowData` object for each item and populates it based on the values in the `VoyageOptionsGropProps` object and the specified `tableOptions`.

For each key-value pair in the `VoyageOptionsGropProps` object:

If the value is an object (excluding `null`), the function iterates over its properties.
    - If a matching property is found in the `tableOptions` object, the value is assigned to the corresponding property in the RowData object.
    - If the value is not an object, it is directly assigned to the corresponding property in the `RowData` object.
Finally, the generated RowData object is added to the `rows` array, and the process is repeated for each `VoyageOptionsGropProps` object in the `data` array.

The function returns the `rows` array containing the generated row data for the table.

## Example
Here's an example of how to use the `createRowData` function:
```jsx
import { ColumnObjectProps, RowData } from "@/share/InterfaceTypes";
import { VoyageOptionsGropProps } from "@/share/InterfaceTypesTable";

// Define the data and tableOptions
const data: VoyageOptionsGropProps[] = [
  // VoyageOptionsGropProps objects
  // ...
];

const tableOptions: ColumnObjectProps = {
  // Define the table options
  // ...
};

// Call the function to generate row data
const rows: RowData[] = createRowData(data, tableOptions);

// Use the generated row data as needed
// ...
```