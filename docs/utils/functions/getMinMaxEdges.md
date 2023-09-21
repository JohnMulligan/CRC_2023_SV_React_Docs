# Documentation for getMinEdges and getMaxEdges Functions

The `getMinEdges` and `getMaxEdges` functions are utility functions used to calculate the minimum and maximum edge sizes within a collection of transportation edges. These functions are helpful for determining the range of edge sizes in a network or graph visualization.

## Usage
### `getMinEdges Function`

```jsx
/**
 * Calculate the minimum edge size within a collection of transportation edges.
 *
 * @param {Transportation[]} edges - An array of transportation edges.
 * @returns {number} - The minimum edge size.
 */
export const getMinEdges = (edges: Transportation[]): number => {
    // Implementation details...
};
```

### `getMaxEdges Function`
```jsx
/**
 * Calculate the maximum edge size within a collection of transportation edges.
 *
 * @param {Transportation[]} edges - An array of transportation edges.
 * @returns {number} - The maximum edge size.
 */
export const getMaxEdges = (edges: Transportation[]): number => {
    // Implementation details...
};
```

## Parameters
- `edges (required):` An array of Transportation objects representing transportation edges.

## Return Value
- `getMinEdges Function:` Returns the minimum edge size (a number) within the collection of edges.

- `getMaxEdges Function:` Returns the maximum edge size (a number) within the collection of edges.

## Example
```jsx
// Example usage of getMinEdges and getMaxEdges functions
const edgesData = [
    { id: 1, size: 5 },
    { id: 2, size: 10 },
    { id: 3, size: 3 },
    { id: 4, size: 7 },
    { id: 5, size: 2 },
];

const minEdgeSize = getMinEdges(edgesData); // Output: 2
const maxEdgeSize = getMaxEdges(edgesData); // Output: 10

console.log("Minimum Edge Size:", minEdgeSize);
console.log("Maximum Edge Size:", maxEdgeSize);
```

In this example, the `getMinEdges` and `getMaxEdges` functions are used to calculate the minimum and maximum edge sizes within the `edgesData` array. The resulting `minEdgeSize` and `maxEdgeSize` values represent the minimum and maximum edge sizes, respectively. These functions are useful for visualizing and scaling edges in network or graph representations.