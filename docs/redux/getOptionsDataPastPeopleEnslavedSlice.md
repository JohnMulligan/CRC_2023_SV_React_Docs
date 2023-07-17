# Redux Store: getOptionsDataPastPeopleEnslavedSlice

This code defines a Redux slice for managing options data related to past enslaved people. The slice is created using the `createSlice` function from the `@reduxjs/toolkit` library.

## Usage
To use this Redux slice, follow these steps:

1) Install the required dependencies by running `npm install @reduxjs/toolkit`.

2) Import the necessary modules and types:
```jsx
import { createSlice, PayloadAction } from '@reduxjs/toolkit';
import { OptionsDataState } from '@/share/InterfaceTypes';

```
3) Define the initial state for the options data:
```jsx
const initialState: OptionsDataState = {
    value: {},
};

```
4) Create the Redux slice using the `createSlice` function:
```jsx
export const getOptionsDataPastPeopleEnslavedSlice = createSlice({
    name: 'getOptionsEnslaved',
    initialState,
    reducers: {
        getOptionsEnslaved: (state, action: PayloadAction<Record<string, never>>) => {
            state.value = action.payload;
        },
    },
});

```

5) Export the action creator and reducer from the slice:

```jsx
export const { getOptionsEnslaved } = getOptionsDataPastPeopleEnslavedSlice.actions;
export default getOptionsDataPastPeopleEnslavedSlice.reducer;

```
## State Structure

The state structure of the options data slice is as follows:
```jsx
{
    value: {}
}

```

- `value`: An object containing the options data related to past enslaved people. The specific structure of the options data depends on the implementation and usage.
## Actions
This Redux slice defines a single action:

- `getOptionsEnslaved`: Sets the options data state to the value provided in the payload. The payload should be a record type `(Record<string, never>)` representing the options data related to past enslaved people.

## Reducer
The reducer function in this slice updates the state with the payload received from the `getOptionsEnslaved` action.

## Example Usage
To use this Redux slice in your application, you can dispatch the `getOptionsEnslaved` action with the desired options data payload:
```jsx
import { useDispatch } from 'react-redux';
import { getOptionsEnslaved } from './path/to/getOptionsDataPastPeopleEnslavedSlice';

// Inside a component or action creator
const dispatch = useDispatch();

const optionsData = {
    // Define your options data here
    // ...
};

dispatch(getOptionsEnslaved(optionsData));
```
This will update the state with the new options data and trigger any relevant Redux state updates or subscriptions.

Note: Make sure to adjust the import paths according to your project structure.