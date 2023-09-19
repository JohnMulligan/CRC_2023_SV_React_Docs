# FilterButton Component

The `FilterButton` component is a React functional component that renders a button with a filter icon to enable or disable filtering functionality in your application. It is typically used as part of a navigation bar or user interface to allow users to toggle filtering options. The component provides options to control the filtering state and handle user interactions.

## Prerequisites
Before using the `FilterButton` component, ensure that you have the following dependencies and prerequisites installed:

- React: The component is designed for use within a React application.
- Redux: This component interacts with the Redux store for state management.
- Material-UI: The component uses Material-UI's `FilterAltIcon` for the filter icon.
- Various utility functions and assets: The component relies on utility functions, constants, and assets imported from various locations in your project.

## Installation
To use the FilterButton component, you can import it directly into your React application. Ensure that you have the necessary dependencies installed in your project.

```jsx
import { FilterButton } from './FilterButton'; // Adjust the import path as needed

```

## Usage
The `FilterButton` component is typically used within a navigation bar or user interface where filtering functionality needs to be enabled or disabled. Here's an example of how to use it:


```jsx
import React from 'react';
import { FilterButton } from './FilterButton'; // Adjust the import path as needed

function NavigationBar() {
  const pathName = 'myPage'; // Specify the current page's path name
  const currentPage = 2; // Specify the current page number

  return (
    <div className="NavigationBar">
      {/* Render the FilterButton component */}
      <FilterButton pathName={pathName} currentPage={currentPage} />
      {/* Other navigation elements */}
    </div>
  );
}

export default NavigationBar;

```

In the example above, the `FilterButton` component is used within a `NavigationBar` component to allow users to toggle filtering options based on the current page and filtering state.


## Component Features
## Props
The `FilterButton` component accepts the following props:

- `pathName:` A string representing the current page's path name. This is used to update the Redux store with the current path name when the filter button is clicked.
- `currentPage:` An integer representing the current page number. The filter button is displayed conditionally based on this value.

## Redux State
The `FilterButton` component interacts with the Redux store to retrieve the current filtering state `(isFilter)` using the `useSelector` hook.
It also dispatches actions to update the filtering state and path name in the Redux store.

## Functionality
The `FilterButton` component provides the following functionality:

- Toggling the filtering state `(isFilter)` when clicked.
- Updating the path name in the Redux store to indicate the current page.
- Conditional rendering based on the current page number to control when the button is displayed.

## Styling
The component utilizes Material-UI's `FilterAltIcon` for the filter icon. It also applies custom styling to the icon and text for visual presentation.

## Customization
You can customize the appearance and behavior of the `FilterButton` component by passing different props, adjusting the conditional rendering logic, and modifying the styling within the component.

## Dependencies
Ensure that you have the following dependencies installed and configured in your project:

- React: Used as the base framework for building the component.
- Redux: Utilized for state management.
- Material-UI: Used for rendering the filter icon.
- Various utility functions and assets imported from specific paths in your project.

## License
This component is subject to the license terms and conditions specified in your project. Make sure to comply with the licensing requirements of the libraries and assets used within this component.

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.