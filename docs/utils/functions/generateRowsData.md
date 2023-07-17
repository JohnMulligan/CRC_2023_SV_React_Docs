## generateRowsData Function
This function is used to generate rows of data for a table based on a given array of `VoyageOptionsGropProps`. It utilizes the `traverseData` function and the `TableCollectionsOptions` module to extract specific values from the data and organize them into an array of objects.

## Usage
To use this function, follow these steps:

1) Import the necessary modules and types:

```jsx
import { VoyageOptionsGropProps } from '@/share/InterfaceTypesTable';
import { traverseData } from './traverseData';
import { TableCollectionsOptions } from './TableCollectionsOptions';

```

2) Define the generateRowsData function:

```jsx
export const generateRowsData = (
    dataRow: VoyageOptionsGropProps[],
    file?: string,
): Record<string, any> => {
    const finalRowArr: Record<string, any>[] = [];
    const columns = TableCollectionsOptions(file);
    const varNames = columns.var_name;
    dataRow.forEach((data) => {
        const finalRowObj: Record<string, any> = {};
        varNames.forEach((varName: string) => {
            const varArray = varName.split('__');
            const output = traverseData(data, varArray);
            finalRowObj[varName] = output;
        });
        finalRowArr.push(finalRowObj);
    });
    return finalRowArr;
};
```
## Parameters
The `generateRowsData` function accepts two parameters:

- `dataRow (required)`: An array of `VoyageOptionsGropProps` representing the data to be transformed into rows for the table.
- `file (optional)`: A string representing the file name or identifier, used to determine the table column structure. This parameter is passed to the `TableCollectionsOptions` module.

## Return Value
The function returns a record of type `Record<string, any>`, representing the generated rows of data for the table. Each row is an object with keys corresponding to the table column names.

## Example Usage
Here's an example of how you can use the `generateRowsData` function:
```jsx
import { generateRowsData } from './path/to/generateRowsData';

const data = [
    // Array of VoyageOptionsGropProps representing the data
    // ...
];

const file = 'example_file'; // Optional file name or identifier

const rowsData = generateRowsData(data, file);
console.log(rowsData);

```
This will generate the rows of data based on the input data and file identifier, and log the resulting rows to the console.

Note: Make sure to adjust the import paths according to your project structure.