# Redux Store: rangeSliderSlice
The rangeSliderSlice slice in the Redux store manages the state related to range slider functionality in the application.

### Slice Configuration
The rangeSliderSlice is configured using the createSlice function from the @reduxjs/toolkit package. It defines the following properties:

- `name`: The name of the slice is set to "rangeSlider".
- `initialState`: The initial state of the slice includes the following properties:

    - `rangeValue` : Represents the range values for the slider and is initially an ``empty object``.
    - `loading`: A boolean flag indicating whether the data is being fetched, initially set to ``false``.
    - `error`: A boolean flag indicating whether an error occurred during the data fetch, initially set to ``false``.
    - `varName`: Represents the variable name associated with the range slider, initially an ``empty string``.
    - `isChange`: A boolean flag indicating whether the range slider value has changed, initially set to `false`.
    - `rangeSliderMinMax`: Represents the minimum and maximum values for the range slider, initially an ``empty object``.
### Actions
The `rangeSliderSlice` slice defines the following actions:

- `setRangeValue`: Accepts a payload of type `Record<string, number[]>` and updates the rangeValue property in the state with the provided values.
- `setKeyValue`: Accepts a payload of type string and updates the varName property in the state with the provided value.
- `setIsChange`: Accepts a payload of type boolean and updates the isChange property in the state with the provided value.
- `setRangeSliderValue`: Accepts a payload of type `Record<string, number[]>` and updates the rangeSliderMinMax property in the state with the provided values.

### Usage
To use the ```rangeSliderSlice``` in other parts of the application, follow these steps:

1) Import the necessary actions and the reducer function from `rangeSliderSlice`.
2) Dispatch the actions `(setRangeValue, setKeyValue, setIsChange, setRangeSliderValue)` when needed, providing the appropriate payload values.
Example usage:
```jsx
import { setRangeValue, setKeyValue, setIsChange, setRangeSliderValue } from './path/to/rangeSliderSlice';
import { useDispatch, useSelector } from 'react-redux';

// Inside a component
const dispatch = useDispatch();

// Dispatching the actions
dispatch(setRangeValue({...rangeValue,[varName]: initialValue as number[]}));
dispatch(setKeyValue(value));
dispatch(setIsChange(!isChange));
dispatch(setRangeSliderValue({...rangeSliderMinMax,[varName]: currentSliderValue as number[]}));

// Accessing the state
const rangeValue = useSelector(state => state.rangeSlider.rangeValue);
const varName = useSelector(state => state.rangeSlider
const { rangeValue, varName, rangeSliderMinMax } = useSelector((state: RootState) => state.rangeSlider as RangeSliderState);
```