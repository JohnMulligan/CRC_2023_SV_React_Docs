# Table Component Documentation
The `Table` component is a React functional component that represents a table with interactive features such as pagination, column selection, filtering, and sorting. It utilizes the `ag-grid-react` library for rendering and managing the table.

## Usage
To use the `Table` component, import it into your React application and place it within your component hierarchy. You can customize the component by passing different props or modifying the code.

```jsx
import Table from './Table';

const ScrollPage = () => {
  return (
    <div>
      <h1>Table Component</h1>
      <Table />
    </div>
  );
};

export default App;
```

## Props
The Table component does not accept any props.


## Functionality
1) Data Fetching and Pagination:

- The component fetches data from an API using the `fetchVoyageOptionsPagination` function.
- The fetched data is stored in the Redux store and can be accessed via the `getTableData` slice.
- Pagination is implemented using the `Pagination` component from MUI.
- The number of rows per page can be configured using the `rowsPerPageOptions` prop of the `TablePagination` - component.

2) Column Customization:

The component supports column visibility customization using the `ColumnSelector` component.
- The selected visible columns are stored in the Redux store and can be accessed via the `getColumns` slice.
- The column visibility is updated dynamically based on user selection.
3) Table Rendering:

- The component uses the Ag-Grid library to render the table.
- The table's appearance is styled using the "ag-theme-alpine" CSS class.
- The column definitions and row data are passed to the `AgGridReact` component.
- The column definitions are generated based on the `TABLE_FLAT` constant and the visible columns stored in the Redux store.
- The row data is generated using the generateRowsData function.
- The table supports sorting, filtering, and resizing of columns.

4) Loading State:

- The component displays a loading skeleton when data is being fetched.
- The loading state is controlled by the loading state variable.

## Styling
The component includes some predefined styles and uses CSS modules for scoped styling. The component's main container has the CSS class "grid-container", and the table has the CSS class "ag-theme-alpine". You can customize the styles by modifying the provided CSS classes or by adding your own styles.

## Local Storage
The component saves the fetched data and the selected visible columns in the browser's local storage. This allows the component to retrieve the data from local storage when the page is refreshed or revisited, reducing unnecessary API requests.

## Limitations
- The component assumes the availability of the Redux store and the required slices for storing data and managing column visibility. Please make sure to set up the Redux store and the required slices before using this component.
- The component relies on the Ag-Grid library for rendering the table. Make sure to install and import the required Ag-Grid dependencies before using this component.
- The component assumes the availability of the MUI library for rendering the pagination component. Make sure to install and import the required MUI dependencies before using this component.

## Conclusion
The provided table component offers a flexible and customizable way to display data in a tabular format with pagination, column customization, and other.