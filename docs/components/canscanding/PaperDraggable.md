# PaperDraggable
The `PaperDraggable` component is a wrapper component that provides draggable behavior to a `Paper` component from the Material-UI library. It uses the `react-draggable` library to enable dragging functionality.

## Installation
To use this component in your React application, make sure you have the required dependencies installed. You need to install React, Material-UI, and `react-draggable`. You can install them using npm or yarn.

```js
npm install react @mui/material react-draggable
```
or
```js
yarn add react @mui/material react-draggable
```

## Usage
You can import the PaperDraggable component and use it in your React application as follows:
```jsx
import { PaperDraggable } from './PaperDraggable';

function App() {
  return (
    <div>
      {/* Your other components */}
     <Dialog
        BackdropProps={{ style: { backgroundColor: "transparent", width: 400 } }}
        sx={StyleDialog}
        open={isOpenDialog}
        onClose={handleCloseDialog}
        PaperComponent={PaperDraggable}
        aria-labelledby="draggable-dialog-title"
      >
        <DialogTitle
          sx={{ cursor: "move", fontWeight: 600 }}
          id="draggable-dialog-title"
        >
          {label}
        </DialogTitle>
        <DialogContent style={{ textAlign: "center" }}>
          {varName && type === TYPES.CharField && <AutocompleteBox />}
          {((varName && type === TYPES.IntegerField) ||
            (varName && type === TYPES.DecimalField)) && <RangeSlider />}
        </DialogContent>
        <DialogActions>
          <Button
            autoFocus
            onClick={handleCloseDialog}
            sx={{ color: BLACK, fontSize: 16, fontWeight: 600 }}
          >
            Cancel
          </Button>
        </DialogActions>
      </Dialog>
      {/* Your other components */}
    </div>
  );
}

export default App;
```

## Description
The `PaperDraggable` component is a functional component that wraps a Paper component and adds draggable behavior to it. It accepts the same props as the `Paper` component from Material-UI.

The `PaperDraggable` component utilizes the `Draggable` component from the `react-draggable` library to handle the dragging functionality. The `handle` prop specifies the element that acts as the handle for dragging, while the `cancel` prop defines the elements that should not trigger dragging when interacted with.

## Props
The PaperDraggable component accepts the same props as the Paper component from Material-UI. These props include:

- All HTML attributes and component properties available for a div element.
Please refer to the `Material-UI Paper component documentation` for a detailed list of props available for customization.

Please refer to the `Material-UI Paper component documentation` for a detailed list of props available for customization.


## Example
Here's an example of how you can use the PaperDraggable component in your application:

```jsx
import { PaperDraggable } from './PaperDraggable';

function App() {
  return (
    <div>
      {/* Your other components */}
      <PaperDraggable elevation={3}>
        <div style={{ padding: '16px' }}>
          Drag me!
        </div>
      </PaperDraggable>
      {/* Your other components */}
    </div>
  );
}

export default App;
```
In this example, we wrap the content inside the `PaperDraggable` component. The `elevation` prop is passed to customize the shadow effect of the `Paper` component. You can add any desired content within the `PaperDraggable` component, and it will become draggable.

Please note that you may need to adjust the import statements and file paths based on your project's file structure.

That's it! You can now use the `PaperDraggable` component in your React application to create draggable `Paper` components.