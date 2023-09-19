# ModalNetworksGraph Component Documentation

The `ModalNetworksGraph` component is a React component that displays a modal dialog for presenting network graph data. This documentation will guide you through the usage and functionality of this component.

## Installation
This component assumes you have the necessary dependencies installed for React, Material-UI, and Redux. Make sure you have these dependencies set up in your project before using the `ModalNetworksGraph` component.

```jsx
npm install react @mui/material react-redux
```

## Usage
To use the `ModalNetworksGraph` component, follow these steps:

1) Import the `ModalNetworksGraph` component into your React application.
```jsx
import ModalNetworksGraph from './ModalNetworksGraph'; // Update the path to the component
```

2) Include the `ModalNetworksGraph` component within your JSX by adding it to your component hierarchy.

```jsx
function MyComponent() {
  // ...
  return (
    <div>
      {/* Your other components */}
      <ModalNetworksGraph />
    </div>
  );
}

```
## Functionality
The `ModalNetworksGraph` component provides the following functionality:

## 1. Modal Dialog
- The component displays a modal dialog that is controlled by a Redux state variable `(isOpenDialog)`.
- The modal dialog is opened when `isOpenDialog` is `true` and closed when it is false.

## 2. Closing the Modal
- Users can close the modal dialog by clicking outside of it or using any other configured method.

## 3. Content Display
- The modal dialog displays the content provided by the `GeoTreeSelected` component.

## 4. Redux Integration
- The component uses Redux to manage the state of the modal dialog.
- It dispatches actions to open `(true)` or close `(false)` the modal dialog when needed.


## Props
The `ModalNetworksGraph` component does not accept any props. It relies on Redux for managing the state of the modal dialog and the content to be displayed.

Example
Here's an example of how to use the `ModalNetworksGraph` component within a React application:


```jsx
import React from 'react';
import ModalNetworksGraph from './ModalNetworksGraph';

function App() {
  return (
    <div className="App">
      {/* Other components */}
      <ModalNetworksGraph />
    </div>
  );
}

export default App;

```

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.

