# NetworkDiagramSlaveVoyages Component Documentation

The `NetworkDiagramSlaveVoyages` component is a React component designed to display a network diagram related to past networks, such as enslaved individuals and their connections. It integrates with various data sources, Redux for state management, and a network diagram visualization component. This documentation provides an overview of the component, its features, usage, and dependencies.

## Features
- Displays a network diagram related to past networks.
- Utilizes data fetched from an API.
- Handles double-click events on nodes to fetch additional network data.
- Integrates with Redux for managing network data and state.
- Shows a loading logo while data is being fetched.


## Usage
To use the NetworkDiagramSlaveVoyages component in your React application, follow these steps:

1) Import the Component

Import the `NetworkDiagramSlaveVoyages` component into your application:
```jsx
import { NetworkDiagramSlaveVoyages } from './NetworkDiagramSlaveVoyages';

```

2) Include the Component in Your JSX

You can include the `NetworkDiagramSlaveVoyages` component in your JSX to display the network diagram. Ensure that you have the necessary Redux store and actions set up to manage the network data and state.

```jsx
// Inside your JSX
<NetworkDiagramSlaveVoyages />
```

3) Redux Integration

The component relies on Redux for managing the network data and state. Ensure that you have the Redux store configured with the following slices and actions:

- `getPastNetworksGraphData` slice with fields like `data`, `networkID`, and `networkKEY`.
- Actions such as `setPastNetworksData`, `setNetWorksID`, `setIsModalCard`, and `setNodeClass` should be available to update the network data and state.

Example Redux usage:
```jsx
// Import necessary Redux dependencies
import { useDispatch, useSelector } from 'react-redux';
import { setPastNetworksData, setNetWorksID, setIsModalCard, setNodeClass } from '@/redux/getPastNetworksGraphDataSlice';
import { RootState } from '@/redux/store';

// Inside a component
const dispatch = useDispatch();
const { data, networkID, networkKEY } = useSelector((state: RootState) => state.getPastNetworksGraphData);

// Set network data
const updateNetworkData = (newData) => {
  dispatch(setPastNetworksData(newData));
};

// Other actions like setNetWorksID, setIsModalCard, and setNodeClass can be used similarly.
```

## Data Fetching
The component uses the `fetchPastNetworksGraphApi` function to fetch network data. This function can be customized to fetch data from your specific API.

## Loading Animation
While data is being fetched, a loading animation with the `LOADINGLOGO` image is displayed. You can customize the loading animation as needed.

## Dependencies
The `NetworkDiagramSlaveVoyages` component relies on the following dependencies:

- React
- Redux
- A network diagram visualization component `(NetworkDiagram)`
- An API for fetching network data
- An image file `(LOADINGLOGO)` for the loading animation

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.