# Documentation for getMinValueNode and getMaxValueNode Functions

The `getMinValueNode` and `getMaxValueNode` functions are utility functions used to calculate the minimum and maximum node sizes within a collection of nodes. These functions are helpful for determining the range of node sizes in a network or graph visualization.

## Usage
### `getMinValueNode Function`
```jsx
/**
 * Calculate the minimum node size within a collection of nodes.
 *
 * @param {NodeAggroutes[]} nodesData - An array of NodeAggroutes objects representing nodes.
 * @returns {number} - The minimum node size.
 */
export const getMinValueNode = (nodesData: NodeAggroutes[]): number => {
    // Implementation details...
};

```

### `getMaxValueNode Function`

```jsx
/**
 * Calculate the maximum node size within a collection of nodes.
 *
 * @param {NodeAggroutes[]} nodesData - An array of NodeAggroutes objects representing nodes.
 * @returns {number} - The maximum node size.
 */
export const getMaxValueNode = (nodesData: NodeAggroutes[]): number => {
    // Implementation details...
};
```

## Parameters
- `nodesData (required):` An array of NodeAggroutes objects representing nodes in a network or graph visualization.
## Return Value
- `getMinValueNode Function:` Returns the minimum node size (a number) within the collection of nodes.

- `getMaxValueNode Function:` Returns the maximum node size (a number) within the collection of nodes.

## Example

```jsx
// Example usage of getMinValueNode and getMaxValueNode functions
const nodesData = [
    { id: 1, size: 20 },
    { id: 2, size: 10 },
    { id: 3, size: 30 },
    { id: 4, size: 15 },
    { id: 5, size: 5 },
];

const minNodeSize = getMinValueNode(nodesData); // Output: 5
const maxNodeSize = getMaxValueNode(nodesData); // Output: 30

console.log("Minimum Node Size:", minNodeSize);
console.log("Maximum Node Size:", maxNodeSize);
```

In this example, the `getMinValueNode` and `getMaxValueNode` functions are used to calculate the minimum and maximum node sizes within the `nodesData` array. The resulting `minNodeSize` and `maxNodeSize` values represent the minimum and maximum node sizes, respectively. These functions are useful for visualizing and scaling nodes in network or graph representations.