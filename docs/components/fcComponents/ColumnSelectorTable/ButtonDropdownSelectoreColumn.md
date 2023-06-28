# ButtonDropdownSelectoreColumn
This component defines a React component called ButtonDropdownSelectoreColumn. 
It is responsible for rendering a button with a dropdown menu that allows users to configure column visibility.

## Usage
To use this component, import it into your React application and include it in your JSX code.

```jsx
import ButtonDropdownSelectoreColumn from './ButtonDropdownSelectoreColumn';

// Inside your JSX component
<ButtonDropdownSelectoreColumn />
```
## Dependencies
This component requires the following dependencies:

- `@mui/icons-material`: Provides icons for the dropdown menu.
- `@mui/material`: Provides the `Button` component used for the dropdown trigger.
- `react`: The React library for building user interfaces.
- `react-redux`: Allows the component to interact with the Redux store.
- `@/redux/store`: Provides the Redux store and types.
- `@/redux/getColumnSlice`: Contains Redux actions and reducers related to column visibility.
- `@/share/InterfaceTypesTable`: Defines types for table cell structures.

## Props
This component does not accept any props.

## Functionalities
handleColumnVisibilityChange
This function handles the column visibility change when a user selects or deselects a column in the dropdown menu. It is triggered by a click event on a menu item and dispatches the `setVisibleColumn` action from Redux with the updated visible columns.

## renderMenuItems
This function recursively renders the menu items for the dropdown menu. It takes an array of nodes and maps over them to create the menu items. Each item can be either a regular column or a nested menu item. The function determines the item type based on the presence of children. Regular columns can be selected or deselected, while nested menu items provide a submenu.

## Return
The component returns a `DropdownColumn` component, which includes a button trigger and a dropdown menu. The button is styled with Material-UI and displays the text "configure columns". The dropdown menu is rendered using the renderMenuItems function and displays the columns and nested menu items based on the menuValueCells data.

## Example

```jsx 
import ButtonDropdownSelectoreColumn from "./ButtonDropdownSelectoreColumn";

export const ColumnSelector = () => {
  return <ButtonDropdownSelectoreColumn />;
};

```

In this example, the `ButtonDropdownSelectoreColumn` component is included in the `ColumnSelector` component, allowing users to configure column visibility using the dropdown menu.