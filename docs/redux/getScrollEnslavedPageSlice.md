# getScrollEnslavedPageSlice

Scroll Enslaved Page Redux Slice
This code defines a Redux slice for managing the current page number for an enslaved scroll. The slice is created using the `createSlice` function from the `@reduxjs/toolkit` library.

## Usage
To use this Redux slice, follow these steps:

1) Import the necessary modules:
```jsx
import { PayloadAction, createSlice } from '@reduxjs/toolkit';

```
2) Create the Redux slice using the createSlice function:
```jsx
export const getScrollEnslavedPageSlice = createSlice({
    name: 'getScrollEnslavedPage',
    initialState: {
        currentEnslavedPage: 1,
    },
    reducers: {
        setCurrentEnslavedPage: (state, action: PayloadAction<number>) => {
            state.currentEnslavedPage = action.payload;
        },
    }
});

```
3) Export the action creator and reducer from the slice:
```jsx
export const { setCurrentEnslavedPage } = getScrollEnslavedPageSlice.actions;
export default getScrollEnslavedPageSlice.reducer;

```

## State Structure
The state structure of the scroll enslaved page slice is as follows:

```jsx
{
    currentEnslavedPage: 1
}
```
- currentEnslavedPage: The current page number for the enslaved scroll. It is initially set to 1.

## Actions
This Redux slice defines a single action:

- `setCurrentEnslavedPage`: Sets the current page number for the enslaved scroll. The payload should be a number representing the new page number.

## Reducer
The reducer function in this slice updates the state with the payload received from the `setCurrentEnslavedPage` action.

## Example Usage
To use this Redux slice in your application, you can dispatch the `setCurrentEnslavedPage` action with the desired page number payload:

```jsx
import { useDispatch } from 'react-redux';
import { setCurrentEnslavedPage } from './path/to/getScrollEnslavedPageSlice';

// Inside a component or action creator
const dispatch = useDispatch();

const page = 2; // Set the desired page number

dispatch(setCurrentEnslavedPage(page));

```
## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing data list values. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.


This will update the state with the new page number and trigger any relevant Redux state updates or subscriptions.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.

Note: Make sure to adjust the import paths according to your project structure.