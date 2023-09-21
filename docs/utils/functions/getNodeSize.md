# Documentation for getNodeSize and getEdgesSize Functions

The `getNodeSize` and `getEdgesSize` functions are utility functions used to calculate the size of nodes and edges in a network or graph visualization, respectively. These functions are designed to handle specific attributes and weights associated with nodes and edges.

## `getNodeSize` Function
## Usage
```jsx
/**
 * Calculate the size of a node based on its weights and attributes.
 *
 * @param {NodeAggroutes} node - The NodeAggroutes object representing the node.
 * @returns {number|null} - The calculated node size or null if no weights are found.
 */
export function getNodeSize(node: NodeAggroutes): number | null {
    // Implementation details...
}

```
## Parameters
- `node (required)`: A NodeAggroutes object representing the node for which you want to calculate the size.

## Return Value
- A number representing the calculated node size, or null if no weights are found in the node.

### `getEdgesSize Function`

## Usage
```jsx
/**
 * Get the size of an edge.
 *
 * @param {Transportation} edges - The Transportation object representing the edge.
 * @returns {number|null} - The size of the edge or null if no edge is provided.
 */
export function getEdgesSize(edges: Transportation): number | null {
    // Implementation details...
}
```

## Parameters
- `edges (required):` A `Transportation` object representing the edge for which you want to get the size.

## Return Value
- A number representing the size of the edge, or null if no edge is provided.

## Example

```jsx
// Example usage of getNodeSize and getEdgesSize functions
const nodeData = {
    weights: {
        disembarkation: 50,
        embarkation: 30,
        'post-disembarkation': 10,
        origin: 5,
    },
};

const edgeData = {
    w: 25,
};

const nodeSize = getNodeSize(nodeData); // Output: 95
const edgeSize = getEdgesSize(edgeData); // Output: 25

console.log("Node Size:", nodeSize);
console.log("Edge Size:", edgeSize);
```

In this example, the `getNodeSize` function is used to calculate the size of a node based on its weights and attributes, and the `getEdgesSize` function is used to retrieve the size of an edge. The resulting `nodeSize` and `edgeSize` values represent the calculated sizes for the node and edge, respectively.