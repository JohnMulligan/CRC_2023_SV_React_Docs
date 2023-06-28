# DropdownColumn
DropdownColumn is a React component that provides a dropdown functionality. It renders a trigger element and a menu that can be opened and closed.

## Installation
To use DropdownColumn, you need to have React and Material-UI installed in your project. You can install them using npm or yarn:
```js
npm install react
npm install @mui/material
```
OR

```js
yarn add react
yarn add @mui/material

```

## Usage
To use the DropdownColumn component, import it into your file and use it in your React component:

```jsx
import { DropdownColumn } from 'path/to/DropdownColumn';

function App() {
  return (
    <DropdownColumn
      trigger={<button>Click me</button>}
      menu={[
        <div>Option 1</div>,
        <div>Option 2</div>,
        <div>Option 3</div>,
      ]}
      onOpen={(event) => {
        // Handle dropdown open event
      }}
      onClick={() => {
        // Handle trigger click event
      }}
    />
  );
}
```

## Props
The DropdownColumn component accepts the following props:

- `trigger` (required): ReactElement - The element that triggers the dropdown when clicked.
- `menu`: ReactElement[] - An array of React elements that - represents the dropdown menu options.
- `keepOpen`: boolean - If true, the dropdown will stay open even when a menu option is clicked.
- `isOpen`: boolean - Controls the open state of the dropdown when used in a controlled manner.
- `onOpen`: (event: MouseEvent<Element, MouseEvent> | null) => void - Event handler for the dropdown open event.
- `onClick`: () => void - Event handler for the trigger element click event.

## Example
Here's an example of using the DropdownColumn component:

```jsx
import { DropdownColumn } from 'path/to/DropdownColumn';

function ButtonDropdownSelectoreColumn() {
   return (
    <DropdownColumn
      trigger={
        <span style={{ display: "flex", alignItems: "center" }}>
          <Button
            style={{
              fontSize: 12,
              backgroundColor: "#17a2b8",
              color: "#ffffff",
            }}
            endIcon={<ArrowDropDown />}
          >
            configure columns
          </Button>
        </span>
      }
      menu={renderMenuItems(menuValueCells)}
    />
  );
}
```
This example renders a button as the trigger element. When the button is clicked, the dropdown menu will appear, showing three options. The `onOpen` callback logs the event object when the dropdown is opened, and the `onClick` callback logs a message when the trigger button is clicked.