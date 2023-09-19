# VoyagesTable React Component

## Overview
The `VoyagesTable` component is a React-based table component designed for displaying and interacting with data related to voyages. It uses the `Ag-Grid` library to provide a feature-rich and highly customizable table for displaying data. This component also interacts with various Redux state variables to manage and display data, including filtering, pagination, and column visibility.

## Usage
To use the `VoyagesTable` component, import it into your React application and place it within your component hierarchy. You can customize the component by passing different props or modifying the code.
1) Import the component:
2) Include the VoyagesTable component within your application, typically within a parent component or route.
```jsx
import VoyagesTable from './VoyagesTable';

const ScrollPage = () => {
  return (
    <div>
      <h4>Table Component</h4>
      <VoyagesTable />
    </div>
  );
};

export default App;
```
## Dependencies
The `VoyagesTable` component relies on the following external libraries and resources:

- React: The component is built using React.
- Ag-Grid: A powerful grid library for displaying tabular data.
- Material-UI: Used for pagination components (Pagination, TablePagination).
- Redux: State management library for managing application state.
- axios: Used for making HTTP requests.
- @mui/material: Material-UI components for pagination.

## Props
The `VoyagesTable` component does not accept any props. Instead, it relies on Redux for managing its state and data.

## Functionality
- <h4>Data Fetching:</h4> The component fetches data from an API using the `fetchVoyageOptionsAPI` function. It sends various parameters, such as search terms, pagination, and filters, to the API.

- <h4>Pagination:</h4> The component includes pagination controls at the bottom of the table, allowing users to navigate through multiple pages of data.

- <h4>Column Selection:</h4> Users can select which columns to display in the table using the "ColumnSelector" component.

- <h4>Column Filtering:</h4> Users can filter data within each column by typing in the filter input boxes in the column headers.

- <h4>Resizable Columns:</h4> Columns in the table are resizable.

- <h4>Sorting:</h4> Columns can be sorted in ascending or descending order by clicking on the column header.

- <h4>Custom Header:</h4> The component uses a custom header component (CustomHeader) for rendering table headers.

- <h4>Responsive Design:</h4> The table's width and height adjust dynamically based on the screen size.

- <h4>Local Storage:</h4> The component saves data and visible column settings to local storage to persist user preferences.

- <h4>Network Graph and Card Modal:</h4> The component includes additional components, "ModalNetworksGraph" and "CardModal," for displaying network graphs and card modals.

## Redux State
The `VoyagesTable` component relies on several slices of Redux state to manage its behavior and data. These include slices for managing table data, column visibility, filtering, and more. The component dispatches actions to update these slices when interacting with the table.

## Styling
The component includes some predefined styles and uses CSS modules for scoped styling. The component's main container has the CSS class "grid-container", and the table has the CSS class "ag-theme-alpine". You can customize the styles by modifying the provided CSS classes or by adding your own styles.

## Local Storage
The component saves the fetched data and the selected visible columns in the browser's local storage. This allows the component to retrieve the data from local storage when the page is refreshed or revisited, reducing unnecessary API requests.

## Additional Information
- The component uses the `@react-hook/window-size` library to track window size changes for responsive design.
- It calculates the number of rows to display per page based on the window size.
- The `updateColumnDefsAndRowData` function is used to update column definitions and row data based on user interactions.

## Limitations
- The component assumes the availability of the Redux store and the required slices for storing data and managing column visibility. Please make sure to set up the Redux store and the required slices before using this component.
- The component relies on the Ag-Grid library for rendering the table. Make sure to install and import the required Ag-Grid dependencies before using this component.
- The component assumes the availability of the MUI library for rendering the pagination component. Make sure to install and import the required MUI dependencies before using this component.

## Conclusion
The provided table component offers a flexible and customizable way to display data in a tabular format with pagination, column customization, and other.

Please note that this documentation provides an overview of the `VoyagesTable` component and its functionality. Developers integrating this component into their project should refer to the actual code for implementation details and may need to make adjustments based on specific project requirements and updates beyond the knowledge cutoff date.