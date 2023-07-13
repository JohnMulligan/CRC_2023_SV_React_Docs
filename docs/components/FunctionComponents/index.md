# Factory Component
The Factory component is a key component in the Voyage app that combines several sub-components to provide a comprehensive user interface for data analysis and visualization. It integrates the following components:

## Folder Structure
```
fcComponents/
|- index.md
|- AGTable.md
|- AutocompletedTree.md
|- Slider
|- TableCharacter
|- TableRangeSlider
```

## AGTable
The AGTable component displays data in a tabular format with advanced features such as sorting, filtering, and pagination. It provides an interactive and efficient way to explore and analyze large datasets.

## AutocompletedTree
The AutocompletedTree component is a combination of an autocomplete input and a tree view. It allows users to search for and select items from a hierarchical structure using auto-completion. This component is useful for navigating and selecting options from complex data hierarchies.

## Slider
The Slider component provides a user-friendly interface for selecting a value within a specified range. It allows users to adjust a numerical value by dragging a slider handle along a track. This component is commonly used for filtering and parameter selection.

## TableCharacter
The TableCharacter component presents categorical data in a table format. It displays the frequency or count of each category along with other relevant statistics. This component is useful for summarizing and analyzing categorical variables.

## TableRangeSlider
The TableRangeSlider component combines a table view with range sliders. It enables users to interactively filter and explore data based on a specified range of values. This component is particularly useful for exploring data distributions and identifying patterns within specific ranges.

## Usage
To use the Factory component and its sub-components, import them into your Voyage app and integrate them into your desired user interface:

```jsx
import Factory from "./Factory";
import AGTable from "./AGTable";
import AutocompletedTree from "./AutocompletedTree";
import Slider from "./Slider";
import TableCharacter from "./TableCharacter";
import TableRangeSlider from "./TableRangeSlider";

function App() {
  return (
    <div>
      <Factory>
        <AGTable />
        <AutocompletedTree />
        <Slider />
        <TableCharacter />
        <TableRangeSlider />
      </Factory>
    </div>
  );
}

```
