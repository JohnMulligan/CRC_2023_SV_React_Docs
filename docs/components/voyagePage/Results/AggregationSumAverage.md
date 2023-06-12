# Aggregation Sum Average Component

This component represents the aggregation options for sum and average.

## Installation
No additional installation is required for this component.

## Usage
Import the necessary modules:
```jsx
import {
  Alert,
  AlertTitle,
  FormControl,
  FormControlLabel,
  FormLabel,
  Radio,
  RadioGroup,
  Typography,
} from "@mui/material";
import { ChangeEvent, FunctionComponent } from "react";
import { Options, VoyagesOptionProps } from "@/share/InterfaceTypes";
```
`AggregationSumAverage`

This component represents the aggregation options for sum and average.

```jsx 
interface AggregationSumAverageProps {
  showAlert: boolean;
  aggregation: string;
  handleChange: (event: ChangeEvent<HTMLInputElement>, value: string) => void;
  optionFlat: Options;
  scatterOptions: VoyagesOptionProps;
}

export const AggregationSumAverage: FunctionComponent<AggregationSumAverageProps> = (props) => {
  // Component logic goes here
};
```

## Component Structure
The component structure includes MUI components such as `FormControl`, `RadioGroup`, `FormControlLabel`, and `Typography` to handle the aggregation options and display an alert if needed.

## Component Logic
The component logic includes handling the selected aggregation option, displaying an alert based on the showAlert prop, and handling the change event when selecting an aggregation option.

## Example Usage
```jsx
import { AggregationSumAverage } from "./AggregationSumAverage";

function Scatter() {
  return (
    <div>
      {/* Other components */}
      <AggregationSumAverage
        showAlert={true}
        aggregation="sum"
        handleChange={handleChange}
        optionFlat={options}
        scatterOptions={scatterOptions}
      />
      {/* Other components */}
    </div>
  );
}

export default Scatter;
```
<br/>

![aggregation](../../../assets/aggregation.png)

That's it! You can now use the `AggregationSumAverage` component to provide aggregation options for sum and average in your application.