# StyleBurger
`StyledBurger` using the `styled-components `library. The `StyledBurger` component renders a button that represents a burger menu icon. The appearance of the burger icon can be customized based on the `open` prop passed to it.

## Usage
To use this styled component, follow these steps:

- Import the necessary dependencies:
```jsx
import styled from "styled-components";
```

- Define the interface for the `StyledBurger` component props:

```jsx
interface StyledBurgerProps {
  open: boolean;
}
```

The `StyledBurgerProps` interface specifies that the `StyledBurger` component expects a prop called `open` of type `boolean`.

- Implement the StyledBurger component:

```jsx
export const StyledBurger = styled.button<StyledBurgerProps>`
    position: absolute;
    top: 1%;
    left: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    width: 2rem;
    height: 2rem;
    background: transparent;
    border: none;
    cursor: pointer;
    padding: 0;
    z-index: 10;
  
    &:focus {
      outline: none;
    }
  
    div {
      width: 2rem;
      height: 0.25rem;
      background: ${({ open }) => (open ? "#0D0C1D" : "#000000")};
      border-radius: 10px;
      transition: all 0.3s linear;
      position: relative;
      transform-origin: 1px;
  
      :first-child {
        transform: ${({ open }) => (open ? "rotate(45deg)" : "rotate(0)")};
      }
  
      :nth-child(2) {
        opacity: ${({ open }) => (open ? "0" : "1")};
        transform: ${({ open }) => (open ? "translateX(20px)" : "translateX(0)")};
      }
  
      :nth-child(3) {
        transform: ${({ open }) => (open ? "rotate(-45deg)" : "rotate(0)")};
      }
    }
`;
```

The `StyledBurger` component is created using the `styled.button` function from `styled-components.` It is a button element with customized styling defined within the template literal. The styles include positioning, size, background, transitions, and transformations.

The `background` property of the inner `div` elements is dynamically set based on the value of the `open` prop. If `open` is true, the background color will be`#0D0C1D`, otherwise, it will be `#000000`. This allows the burger icon to change color based on its state.

The `transform` properties of the inner `div` elements are also dynamically set based on the `open` prop. When `open` is `true`, the first `div` rotates 45 degrees, the second div becomes transparent and translates to the right, and the third `div` rotates -45 degrees. When `open` is `false`, the transformations are set to their initial values.

## Example Usage
Here's an example of how you can use the `StyledBurger` component in a React component:

```jsx
import React, { useState } from 'react';
import { StyledBurger } from './StyledBurger';

const MyComponent = () => {
  const [open, setOpen] = useState(false);

  const handleBurgerClick = () => {
    setOpen(!open);
  };

  return (
    <div>
      <h1>My Component</h1>
      <StyledBurger open={open} onClick={handleBurgerClick} />
      {/* Add other components or content */}
    </div>
  );
};

export default MyComponent;

```
In this example, the `StyledBurger` component is used within the `MyComponent` parent component. The open state variable is used to control the appearance of the burger icon. When the icon is clicked, the `handleBurgerClick` function is invoked, toggling the `open` state.

The `open` prop of the `StyledBurger` component is set to the current value of the `open` state. The `onClick` prop is also passed to the component, linking it to the `handleBurgerClick` function.

By modifying the styles and behavior of the `StyledBurger` component, you can achieve different visual effects and interactions for your burger menu icon.