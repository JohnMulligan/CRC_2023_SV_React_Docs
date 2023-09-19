## EnslavedTable Component
# EnslavedTable Component Documentation

The `EnslavedTable` component is a React component designed to display and interact with a tabular data grid, with various features such as filtering, pagination, and customization of the displayed table. Below is a detailed documentation of this component:

## Prerequisites
Before using this component, ensure that you have the following dependencies installed:

- React: ^16.8.0 or higher
- Material-UI: ^4.0.0 or higher (for styling and UI components)
- Redux: ^4.0.0 or higher (for state management)
- ag-Grid: ^25.0.0 or higher (for displaying and managing the data table)

## Installation
To use the `EnslavedTable` component in your React application, follow these steps:

1) Import the component as follows:

```jsx
import EnslavedTable from './EnslavedTable'; // Replace with the actual path to the component file
```

1) Render the component within your JSX/TSX code:
```jsx 
<EnslavedTable />
```
## Usage
- The `EnslavedTable` component provides the following functionality for displaying and managing tabular data:

## Data Retrieval and Filtering
- It fetches data based on various filter criteria, including search keywords, range sliders, auto-complete selections, and more.


## Pagination
- he component offers pagination controls to navigate through multiple pages of data.


## Customization
You can customize the appearance and behavior of the table, including column visibility and ordering, through the `ButtonDropdownSelectorEnslaved` component.

## Table Interaction
The table supports sorting, resizing columns, filtering, and tooltips for improved user interaction.

## Modal Components
It includes the ModalNetworksGraph and CardModal components for displaying additional information.

## Responsive Design
The table is designed to adapt to different screen sizes and orientations.
## Table Cell Structure
The structure of the table cells can be loaded dynamically based on the selected dataset, such as "All Enslaved," "African Origins," or "Texas." The structure is loaded from JSON files located in utils/flatfiles.

## Component Dependencies
The `EnslavedTable` component relies on several Redux states and actions to manage data, filtering, column visibility, and dataset selection. Ensure that your application has the necessary Redux setup and state slices as described in the component code.

## Customization
You can customize various aspects of the `EnslavedTable` component, including styling, column definitions, and interaction behavior, to suit your project's requirements. Refer to the component code for specific customization options.

## Note: 
Make sure to adapt the component to your project's specific requirements. This README assumes you are familiar with React, Material-UI, Redux, and ag-Grid.