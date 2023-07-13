# DrawerMenuPeopleBar Component
The `DrawerMenuPeopleBar` component is a reusable component that renders a list of menu items in a drawer menu. It utilizes the Material-UI library for the menu components.

## Props
The `DrawerMenuPeopleBar` component accepts the following props:

- `value (optional)`: An array of strings representing the menu items.
- `handleSelectMenuItems`: A callback function that is called when a menu item is selected. It receives the selected item as a parameter.

## Usage
To use the `DrawerMenuPeopleBar` component, follow these steps:

- Import the necessary components from the Material-UI library:
```jsx
import { ListItemText, MenuItem, MenuList } from '@mui/material';
```
- Define the `DrawerMenuPeopleBar` component:
```jsx
interface DrawerMenuPeopleBarProps {
  value?: string[];
  handleSelectMenuItems: (item: string) => void;
}

export const DrawerMenuPeopleBar = (props: DrawerMenuPeopleBarProps) => {
  const { value, handleSelectMenuItems } = props;

  return value?.map((item: string, index: number) => {
    return (
      <MenuList dense style={{ padding: 0 }} key={`${item}-${index}`}>
        <MenuItem>
          <ListItemText
            className="menu-nav-bar"
            onClick={() => handleSelectMenuItems(item)}
            primary={item}
          />
        </MenuItem>
      </MenuList>
    );
  });
};

```

- Use the `DrawerMenuPeopleBar` component in your application by passing the necessary props:
```jsx
<DrawerMenuPeopleBar
  value={menuItems}
  handleSelectMenuItems={handleSelectMenuItem}
/>
```
In the above example, `menuItems` is an array of strings representing the menu items, and `handleSelectMenuItem` is a callback function that handles the selection of a menu item.

Feel free to customize the component's styling and functionality to fit your specific use case.