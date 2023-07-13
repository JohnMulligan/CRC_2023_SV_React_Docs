
# MenuDropdown Component
The `MenuDropdown` component is a React functional component that represents a dropdown menu. It utilizes the `StyledMenu` component from the `stylesMenu/StyledMenu` module.

## Props
The `MenuDropdown` component accepts the following prop:

- `open` (boolean): Indicates whether the dropdown menu is currently open or closed.

## Usage
To use the `MenuDropdown` component, follow these steps:

- Import the `StyledMenu` component from the `stylesMenu/StyledMenu` module:

```jsx
import { StyledMenu } from './stylesMenu/StyledMenu';
```

- Define the interface for the `MenuDropdown` component props:
```jsx
interface MenuDropdownProps {
  open: boolean;
}

```

The `MenuDropdownProps` interface specifies that the `MenuDropdown` component expects a prop called `open` of type `boolean` to represent the open/closed state of the dropdown menu.

- Implement the `MenuDropdown` component:
```jsx
export const MenuDropdown: React.FC<MenuDropdownProps> = ({ open }) => {
  return (
    <StyledMenu open={open}>
      <a href="/">TIMELAPSE</a>
      <a href="/">LESSON PLANS</a>
      <a href="/">INTRODUCTORY MAPS</a>
      <a href="/">3D VIDEOS</a>
      <a href="/">ABOUT</a>
    </StyledMenu>
  );
};
```

The `MenuDropdown` component is a functional component that receives the `open` prop. It renders the `StyledMenu` component and passes the `open` prop to it.

The `MenuDropdown` component contains `a` series of a elements representing the menu items. These can be customized by modifying the text and `href` attributes as needed.

## Example Usage
Here's an example of how you can use the `MenuDropdown` component in a parent component:
```jsx
import React, { useState } from 'react';
import MenuDropdown from './MenuDropdown';

const MyComponent: React.FC = () => {
  const [open, setOpen] = useState(false);

  return (
    <div>
      <h1>My Component</h1>
      <MenuDropdown open={open} />
      {/* Add other components or content */}
    </div>
  );
};

export default MyComponent;

```

In this example, the `MenuDropdown` component is used within the `MyComponent` parent component. The `open` state and `setOpen` state setter function are initialized using the useState hook.

The `MenuDropdown` component is rendered with the `open` prop set to the `open` state. This allows the component to control the open/closed state of the dropdown menu.

By customizing the menu items in the `MenuDropdown` component, you can create a dropdown menu with specific links or actions for your application or website.