# ModalNetworksGraph Component 
The `ModalNetworksGraph` component is a React component designed to display a modal window containing a network diagram of people and their connections. It integrates with Material-UI for styling and Redux for state management. This documentation provides an overview of the component, its features, usage, and dependencies.

## Features
- Displays a modal window with a network diagram of people and their connections.
- Utilizes Material-UI for styling the modal and its content.
- Manages the modal's visibility using Redux state.

## Usage
To use the `ModalNetworksGraph` component in your React application, follow these steps:

1) Import the Component

Import the `ModalNetworksGraph` component into your application:
```jsx
import ModalNetworksGraph from './ModalNetworksGraph';
```
2) Include the Component in Your JSX

You can include the `ModalNetworksGraph` component in your JSX to display the network diagram modal. Ensure that you have the necessary Redux store and actions set up to control the modal's visibility.

```jsx
// Inside your JSX
<ModalNetworksGraph />
```

3) Redux Integration

The component relies on Redux for managing the modal's state. Ensure that you have the Redux store configured with the following slice and action:

- `getPastNetworksGraphData` slice with the `openModal` field.
- The action `setsetOpenModalNetworks` should be available to update the modal's visibility.

Example Redux usage:
```jsx
// Import necessary Redux dependencies
import { useDispatch, useSelector } from 'react-redux';
import { setsetOpenModalNetworks } from '@/redux/getPastNetworksGraphDataSlice';
import { RootState } from '@/redux/store';

// Inside a component
const dispatch = useDispatch();
const { openModal } = useSelector((state: RootState) => state.getPastNetworksGraphData);

// Open the modal
const openModalNetworks = () => {
  dispatch(setsetOpenModalNetworks(true));
};

// Close the modal
const closeModalNetworks = () => {
  dispatch(setsetOpenModalNetworks(false));
};

```

## Styling
The component utilizes Material-UI for styling. Custom styles are defined in `styleModalNetworks`. You can modify this style object to match your application's design requirements.

## Dependencies
The `ModalNetworksGraph` component relies on the following dependencies:

- React
- Material-UI (@mui/material)
- Redux
- An image file (NETWORKICON) for the network icon


Ensure that you have these dependencies installed and configured in your project.

Please note that you should customize this example to fit your specific project structure and requirements. Ensure that you have the required dependencies and Redux store properly configured for the `ModalNetworksGraph` component to work correctly.