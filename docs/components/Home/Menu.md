# MenuButtonHomePage Component
The `MenuButtonHomePage` component is a React functional component that represents a menu button for a home page. It utilizes the `BurgerMenu` and `MenuDropdown` components.

## Usage
To use the `MenuButtonHomePage` component, follow these steps:

- Import the necessary components:
```jsx
import React, { useState, useRef, useEffect } from 'react';
import { BurgerMenu } from './BurgerMenu';
import { MenuDropdown } from './MenuDropdown';
```

- Implement the `MenuButtonHomePage` component:
```jsx
const MenuButtonHomePage: React.FC = () => {
  const [open, setOpen] = useState(false);
  const node = useRef<HTMLDivElement>(null);

  useEffect(() => {
    const listener = (event: MouseEvent) => {
      if (!node.current || node.current.contains(event.target as Node)) {
        return;
      }
      setOpen(false);
    };
    document.addEventListener('mousedown', listener);

    return () => {
      document.removeEventListener('mousedown', listener);
    };
  }, []);

  return (
    <div>
      <div ref={node}>
        <BurgerMenu open={open} setOpen={setOpen} />
        <MenuDropdown open={open} />
      </div>
    </div>
  );
};
export default MenuButtonHomePage;

```
The `MenuButtonHomePage` component is a functional component that renders the `BurgerMenu` and `MenuDropdown` components. It handles the state of the menu button and controls the opening and closing of the dropdown menu.

The component uses the `useState` hook to manage the `open` state, which determines whether the dropdown menu is currently open or closed. The `setOpen` function is used to update the `open` state.

The `node` variable is created using the `useRef` hook and is used to refer to the outermost div element enclosing the menu button and dropdown menu. This allows the component to detect clicks outside of this element to close the dropdown menu.

The `useEffect` hook is used to add a click event listener to the `document` object. When a click event occurs outside of the `node.current` element (the outermost `div`), the `open` state is set to `false` to close the dropdown menu. The event listener is removed when the component is unmounted to avoid memory leaks.

Finally, the component renders the `BurgerMenu` and `MenuDropdown` components inside the `div` with the `ref={node}` attribute. The `open` state is passed as a prop to both components, allowing them to update their appearance based on the state.

## Example Usage
Here's an example of how you can use the `MenuButtonHomePage` component in a parent component:
```jsx
import React from 'react';
import MenuButtonHomePage from './MenuButtonHomePage';

const HomePage: React.FC = () => {
  return (
    <div>
      <h1>Home Page</h1>
      <MenuButtonHomePage />
      {/* Add other components or content */}
    </div>
  );
};

export default HomePage;
```

In this example, the `MenuButtonHomePage` component is used within the `HomePage` parent component. The `MenuButtonHomePage` component is rendered as part of the home page content.

By incorporating the `MenuButtonHomePage` component, you can create a menu button with a dropdown menu on your home page. The menu button's appearance and the content of the dropdown menu can be customized using the `BurgerMenu` and `MenuDropdown` components, respectively.

