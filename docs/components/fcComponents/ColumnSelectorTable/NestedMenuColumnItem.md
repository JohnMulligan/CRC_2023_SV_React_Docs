# NestedMenuColumnItem
NestedMenuColumnItem is a React component that provides a nested menu functionality. It renders a menu item with a label and an optional right icon. When the menu item is hovered or focused, a submenu is displayed with additional menu options.

## Installation
To use NestedMenuColumnItem, you need to have React and Material-UI installed in your project. You can install them using npm or yarn:

```js
npm install react
npm install @mui/material
```
or
```
yarn add react
yarn add @mui/material
```

## Usage
To use the NestedMenuColumnItem component, import it into your file and use it in your React component:

```jsx
import NestedMenuColumnItem from 'path/to/NestedMenuColumnItem';

function App() {
  return (
    <NestedMenuColumnItem
      label="Menu Item"
      rightIcon={<ArrowRight />}
      keepOpen={false}
      onClickMenu={(event) => {
        // Handle menu item click event
      }}
    >
      <NestedMenuColumnItem label="Submenu Item 1" />
      <NestedMenuColumnItem label="Submenu Item 2" />
    </NestedMenuColumnItem>
  );
}
```

## Props
The NestedMenuColumnItem component accepts the following props:

- `label` (required): React.ReactNode - The label or text to display for the menu item.
- `rightIcon`: React.ReactNode - An optional icon to display on the right side of the menu item.
- `keepOpen`: boolean - If true, the submenu will stay open even when a submenu option is clicked.
- `children`: React.ReactNode - An optional nested menu items to display as submenus.
- `customTheme`: any - An optional custom theme object for styling the menu item.
- `className`: string - An optional class name for the menu item.
- `tabIndex`: number - An optional tab index for the menu item.
- `rightAnchored`: boolean - If true, the submenu will be anchored to the right side of the menu item.
- `menu`: React.ReactElement[] - An array of React elements that represents the submenu options.
- `onClickMenu`: (event: MouseEvent<HTMLLIElement> | MouseEvent<HTMLDivElement>) => void - Event handler for the menu item click event.

## Example
Here's an example of using the NestedMenuColumnItem component:
```jsx
import NestedMenuColumnItem from 'path/to/NestedMenuColumnItem';

function Dropdown() {
  return (
    <NestedMenuColumnItem
      label="Menu Item"
      rightIcon={<ArrowRight />}
      keepOpen={false}
      onClickMenu={(event) => {
        console.log('Menu item clicked', event);
      }}
    >
      <NestedMenuColumnItem label="Submenu Item 1" />
      <NestedMenuColumnItem label="Submenu Item 2" />
    </NestedMenuColumnItem>
  );
}

export const DropdownNestedMenuColumnItem = styled(NestedMenuColumnItem)`
  display: flex;
  justify-content: space-between !important;

  & > svg {
    margin-left: 32px;
  }
`;
```

This example renders a menu item with the label "Menu Item" and a right arrow icon. When the menu item is clicked, the `onClickMenu` callback logs the event object. Additionally, the component has two nested menu items as submenus, "Submenu Item 1" and "Submenu Item 2".