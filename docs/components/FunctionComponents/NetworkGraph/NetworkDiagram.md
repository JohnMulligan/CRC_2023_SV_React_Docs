# NetworkDiagram Component Documentation

The `NetworkDiagram` component is a React component designed for visualizing network diagrams using `D3.js` within a canvas element. This component allows you to render nodes and edges representing entities and connections in a network. Users can interact with the network diagram, including zooming, dragging, and clicking on nodes. This documentation provides an overview of the component, its purpose, and usage.

## Purpose
The primary purpose of the `NetworkDiagram` component is to create an interactive network diagram visualization within a canvas. It uses D3.js for managing the layout of nodes and edges, enabling users to perform the following actions:

- Zoom in and out of the diagram.
- Drag nodes to reposition them.
- Double-click on nodes to trigger custom actions.
- Click on nodes to show additional information or trigger other events.

## Props
The `NetworkDiagram` component accepts the following props:

- `width` (number): The width of the canvas where the network diagram is rendered.

- `height` (number): The height of the canvas where the network diagram is rendered.

- `data` (Datas): An object containing data about nodes and edges in the network diagram.

- `handleNodeDoubleClick` (function): A function that is called when a node is double-clicked. It typically takes the `nodeId` and nodeClass as parameters to perform custom actions.

- `handleClickNodeShowCard` (function): A function that is called when a node is clicked. It typically takes the `nodeId` and `nodeClass` as parameters to display additional information or trigger other events.

## Usage
To use the `NetworkDiagram` component, follow these steps:

1) Ensure that you have the required dependencies installed, including `React` and `D3.js.`

2) Import the `NetworkDiagram` component into your React application.

3) Render the `NetworkDiagram` component within your application, providing the required props.

4) Customize the interaction behavior by implementing the `handleNodeDoubleClick` and `handleClickNodeShowCard` functions to define specific actions when nodes are double-clicked or clicked.

```jsx
import React from 'react';
import { NetworkDiagramSlaveVoyages } from './NetworkDiagramSlaveVoyages'; // Adjust the import path as needed

function NetworkDiaNetworkDiagramSlaveVoyagesgram() {
  // Define data for the network diagram
  const diagramData = {
    nodes: [...], // Define an array of node data
    edges: [...], // Define an array of edge data
  };

  // Handle double-click on a node
  const handleNodeDoubleClick = (nodeId, nodeClass) => {
    // Implement custom logic here
    console.log('Node double-clicked:', nodeId, nodeClass);
  };

  // Handle click on a node
  const handleClickNodeShowCard = (nodeId, nodeClass) => {
    // Implement custom logic here
    console.log('Node clicked:', nodeId, nodeClass);
  };

  return (
    <div>
      <h2>Network Diagram</h2>
      <NetworkDiagram
        width={800} // Adjust the width as needed
        height={600} // Adjust the height as needed
        data={diagramData}
        handleNodeDoubleClick={handleNodeDoubleClick}
        handleClickNodeShowCard={handleClickNodeShowCard}
      />
    </div>
  );
}

export default NetworkDiagramSlaveVoyages;

```

## Interactions
The `NetworkDiagram` component provides the following user interactions:

1) `Double-Click:` When a node is double-clicked, the `handleNodeDoubleClick` function is called, passing the `nodeId` and `nodeClass` as parameters. You can customize this function to perform actions based on the double-click event.

2) `Click:` When a node is clicked, the `handleClickNodeShowCard` function is called, passing the `nodeId` and `nodeClass` as parameters. You can customize this function to display additional information or trigger other events based on the click event.

3) `Drag:` Users can drag nodes to reposition them within the diagram. Node positions are updated automatically.

4) `Zoom:` Users can zoom in and out of the diagram to adjust the view. Zooming is supported using `D3.js.`


Make sure to adapt the `NetworkDiagram` component to your specific use case and styling requirements. Customize the interaction behavior and appearance as needed for your application.