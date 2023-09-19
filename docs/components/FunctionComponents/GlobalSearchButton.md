# GlobalSearchButton Component Readme Documentation


## Overview
The `GlobalSearchButton` component is a React component designed to work with Redux for managing global search functionality. It provides a user interface for displaying and exiting global search mode. This readme documentation will guide you through the usage and functionality of this component.

## Installation
This component assumes you have a Redux store set up in your React application. Before using the `GlobalSearchButton`, ensure you have the required dependencies and configurations in place.

1) Install the necessary dependencies if you haven't already:
```jsx 
npm install react react-redux @mui/icons-material
```

2) Import the required dependencies at the beginning of your component file:
```jsx
import { setInputSearchValue } from '@/redux/getCommonGlobalSearchResultSlice';
import { AppDispatch, RootState } from '@/redux/store';
import { useEffect } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import ExitToAppIcon from '@mui/icons-material/ExitToApp';
import '@/style/homepage.scss';

```

## Usage
To use the `GlobalSearchButton` component, follow these steps:
1) Add the `GlobalSearchButton` component to your React application.
```jsx
import GlobalSearchButton from './GlobalSearchButton'; // Update the path to the component
```
2) Use the `GlobalSearchButton` component within your JSX by including it in your component hierarchy.
```jsx
function MyComponent() {
  // ...
  return (
    <div>
      {/* Your other components */}
      <GlobalSearchButton />
    </div>
  );
}
```

3) The `GlobalSearchButton` component will now display a button and text indicating the current global search value.


## Functionality
The `GlobalSearchButton` component provides the following functionality:

## 1. Display Current Global Search Value
- The component displays the current global search value obtained from the Redux store.
## 2. Exit Global Search
- Clicking the "Exit global search" button triggers the `handleExitGlobalSearch` function.
- This function clears the global search value in the Redux store and updates the filterObject in `localStorage` by removing the "global_search" key.
## 3. Initialization
- The component checks for a previously stored global search value in `localStorage` during its initialization.
- If a value is found, it sets it in the Redux store using setInputSearchValue.


## Customization
You can customize the appearance and behavior of the `GlobalSearchButton` component by modifying the styles and logic within the component file as needed.

## Example
Here's a basic example of how to use the `GlobalSearchButton` component within a React application:

```jsx
import React from 'react';
import { Provider } from 'react-redux';
import store from './redux/store'; // Import your Redux store configuration
import GlobalSearchButton from './GlobalSearchButton';

function App() {
  return (
    <Provider store={store}>
      <div className="App">
        {/* Other components */}
        <GlobalSearchButton />
      </div>
    </Provider>
  );
}

export default App;

```

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.
