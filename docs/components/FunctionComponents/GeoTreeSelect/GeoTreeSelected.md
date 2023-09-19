# GeoTreeSelected Component Documentation

The `GeoTreeSelected` component is a React-based user interface element used for selecting and filtering geographic tree data within an application. This component interacts with various data sources, Redux state, and user interactions to provide a dynamic and responsive user experience.

## Prerequisites
Before using the `GeoTreeSelected` component, ensure that you have the following prerequisites in place:

- React: This component is built using React, so make sure your project includes React.
- Redux: The component relies on Redux for state management, so ensure that Redux is set up and configured in your project.
- Ant Design: The component uses Ant Design's `TreeSelect` for user interaction, so make sure Ant Design is installed and configured in your project.
- Various utility functions, constants, and API functions: The component depends on several utility functions, constants, and API functions imported from specific paths in your project.

## Component Overview
The `GeoTreeSelected` component is designed to provide the user with the ability to filter geographic tree data based on user selections. It includes the following key features and functionality:

- Selection of geographic tree values: Users can select one or more geographic tree values from a dropdown menu.
- Dynamic data loading: The component fetches and loads geographic tree data dynamically based on user interactions and changes in application state.
- Local storage: Selected values and filter criteria are stored in the browser's local storage for persistence across sessions.
- Integration with other application components: The component interacts with other application components and Redux stores to coordinate filtering and data display.

## Usage
To use the `GeoTreeSelected` component within your application, follow these steps:

1) Import the component:
```jsx
import GeoTreeSelected from './GeoTreeSelected';
```

2) Include the component in your JSX/HTML markup where you want to display it:
```jsx
<GeoTreeSelected />
```
3) Ensure that you have set up the required Redux store, Ant Design components, and utility functions in your project for the component to work effectively.

## Functionality
## Geographic Tree Selection
The primary functionality of the `GeoTreeSelected` component is to allow users to select geographic tree values. Here's how it works:

- Users can select one or more geographic tree values from a dropdown menu presented as a `TreeSelect` component from Ant Design.
- Selected values are stored in the `selectedValue` state variable using React's useState.

## Dynamic Data Loading
The component fetches geographic tree data dynamically based on various criteria:

- The `varName` and `geoTreeValue` values are used to construct a FormData object for API requests.
- Data is fetched based on the user's interactions, such as changes in selected values, auto-complete options, and range slider values.
- Data is fetched using API functions such as `fetcVoyagesGeoTreeSelectLists`, `fetchEnslavedGeoTreeSelect`, and `fetchEnslaversGeoTreeSelect`.

## Local Storage
Selected values and filter criteria are stored in the browser's local storage for persistence across sessions. This allows users to retain their selections even after closing and reopening the application.


## Interaction with Redux
The component interacts with the Redux store to manage state related to geographic tree data and filtering:

- It uses Redux selectors to retrieve values such as `isChangeGeoTree`, `geoTreeList`, and `geoTreeValue`.
- It dispatches actions to update state variables such as geoTreeValueList, isChangeGeoTree, and geoTreeValueSelect.

## Dependencies
Ensure that you have the following dependencies installed and configured in your project:

- React: Used as the base framework for building the component.
- Redux: Utilized for state management.
- Ant Design: Utilized for the `TreeSelect` component and user interface elements.
- Various utility functions, constants, and API functions imported from specific paths in your project.

Ensure that you have these dependencies installed and configured in your project.

Please make sure to integrate this component into your project following the steps outlined above and adapt it to your specific use case as needed.
