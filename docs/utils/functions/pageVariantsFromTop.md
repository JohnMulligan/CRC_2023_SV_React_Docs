# Documentation for pageVariantsFromTop and pageVariantsFromBottom Objects

The `pageVariantsFromTop` and `pageVariantsFromBottom` objects are used to define variants for animating page transitions in a web application. These objects are typically used in combination with animation libraries or frameworks to create smooth and visually appealing transitions when navigating between pages or components.

### `pageVariantsFromTop` Object

## Usage
```jsx
export const pageVariantsFromTop = {
    initial: { opacity: 0, y: -1000 },
    animate: { opacity: 1, y: 0 },
};

```

## Description
- `initial:` Represents the initial state of the page when it is not visible. In this case, it specifies that the page should have 0 opacity (completely transparent) and be positioned 1000 pixels above its final position on the Y-axis.

- `animate:` Represents the state of the page when it is actively animating into view. In this case, it specifies that the page should have full opacity (completely visible) and be positioned at its final position on the Y-axis.

### `pageVariantsFromBottom` Object

## Usage
```jsx
export const pageVariantsFromBottom = {
    initial: { opacity: -1000, y: 0 },
    animate: { opacity: 0, y: 1 },
};
```

## Description
- `initial:` Represents the initial state of the page when it is not visible. In this case, it specifies that the page should have -1000 opacity (completely transparent, but with a numerical value that indicates it's not visible) and be positioned at its current Y-axis position (no change in position).

- `animate:` Represents the state of the page when it is actively animating out of view. In this case, it specifies that the page should have 0 opacity (completely transparent) and be positioned 1 unit below its current Y-axis position.

## Example
```jsx
// Example usage of pageVariantsFromTop and pageVariantsFromBottom
import { motion } from "framer-motion";

// Animating a component using pageVariantsFromTop
<motion.div
    initial="initial"
    animate="animate"
    variants={pageVariantsFromTop}
>
    {/* Component content */}
</motion.div>

// Animating a different component using pageVariantsFromBottom
<motion.div
    initial="initial"
    animate="animate"
    variants={pageVariantsFromBottom}
>
    {/* Component content */}
</motion.div>
```
In this example, the `pageVariantsFromTop` and `pageVariantsFromBottom` objects are used with the `motion` component from the Framer Motion library to animate the entrance and exit of different components. These objects define the animation variants for the components, specifying how they should transition from their initial state to their animated state. The `initial` and `animate` properties in the motion component determine which animation variant to use.