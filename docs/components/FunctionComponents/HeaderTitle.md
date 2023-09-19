# HeaderTitle Component Readme Documentation

## Overview
The `HeaderTitle` component is a React component designed to display a title and an optional subtitle with a link. This component is intended for use in a header or navigation bar where you want to provide a clickable title. This readme documentation will guide you through the usage and functionality of this component.

## Installation
1) If you haven't already, make sure you have React and React Router installed in your project:
```jsx
npm install react react-dom react-router-dom
```

2) Import the `HeaderTitle` component at the beginning of your component file:

```jsx
import { Link } from 'react-router-dom';

```

3) Define the `HeaderTitle` component:

```jsx
interface HeaderTitleProps {
  textHeader: string;
  HeaderTitle: string;
  pathLink: string;
  onClickReset: () => void;
}

export const HeaderTitle = (props: HeaderTitleProps) => {
  // Component implementation here
};
```

## Usage
To use the `HeaderTitle` component, follow these steps:

1) Import the `HeaderTitle` component into your React application:
```jsx
import { HeaderTitle } from './HeaderTitle'; // Update the path to the component
```

2) Use the `HeaderTitle` component within your JSX by including it in your component hierarchy:

```jsx
function MyComponent() {
  // ...
  return (
    <div>
      {/* Your other components */}
      <HeaderTitle
        textHeader="Subtitle Text"
        HeaderTitle="Main Title"
        pathLink="/link-path"
        onClickReset={() => {
          // Handle reset logic here
        }}
      />
    </div>
  );
}
```

3) Customize the `HeaderTitle` component by passing the following props:

    - `textHeader (string):` Optional subtitle text to display below the main title.
    - `HeaderTitle (string):` The main title to be displayed.
    - `pathLink (string):` The path to navigate to when the title is clicked. You can use React Router's Link component for navigation.
    - `onClickReset (function):` A callback function to execute when the title is clicked. You can use this to perform any reset or action when the title is clicked.

## Example
Here's an example of how to use the `HeaderTitle` component within a React application:
```jsx
import React from 'react';
import { HeaderTitle } from './HeaderTitle';
import { useHistory } from 'react-router-dom';

function App() {
  const history = useHistory();

  const handleReset = () => {
    // Handle reset logic here
  };

  return (
    <div className="App">
      {/* Other components */}
      <HeaderTitle
        textHeader="Subtitle Text"
        HeaderTitle="Main Title"
        pathLink="/link-path"
        onClickReset={() => {
          handleReset();
          history.push('/link-path'); // Navigate to the specified path
        }}
      />
    </div>
  );
}

export default App;
```

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.


