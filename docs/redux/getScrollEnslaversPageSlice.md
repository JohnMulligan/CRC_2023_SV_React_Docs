# getScrollEnslaversPageSlice

Scroll Enslavers Page Redux Slice
This code defines a Redux slice for managing the current page number for an Enslavers scroll. The slice is created using the `createSlice` function from the `@reduxjs/toolkit` library.

## Usage
To use this Redux slice, follow these steps:

1) Import the necessary modules:
```jsx
import { PayloadAction, createSlice } from '@reduxjs/toolkit';

```
2) Create the Redux slice using the createSlice function:
```jsx
export const getScrollEnslaversPageSlice = createSlice({
    name: 'getScrollEnslaversPage',
    initialState: {
        currentEnslaversPage: 1,
    },
    reducers: {
        setCurrentEnslaversPage: (state, action: PayloadAction<number>) => {
            state.currentEnslaversPage = action.payload;
        },
    }
});

```
3) Export the action creator and reducer from the slice:
```jsx
export const { setCurrentEnslaversPage } = getScrollEnslaversPageSlice.actions;
export default getScrollEnslaversPageSlice.reducer;

```

## State Structure
The state structure of the scroll Enslavers page slice is as follows:

```jsx
{
    currentEnslaversPage: 1
}
```
- currentEnslaversPage: The current page number for the Enslavers scroll. It is initially set to 1.

## Actions
This Redux slice defines a single action:

- `setCurrentEnslaversPage`: Sets the current page number for the Enslavers scroll. The payload should be a number representing the new page number.

## Reducer
The reducer function in this slice updates the state with the payload received from the `setCurrentEnslaversPage` action.

## Example Usage
To use this Redux slice in your application, you can dispatch the `setCurrentEnslaversPage` action with the desired page number payload:

```jsx
import { useDispatch } from 'react-redux';
import { setCurrentEnslaversPage } from './path/to/getScrollEnslaversPageSlice';

// Inside a component or action creator
const dispatch = useDispatch();

const page = 2; // Set the desired page number

dispatch(setCurrentEnslaversPage(page));

```

## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing dataset collections. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.

Note: Make sure to adjust the import paths according to your project structure.
