## VoyageCard Component Documentation

The `VoyageCard` component is a React component designed to display card data related to voyages, enslaved individuals, or enslavers. It integrates with Material-UI, Redux for state management, and several utility functions for data processing. This documentation provides an overview of the component, its features, usage, and dependencies.


## Features
- Displays detailed information about voyages, enslaved individuals, or enslavers.
- Allows expanding and collapsing individual card sections.
- Provides an option to expand or collapse all card sections.
- Utilizes Redux for managing card data and state.
- Integrates Material-UI for styling.

## Usage
To use the `VoyageCard` component in your React application, follow these steps:

1) Import the Component

Import the VoyageCard component into your application:
```jsx
import VoyageCard from './VoyageCard';

```
2) Include the Component in Your JSX

You can include the VoyageCard component in your JSX to display card data. Ensure that you have the necessary Redux store and actions set up to control the card data and its visibility.
```jsx
// Inside your JSX
<VoyageCard />

```

3) Redux Integration
The component relies on Redux for managing card data and state. Ensure that you have the Redux store configured with the following slices and actions:

- `getCardFlatObjectData` slice with fields like `cardData`, `cardRowID`, `cardFileName`, `cardDataArray`, and `nodeType`.
- Actions such as `setCardData`, `setCardDataArray`, and `setCardFileName` should be available to update the card data.

Example Redux usage:
```jsx
// Import necessary Redux dependencies
import { useDispatch, useSelector } from 'react-redux';
import { setCardData, setCardDataArray, setCardFileName } from '@/redux/getCardFlatObjectSlice';
import { RootState } from '@/redux/store';

// Inside a component
const dispatch = useDispatch();
const { cardData, cardRowID, cardFileName, cardDataArray, nodeType } =
  useSelector((state: RootState) => state.getCardFlatObjectData);

// Set card data
const updateCardData = (data) => {
  dispatch(setCardData(data));
};

// Other actions like setCardDataArray and setCardFileName can be used similarly.

```
## Data Processing
The `VoyageCard` component uses the `processCardData` function to process card data before rendering it. You can customize the data processing logic according to your application's needs.

## Styling
The component utilizes Material-UI for styling. Custom styles are defined in `styleCard` and `CardHeaderCustom`. You can modify these styles to match your application's design requirements.

## Dependencies
The `VoyageCard` component relies on the following dependencies:

- React
- Material-UI `(@mui/material)`
- Redux
- Several utility functions and JSON data files
- Ensure that you have these dependencies installed and configured in your project.


Please note that you should customize this example to fit your specific project structure and requirements. Ensure that you have the required dependencies and Redux store properly configured for the `VoyageCard` component to work correctly.