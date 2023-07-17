## Color Utility Functions
This code defines a set of utility functions for obtaining colors and styles based on input values. These functions can be used to customize the appearance of various elements in an application.

## Usage
To use these utility functions, follow these steps:

1) Import the necessary types:

```jsx 
import { TYPESOFDATASET, TYPESOFDATASETPEOPLE } from '@/share/InterfaceTypes';

```
2) Define the utility functions:
```jsx
export const getColorVoyagePageBackground = (item: string, currentPage: number) => {
    // Implementation...
};

export const getColorBackground = (item: string) => {
    // Implementation...
};

export const getColorBTNBackgroundEnslaved = (item: string) => {
    // Implementation...
};

export const getColorBTNBackgroundEnslavers = (item: string) => {
    // Implementation...
};

export const getTextColor = (item: string) => {
    // Implementation...
};

export const getColorNavbarBackground = (item: string) => {
    // Implementation...
};

export const getColorNavbarEnslavedBackground = (item: string) => {
    // Implementation...
};

export const getColorHoverBackground = (item: string) => {
    // Implementation...
};

export const getColorBTNHoverEnslavedBackground = (item: string) => {
    // Implementation...
};

export const getColorBTNHoverEnslaversBackground = (item: string) => {
    // Implementation...
};

export const getColorBoxShadow = (item: string) => {
    // Implementation...
};

export const getColorBoxShadowEnslaved = (item: string) => {
    // Implementation...
};

export const getColorBoxShadowEnslavers = (item: string) => {
    // Implementation...
};

export const getIdStyleName = (idStyle: string) => {
    // Implementation...
};

export const getIntroBackgroundColor = (styleName: string) => {
    // Implementation...
};

export const getBoderColor = (item: string) => {
    // Implementation...
};

```
## Functions
The following utility functions are available:

- `getColorVoyagePageBackground(item: string, currentPage: number)`: Returns the background color for a specific item in the voyage page based on the current page number.
- `getColorBackground(item: string)`: Returns the background color for a specific item.
- `getColorBTNBackgroundEnslaved(item: string)`: Returns the background color for a specific enslaved item.
- `getColorBTNBackgroundEnslavers(item: string)`: Returns the background color for a specific enslavers item.
- `getTextColor(item: string)`: Returns the text color for a specific item.
`getColorNavbarBackground(item: string)`: Returns the background color for the navbar based on a specific item.
- `getColorNavbarEnslavedBackground(item: string)`: Returns the background color for the enslaved navbar based on a specific item.
- `getColorHoverBackground(item: string)`: Returns the hover background color for a specific item.
- `getColorBTNHoverEnslavedBackground(item: string)`: Returns the hover background color for a specific enslaved item.
- `getColorBTNHoverEnslaversBackground(item: string)`: Returns the hover background color for a specific enslavers item.
- `getColorBoxShadow(item: string)`: Returns the box shadow for a specific item.
- `getColorBoxShadowEnslaved(item: string)`: Returns the box shadow for a specific enslaved item.
- `getColorBoxShadowEnslavers(item: string)`: Returns the box shadow for a specific enslavers item.
- `getIdStyleName(idStyle: string)`: Returns the ID style name for a specific style.
- `getIntroBackgroundColor(styleName: string)`: Returns the background color for the intro section based on a specific style.
- `getBoderColor(item: string)`: Returns the border color for a specific item.
## Parameters
The utility functions accept one or more parameters representing the input values used to determine the colors and styles.

## eturn Value
Each utility function returns a string representing the color or style value.

## Example Usage
Here's an example of how you can use these utility functions:
```jsx
import {
    getColorBackground,
    getColorHoverBackground,
    getColorBoxShadow,
    getTextColor
} from './path/to/colorUtils';

const item = TYPESOFDATASET.allVoyages; // Example item value

const background = getColorBackground(item);
const hoverBackground = getColorHoverBackground(item);
const boxShadow = getColorBoxShadow(item);
const textColor = getTextColor(item);

console.log(background);
console.log(hoverBackground);
console.log(boxShadow);
console.log(textColor);

```
This will retrieve the corresponding color and style values based on the input item and log them to the console.

Note: Make sure to adjust the import paths according to your project structure.