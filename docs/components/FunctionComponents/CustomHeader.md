# CustomHeader Component 

The `CustomHeader` component is a React functional component designed to render custom column headers for data tables. It provides options for sorting data, displaying menus, and handling user interactions within the table's column header.

## Prerequisites
Before using the `CustomHeader` component, ensure that you have the following dependencies and prerequisites installed:

- React: The component is designed for use within a React application.
- Redux: This component interacts with the Redux store for state management.
- Various utility functions and assets: The component relies on utility functions, constants, and assets that are imported from various locations in your project.

## Installation
To use the CustomHeader component, you can import it directly into your React application. Ensure that you have the necessary dependencies installed in your project.

```jsx
import CustomHeader from './CustomHeader'; // Adjust the import path as needed

```

## Usage
The `CustomHeader` component is typically used within an ag-Grid table column definition to customize the header for a specific column. Here's an example of how to use it:

```jsx
import React from 'react';
import { AgGridColumn } from 'ag-grid-react'; // Import ag-Grid components
import CustomHeader from './CustomHeader'; // Adjust the import path as needed

function MyTable() {
  return (
    <div className="MyTable">
      <AgGridReact /* Other AgGridReact props */>
        <AgGridColumn
          field="columnName"
          headerComponentFramework={CustomHeader}
          headerComponentParams={{
            displayName: 'Custom Column',
            enableSorting: true,
            enableMenu: true,
            menuIcon: 'fa-bars', // Font Awesome icon class for the menu icon
          }}
        />
        {/* Other columns */}
      </AgGridReact>
    </div>
  );
}

export default MyTable;

```

In the example above, the `CustomHeader` component is assigned as the `headerComponentFramework` for an `AgGridColumn`, allowing customization of the column header.

## Component Features
## Props
The `CustomHeader` component accepts the following props:

- `showColumnMenu:` A function that displays the column menu when called.
- `column:` An object containing information about the column, such as its `colId`, `sort` status, `colDef`, and more.
- `setSort:` A function to set the sorting order of the column.
- `enableMenu:` A boolean indicating whether to enable the column menu.
- `menuIcon:` A string representing a Font Awesome icon class for the menu icon.
- `enableSorting:` A boolean indicating whether to enable column sorting.
- `displayName:` A string representing the display name of the column.


## Redux State
The `CustomHeader` component interacts with the Redux store to retrieve information about the current path name, which is used to determine the data to fetch when sorting the table.

## Functionality
The `CustomHeader` component provides the following functionality:

- Customization of column headers.
- Sorting of columns in ascending or descending order.
- Display of column menus (if enabled).
- Fetching data based on the selected sorting order and column.


## Styling
The component relies on CSS for styling. Ensure that the required CSS files are imported into your project to maintain the expected styling.

## Customization
You can customize the `CustomHeader` component's appearance and behavior by modifying the component's JSX, CSS, and by passing different props when using it in your application. Adjust the styling and icon classes to match your project's design guidelines.

## Dependencies
Ensure that you have the following dependencies installed and configured in your project:

- React: Used as the base framework for building the component.
- Redux: Utilized for state management.
- Various utility functions and assets imported from specific paths in your project.

## License
This component is subject to the license terms and conditions specified in your project. Make sure to comply with the licensing requirements of the libraries and assets used within this component.

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.