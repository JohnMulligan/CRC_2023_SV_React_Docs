## Card Modal Component

This is a React component named CardModal that is designed to display a modal window for showing full details of a card. This component is integrated with Material-UI (MUI) and Redux for state management.

## Features
- Shows detailed information about a card.
- Utilizes Material-UI for styling and user interface components.
- Manages the modal's visibility using Redux state.

## Usage
To use this component in your React application, follow these steps:

1) Import the Component
Import the `CardModal` component into your application:
```jsx
import CardModal from './CardModal';
```

2) Add the Component to Your JSX
You can now include the `CardModal` component in your JSX to display the modal when needed. Make sure you have the necessary Redux store and actions set up to control the modal's visibility.

```jsx
// Inside your JSX
<CardModal />

```
3) Redux Integration
This component relies on Redux for managing the modal's state. Ensure you have the Redux store set up in your application. You should also have the `getCardFlatObjectData` slice with an `isModalCard` field and the `setIsModalCard` action to control the modal's visibility.

Example Redux usage:
```jsx
// Import necessary Redux dependencies
import { useDispatch, useSelector } from 'react-redux';
import { setIsModalCard } from '@/redux/getCardFlatObjectSlice';
import { RootState } from '@/redux/store';

// Inside a component
const dispatch = useDispatch();
const { isModalCard } = useSelector((state: RootState) => state.getCardFlatObjectData);

// Open the modal
const openModal = () => {
  dispatch(setIsModalCard(true));
};

// Close the modal
const closeModal = () => {
  dispatch(setIsModalCard(false));
};

```

## Styling
The component uses Material-UI for styling, and the styles are defined in a `styleModalCard` object. You can customize the styling by modifying this object according to your application's design requirements.

## Dependencies
This component relies on the following dependencies:

- React
- Material-UI `(@mui/material)`
- Redux

Ensure that you have these dependencies installed in your project.

Please note that you should customize this example to fit your specific project structure and requirements. Ensure that you have the required dependencies and Redux store properly configured for the `Card` component to work correctly.