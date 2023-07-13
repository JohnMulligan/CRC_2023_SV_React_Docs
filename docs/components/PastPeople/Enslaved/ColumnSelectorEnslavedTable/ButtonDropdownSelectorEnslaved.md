# ButtonDropdownSelectorEnslaved Component

The `ButtonDropdownSelectorEnslaved` component is a React functional component that represents a button with a dropdown menu for configuring columns. It utilizes various dependencies, components, and Redux state.

## Dependencies
The component imports the following dependencies:

- `@mui/icons-material`: Provides icons such as `ArrowDropDown` and `ArrowRight`.
- `@mui/material`: Provides the `Button` component from Material-UI.
- `react`, `react-redux`, `redux`: Dependencies for React and Redux.
- `@/styleMUI`, `@/share/InterfaceTypesTable`, `@/share/InterfaceTypes`, @`/components/FunctionComponents/ColumnSelectorTable/DropdownColumn`: Custom dependencies specific to the project.

## Usage
To use the `ButtonDropdownSelectorEnslaved` component, follow these steps:

- Import the necessary dependencies and components:
```jsx
import { ArrowDropDown, ArrowRight } from '@mui/icons-material';
import { Button } from '@mui/material';
import { DropdownMenuColumnItem, DropdownNestedMenuColumnItem } from '@/styleMUI';
import { MouseEvent, useEffect, useState } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { AppDispatch, RootState } from '@/redux/store';
import { setVisibleColumn } from '@/redux/getColumnSlice';
import { ColumnSelectorTree, TableCellStructureInitialStateProp } from '@/share/InterfaceTypesTable';
import ENSLAVED_TABLE from '@/utils/flatfiles/enslaved_table_cell_structure.json';
import AFRICANORIGINS_TABLE from '@/utils/flatfiles/african_origins_table_cell_structure.json';
import TEXAS_TABLE from '@/utils/flatfiles/texas_table_cell_structure.json';
import { TYPESOFDATASETPEOPLE } from '@/share/InterfaceTypes';
import { DropdownColumn } from '@/components/FunctionComponents/ColumnSelectorTable/DropdownColumn';
```

- Define the interface for the `MenuDropdown` component props:
```jsx
interface MenuDropdownProps {
  open: boolean;
}
```
The `MenuDropdownProps` interface specifies that the `MenuDropdown` component expects a prop called `open` of type `boolean` to represent the open/closed state of the dropdown menu.

- Implement the `ButtonDropdownSelectorEnslaved` component:

```jsx
const ButtonDropdownSelectorEnslaved = () => {
  // Redux state and dispatch
  const dispatch: AppDispatch = useDispatch();
  const { visibleColumnCells } = useSelector(
    (state: RootState) => state.getColumns as TableCellStructureInitialStateProp
  );
  const { styleName } = useSelector(
    (state: RootState) => state.getDataSetCollection
  );
  const { styleNamePeople } = useSelector(
    (state: RootState) => state.getPeopleDataSetCollection
  );

  // Local state
  const [menuValueCells, setMenuValueCells] = useState<ColumnSelectorTree[]>([]);

  // Event handler for column visibility change
  const handleColumnVisibilityChange = (
    event: MouseEvent<HTMLLIElement> | MouseEvent<HTMLDivElement>
  ) => {
    // ... implementation ...
  };

  // Load menu value cell structure based on styleNamePeople
  useEffect(() => {
    // ... implementation ...
  }, [menuValueCells]);

  // Render menu items recursively
  function renderMenuItems(nodes: any[]) {
    // ... implementation ...
  }

  // Render the component
  return (
    <DropdownColumn
      trigger={
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <Button
            sx={{
              // ... button styles ...
            }}
            className="configureColumnsButton"
            endIcon={<ArrowDropDown />}
          >
            configure columns
          </Button>
        </span>
      }
      menu={renderMenuItems(menuValueCells)}
    />
  );
};
export default ButtonDropdownSelectorEnslaved;
```

The `ButtonDropdownSelectorEnslaved` component is a functional component that handles the configuration of columns in a dropdown menu. It uses various Redux states, dispatches, and local states to manage the visibility of columns.

The component renders a `Button` from Material-UI with the label "configure columns" and an arrow icon `(ArrowDropDown)` as the end icon. Clicking the button reveals a dropdown menu with options for configuring the columns.

The component uses the `DropdownColumn` component to handle the dropdown functionality. The `renderMenuItems` function recursively renders the menu items based on the `menuValueCells` state.

By customizing the styles and behavior of the `ButtonDropdownSelectorEnslaved` component, you can create a configurable column menu with specific options for your application or website.