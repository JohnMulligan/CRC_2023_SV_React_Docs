# LanguagesDropdown Component Documentation

The `LanguagesDropdown` component is a React component that provides a dropdown menu for selecting languages. It interacts with Redux to manage language selection and rendering. This documentation will guide you through the usage and functionality of this component.

## Installation
This component assumes you have the necessary dependencies installed for React, Material-UI, and Redux. Make sure you have these dependencies set up in your project before using the `LanguagesDropdown` component.

```jsx
npm install react @mui/material react-redux
```

## Usage
To use the `LanguagesDropdown` component, follow these steps:

1) Import the `LanguagesDropdown` component into your React application.

```jsx
import LanguagesDropdown from './LanguagesDropdown'; // Update the path to the component
```

2) Include the `LanguagesDropdown` component within your JSX by adding it to your component hierarchy.
```jsx
function MyComponent() {
  // ...
  return (
    <div>
      {/* Your other components */}
      <LanguagesDropdown />
    </div>
  );
}
```

## Functionality
The `LanguagesDropdown` component provides the following functionality:

## 1. Language Selection
- The component displays the currently selected language in a button.
- Clicking the button opens a dropdown menu that lists available languages.
- Users can select a language from the dropdown menu.
## 2. Redux Integration
- The component uses Redux to manage the selected language.
- It retrieves the selected language from the Redux store and displays it in the button.
- When a new language is selected, it dispatches actions to update the language in the Redux store and stores the selected language in `localStorage`.
## Props
The `LanguagesDropdown` component does not accept any props. It relies on Redux for managing language-related state and actions.

## Example
Here's an example of how to use the `LanguagesDropdown` component within a React application:

```jsx
import React from 'react';
import LanguagesDropdown from './LanguagesDropdown';

function App() {
  return (
    <div className="App">
      {/* Other components */}
      <LanguagesDropdown />
    </div>
  );
}

export default App;

```


Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.
