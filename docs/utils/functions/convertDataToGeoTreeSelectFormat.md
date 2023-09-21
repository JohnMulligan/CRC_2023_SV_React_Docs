# Documentation for convertDataToGeoTreeSelectFormat

## Overview
The `convertDataToGeoTreeSelectFormat` function is a utility function that converts a hierarchical data structure into a format suitable for use with a GeoTreeSelect component. This function is designed to work with data that represents a tree-like structure, where each item can have child items, and it converts this data into an array of `TreeSelectItem` objects.

## Usage
```jsx
import { GeoTreeSelectDataProps, TreeSelectItem } from "@/share/InterfaceTypes";

/**
 * Converts hierarchical data into a format suitable for GeoTreeSelect component.
 *
 * @param {GeoTreeSelectDataProps[]} data - The hierarchical data to be converted.
 * @param {boolean} includeSelectAll - Indicates whether to include a "Select All" option at the top level.
 * @returns {TreeSelectItem[]} - An array of TreeSelectItem objects representing the converted data.
 */
export const convertDataToGeoTreeSelectFormat = (
    data: GeoTreeSelectDataProps[],
    includeSelectAll: boolean = true
): TreeSelectItem[] => {
    // Implementation details...
};
```

## Parameters
- `data (required):` An array of `GeoTreeSelectDataProps` objects representing the hierarchical data to be converted. Each object should have properties like `id`, `value`, `name`, and `children`.

- `includeSelectAll (optional)`: A boolean flag indicating whether to include a "Select All" option at the top level of the tree. Defaults to `true`.

## Return Value
- An array of `TreeSelectItem` objects representing the converted data. Each `TreeSelectItem` object has the following properties:

    - `id (number):` A unique identifier for the item.
    - `key (string):` A string key for the item.
    - `title (string):` The display title for the item.
    - `value (string):` The value associated with the item.
    - `children (TreeSelectItem[]):` An array of child TreeSelectItem objects representing the item's sub-items.
    - `disabled (boolean):` A boolean flag indicating whether the item is disabled. It is disabled when there are no children items.

## Example

```jsx
import { GeoTreeSelectDataProps, TreeSelectItem } from "@/share/InterfaceTypes";

// Sample hierarchical data
const hierarchicalData: GeoTreeSelectDataProps[] = [
    {
        id: 1,
        value: 'country',
        name: 'Country',
        children: [
            {
                id: 101,
                value: 'region',
                name: 'Region',
                children: [
                    {
                        id: 1001,
                        value: 'city',
                        name: 'City',
                        children: [],
                    },
                ],
            },
        ],
    },
];

// Convert the data to GeoTreeSelect format
const treeSelectData: TreeSelectItem[] = convertDataToGeoTreeSelectFormat(hierarchicalData);

console.log(treeSelectData);

```

In this example, the `convertDataToGeoTreeSelectFormat` function is used to convert hierarchical data into a format suitable for a `GeoTreeSelect` component. The resulting `treeSelectData` array can then be used to populate the `GeoTreeSelect` component with the appropriate options.