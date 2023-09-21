# hasValueGetter Function

This function is a utility function used in the context of rendering table cells in the ag-Grid library. It extracts and combines values from the provided data object based on a specified cell structure, and returns the resulting value.

## Usage
To use this function, follow these steps:

1) Import the necessary types:
```jsx
import { VoyageTableCellStructure } from "@/share/InterfaceTypesTable";
import { ICellRendererParams } from "ag-grid-community";
```

2) Define the hasValueGetter function:
```jsx
export function hasValueGetter(
    params: ICellRendererParams,
    value: VoyageTableCellStructure
) {
    // Implementation...
}

```
## Parameters
The `hasValueGetter` function accepts two parameters:

- `params`: An object of type `ICellRendererParams` containing information about the cell being rendered, such as the row data and column information.
- `value`: An object of type `VoyageTableCellStructure` representing the structure of the cell, specifying how to extract and combine values from the data.


## Return Value
The function returns the resulting value based on the provided parameters and cell structure.

## Example Usage
Here's an example of how you can use the `hasValueGetter` function within the context of ag-Grid:

```jsx
import { hasValueGetter } from './path/to/hasValueGetter';

const params = {
    // Example ICellRendererParams object
    // ...
};

const value = {
    // Example VoyageTableCellStructure object
    // ...
};

const result = hasValueGetter(params, value);
console.log(result);

```

This will execute the `hasValueGetter` function with the provided parameters and log the resulting value to the console.

Note: Make sure to adjust the import paths according to your project structure.