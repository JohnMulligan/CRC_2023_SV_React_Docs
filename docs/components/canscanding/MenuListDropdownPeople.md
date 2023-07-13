# MenuListDropdownPeople Component Documentation
The `MenuListDropdownPeople` component is a React component that provides a dropdown menu with various options and actions. It is used to display a list of menu items and handle user interactions such as selecting an item, opening a dialog, and resetting data.

## Installation
To use this component in your React application, you need to install the required dependencies. Make sure you have React, Material-UI, and Redux installed in your project. You can install them using npm or yarn.

```js
npm install react @mui/material react-redux
```
or
```js
yarn add react @mui/material react-redux
```

## Usage
You can import the MenuListDropdown component and use it in your React application as follows:

```jsx
import { MenuListDropdownPeople } from './MenuListDropdownPeople';

function CanscandingMenu() {
  return (
    <div>
      {/* Your other components */}
      <MenuListDropdownPeople />
      {/* Your other components */}
    </div>
  );
}

export default CanscandingMenu;
```

## Description
The `MenuListDropdownPeople` component is responsible for rendering a dropdown menu with options. It uses Redux to manage the state and dispatch actions.

The component consists of the following key elements:

- `Button`: Renders a button for each menu item. When clicked, it triggers the opening of the dropdown menu.
- `Dropdown`: Renders a nested dropdown menu with additional options.
- `Dialog`: Displays a dialog box when an option is selected from the dropdown menu. It contains a title, content, and actions.

## Props
The MenuListDropdown component does not accept any props.

## Example
Here's an example of how you can use the MenuListDropdown component in your application:
```jsx
import { MenuListDropdownPeople } from './MenuListDropdownPeople';

function CanscandingMenu() {
  return (
    <div>
      {/* Your other components */}
      <MenuListDropdownPeople />
      {/* Your other components */}
    </div>
  );
}

export default CanscandingMenu;
```

Please note that you may need to adjust the import statements and file paths based on your project's file structure.

That's it! You can now use the `MenuListDropdownPeople` component in your React application to display a dropdown menu with various options and handle the selection of those options.