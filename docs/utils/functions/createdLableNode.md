# Documentation for Node and Edge Labeling Functions

This documentation explains a set of functions used for labeling nodes and edges in a network visualization, typically used to represent historical data related to enslaved individuals, voyages, and their associated details. These functions provide labels and stroke colors for nodes and edges based on the properties of the data.

## `createdLableNode` Function
## Overview
The `createdLableNode` function is used to generate labels for nodes in a network visualization. The label is determined based on the type of node (e.g., enslaved individuals, enslavers, voyages) and specific properties of the node.

## Usage
```jsx
/**
 * Generate a label for a node in a network visualization.
 *
 * @param {Nodes} node - The node object representing a data point.
 * @returns {string} - The label for the node.
 */
export const createdLableNode = (node: Nodes): string => {
    // Implementation details...
};
```

## Parameters
- `node (required):` The node object representing a data point in the network visualization.

## Return Value
- A string representing the label for the node.

## Example
```jsx
// Example usage of createdLableNode function
const nodeData = {
    node_class: ENSLAVEDNODE,
    documented_name: "John Smith",
    voyage_ship__ship_name: "HMS Example",
    voyage_dates__imp_arrival_at_port_of_dis_sparsedate__year: 1780,
    principal_alias: "Alias1",
};

const label = createdLableNode(nodeData);
console.log(label); // Output: "John Smith, HMS Example, 1780"
```

## `createdLableNodeHover` Function

## Overview
The `createdLableNodeHover` function generates labels for nodes in a network visualization, particularly for hover-over tooltips. The label is based on the type of node and specific properties of the node.

## Usage
```jsx
/**
 * Generate a label for a node in a network visualization (for hover-over tooltips).
 *
 * @param {Nodes} node - The node object representing a data point.
 * @returns {string} - The label for the node tooltip.
 */
export const createdLableNodeHover = (node: Nodes): string => {
    // Implementation details...
};
```

## Parameters
- `node (required):` The node object representing a data point in the network visualization.

## Return Value
- A string representing the label for the node tooltip.

## Example
```jsx
// Example usage of createdLableNodeHover function
const nodeData = {
    node_class: ENSLAVEDNODE,
    documented_name: "John Smith",
    voyage_ship__ship_name: "HMS Example",
    voyage_dates__imp_arrival_at_port_of_dis_sparsedate__year: 1780,
    principal_alias: "Alias1",
};

const label = createdLableNodeHover(nodeData);
console.log(label); // Output: "John Smith, HMS Example, 1780"
```

## `createdLableEdges` Function

## Overview
The `createdLableEdges` function generates labels for edges (connections) between nodes in a network visualization. The label is determined based on properties of the edge data.

## Usage
```jsx
/**
 * Generate a label for an edge (connection) in a network visualization.
 *
 * @param {Edges} edge - The edge object representing a connection between nodes.
 * @returns {string} - The label for the edge.
 */
export const createdLableEdges = (edge: Edges): string => {
    // Implementation details...
};
```

## Parameters
`edge (required):` The edge object representing a connection between nodes in the network visualization.

## Return Value
- A string representing the label for the edge.

## Example 
```jsx
// Example usage of createdLableEdges function
const edgeData = {
    data: {
        role__name: "Captain",
    },
};

const label = createdLableEdges(edgeData);
console.log(label); // Output: "Captain"
```
## `createSrokeColor` Function

##  Overview
The `createSrokeColor` function generates stroke colors for edges in a network visualization. The color is determined based on properties of the edge data.

## Usage
```jsx
/**
 * Generate a stroke color for an edge (connection) in a network visualization.
 *
 * @param {Edges} edge - The edge object representing a connection between nodes.
 * @returns {string} - The stroke color for the edge.
 */
export const createSrokeColor = (edge: Edges): string => {
    // Implementation details...
};
```

## Parameters
- `edge (required):` The edge object representing a connection between nodes in the network visualization.

## `Return Value`
- A string representing the stroke color for the edge.

## Example
```jsx
// Example usage of createSrokeColor function
const edgeData = {
    data: {
        role__name: "Captain",
    },
};

const color = createSrokeColor(edgeData);
console.log(color); // Output: "rgb(55, 163, 154)"
```
This documentation outlines the purpose, usage, parameters, and return values of each function, providing a clear understanding of how to use them to label nodes and edges and specify stroke colors in a network visualization context.