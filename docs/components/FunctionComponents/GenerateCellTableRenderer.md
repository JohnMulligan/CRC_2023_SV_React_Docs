# GenerateCellTableRenderer Function

The `GenerateCellTableRenderer` function is a utility function designed for use in Ag-Grid tables within a React application. It is responsible for rendering cell content based on the provided parameters and cell function `(cellFN).` The function allows for custom rendering of cell values and handles user interactions, such as opening modals or triggering actions.

## Prerequisites
Before using the `GenerateCellTableRenderer` function, ensure that you have the following dependencies and prerequisites installed:

- React: The function is designed for use within a React application.
- Ag-Grid: This function is intended for use in Ag-Grid tables and requires the Ag-Grid library.
- Redux: The function interacts with the Redux store for state management.
- Various utility functions, constants, and assets: The function relies on utility functions, constants, and assets imported from various locations in your project.


## Function Signature

```jsx
GenerateCellTableRenderer(
  params: ICellRendererParams,
  cellFN: string,
  nodeClass?: string
): React.ReactNode

```

The `GenerateCellTableRenderer` function accepts the following parameters:

- `params:` An object of type `ICellRendererParams` from Ag-Grid containing information about the cell and its value.
- `cellFN:` A string specifying the cell function, which determines how the cell should be rendered.
- `nodeClass `(optional): A string specifying the node class for certain cell functions.

## Usage
The `GenerateCellTableRenderer` function is typically used as the `cellRenderer` in an Ag-Grid column definition. It is responsible for custom rendering of cell values based on the specified `cellFN`. Below are some examples of how to use the function:

## Rendering Text Values
```jsx
import { AgGridColumn } from 'ag-grid-react';

<AgGridColumn
  headerName="Column Header"
  field="columnName"
  cellRenderer={(params) =>
    GenerateCellTableRenderer(params, 'textCellFunction')
  }
/>

```

In this example, the function is used to render text cell values based on the `textCellFunction`. When the cell is clicked, it triggers actions using Redux.

## Rendering Network Icons
```jsx
import { AgGridColumn } from 'ag-grid-react';

<AgGridColumn
  headerName="Network"
  field="networkData"
  cellRenderer={(params) =>
    GenerateCellTableRenderer(params, 'networks', 'optionalNodeClass')
  }
/>

```

In this example, the function is used to render a network icon cell based on the networks cell function. Clicking the `network` icon opens a modal and triggers actions using Redux.

## Handling Default Values

```jsx
import { AgGridColumn } from 'ag-grid-react';

<AgGridColumn
  headerName="Column Header"
  field="columnName"
  cellRenderer={(params) =>
    GenerateCellTableRenderer(params, 'defaultCellFunction')
  }
/>

```

In this example, the function is used to handle default cell values for the `defaultCellFunction`. It renders a placeholder value and does not trigger additional actions.

## Functionality
The `GenerateCellTableRenderer` function provides the following functionality based on the `cellFN:`

- Rendering text values with click actions for certain cell functions.
- Rendering network icons with modal opening and actions for the `networks` cell function.
- Handling default values for unspecified cell functions.

## Styling
The function applies custom styling to cell values and icons, ensuring they appear correctly within the Ag-Grid table.

## Customization
You can customize the behavior of the `GenerateCellTableRenderer` function by specifying different `cellFN` values and modifying the rendering logic within the function. Additionally, you can adjust styling and Redux actions as needed.

## Dependencies
Ensure that you have the following dependencies installed and configured in your project:

- React: Used as the base framework for building the function.
- Ag-Grid: Utilized for rendering tables and providing cell information.
- Redux: Utilized for state management.
- Various utility functions, constants, and assets imported from specific paths in your project.

## License
This function is subject to the license terms and conditions specified in your project. Make sure to comply with the licensing requirements of the libraries and assets used within this function.

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.