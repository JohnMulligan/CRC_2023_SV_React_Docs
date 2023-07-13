# DrawerMenuBar
This code defines a React component called `DrawerMenuBar` that renders a menu bar with items based on a given set of data. The menu bar allows the user to select a dataset, and when an item is clicked, a callback function called `handleSelectDataset` is invoked with specific parameters.

## Usage
To use this component, follow these steps:

- Import the necessary dependencies from the appropriate packages:
```jsx
import {
  BaseFilter,
  DataSetCollectionProps,
} from '@/share/InterfactTypesDatasetCollection';
import { ListItemText, MenuItem, MenuList } from '@mui/material';
```

- Define the interface for the props required by the DrawerMenuBar component:

```jsx
interface DrawerMenuBarProps {
  value: DataSetCollectionProps[];
  handleSelectDataset: (
    base_filter: BaseFilter[],
    label: string,
    text_introduce: string,
    style_name: string,
    blocks: string[]
  ) => void;
}
```

The `DrawerMenuBarProps` interface specifies that the `DrawerMenuBar` component expects two props: `value` of type `DataSetCollectionProps[]`, and `handleSelectDataset` of type `(base_filter: BaseFilter[], label: string, text_introduce: string, style_name: string, blocks: string[]) => void`.

- Implement the DrawerMenuBar component:

```jsx
export const DrawerMenuBar = (props: DrawerMenuBarProps) => {
  const { value, handleSelectDataset } = props;

  return value.map((item: DataSetCollectionProps, index: number) => {
    const { base_filter, headers, style_name, blocks } = item;
    return (
      <MenuList
        dense
        style={{ padding: 0 }}
        key={`${item.headers.label}-${index}`}
      >
        <MenuItem>
          <ListItemText
            className="menu-nposition: relative;
                right: 5.5%;av-bar"
            onClick={() =>
              handleSelectDataset(
                base_filter,
                headers.label,
                headers.text_introduce,
                style_name,
                blocks
              )
            }
            primary={item.headers.label}
          />
        </MenuItem>
      </MenuList>
    );
  });
};
```

The `DrawerMenuBar` component receives the props passed to it and maps over the `value` array. For each item in the array, it extracts the necessary data and renders a `MenuList` component with a single `MenuItem` containing a `ListItemText` component. The `ListItemText` component displays the label of the item and invokes the `handleSelectDataset` function with the corresponding parameters when clicked.

## Example Usage
Here's an example of how you can use the `DrawerMenuBar` component in a parent component:

```jsx
import React from 'react';
import { DrawerMenuBar } from './DrawerMenuBar';

const MyComponent = () => {
  const datasetCollection = [
    {
      base_filter: [...],
      headers: {
        label: 'Dataset 1',
        text_introduce: 'Introduction to Dataset 1',
      },
      style_name: 'style1',
      blocks: [...],
    },
    // Add more dataset objects as needed
  ];

  const handleSelectDataset = (
    base_filter,
    label,
    text_introduce,
    style_name,
    blocks
  ) => {
    // Handle dataset selection logic here
  };

  return (
    <div>
      <h1>My Component</h1>
      <DrawerMenuBar
        value={datasetCollection}
        handleSelectDataset={handleSelectDataset}
      />
      {/* Add other components or content */}
    </div>
  );
};

export default MyComponent;
```

In this example, the `DrawerMenuBar` component is used within the `MyComponent` parent component. The `datasetCollection` array contains the dataset objects to be rendered in the menu bar. The `handleSelectDataset` function is passed as a prop to the `DrawerMenuBar` component to handle the dataset selection logic.