# NestedMenuItem
This is a React component called NestedMenuItem that represents a nested menu item with submenus. It utilizes the Material-UI library and provides various customization options.

## Installation
To use this component in your React application, you need to install the required dependencies. Make sure you have React and Material-UI installed in your project. You can install them using npm or yarn.

```js
npm install react @mui/material
```
or

```js
yarn add react @mui/material
```

## Usage
You can import the NestedMenuItem component and use it in your React application as follows:
```jsx
import NestedMenuItem from './NestedMenuItem';

function App() {
  return (
    <div>
      {/* Your other components */}
      <NestedMenuItem />
      {/* Your other components */}
    </div>
  );
}

export default App;
```

## Description
The `NestedMenuItem` component is responsible for rendering a nested menu item with submenus. It accepts various props to customize its behavior and appearance.

The component consists of the following key elements:

- `MenuItem`: Represents the main menu item. It displays the label and an optional right icon.
- `Menu`: Renders the submenu when the main menu item is clicked. It contains the nested menu items as children.

## Props
The `NestedMenuItem` component accepts the following props:

- `parentMenuOpen` (boolean, optional): Indicates whether the parent menu is open or not.
- `label` (string, optional): The label text displayed for the menu item.
- `varName` (string | undefined, optional): The variable name associated with the menu item.
- `type` (string | undefined, optional): The type of the menu item.
- `rightIcon` (JSX.Element, optional): The right icon element displayed next to the label.
- `keepOpen` (boolean, optional): Determines if the submenu should remain open after selection.
- `children` (React.ReactNode): The nested menu items to be displayed as children.
- `childrenFilter` (ChildrenFilter, optional): Additional filtering options for the children.
- `customTheme` (any, optional): Custom styling/theme for the submenu.
- `className` (string, optional): Custom CSS class name for the component.
- `tabIndex` (number, optional): The tab index of the menu item.
- `ContainerProps` (React.HTMLAttributes<HTMLDivElement> & { ref?: RefObject<HTMLDivElement> }, optional): Additional props for the container element.
- `rightAnchored` (boolean, optional): Determines if the submenu should be anchored to the right.
- `disabled` (boolean, optional): Indicates whether the menu item is disabled or not.
- `onClickMenu` ((event: MouseEvent<HTMLLIElement> | MouseEvent<HTMLDivElement>) => void): Event handler for the menu item click event.

## Example
Here's an example of how you can use the NestedMenuItem component in your application:

```jsx
import NestedMenuItem from './NestedMenuItem';

function App() {
  return (
    <div>
      {/* Your other components */}
      <NestedMenuItem
        label="Menu Item 1"
        onClickMenu={(event) => {
          console.log('Menu Item 1 clicked');
        }}
      >
        <NestedMenuItem
          label="Submenu Item 1"
          onClickMenu={(event) => {
            console.log('Submenu Item 1 clicked');
          }}
        />
        <NestedMenuItem
          label="Submenu Item 2"
          onClickMenu={(event) => {
            console.log('Submenu Item 2 clicked');
          }}
        />
      </NestedMenuItem>
      {/* Your other components */}
    </div>
  );
}

export default App;
```

Please note that you may need to adjust the import statements and file paths based on your project's file structure.

That's it! You can now use the `NestedMenuItem` component in your React application to create nested menu items with submenus.