# getFilterPeopleObjectSlice

Filter People Object Redux Slice
This code defines a Redux slice for managing a filter menu object used to filter people. The slice is created using the createSlice function from the @reduxjs/toolkit library.

## Usage
To use this Redux slice, follow these steps:

1) Install the required dependencies by running `npm install @reduxjs/toolkit.`
2) Import the necessary modules and files:
```jsx
import { PayloadAction, createSlice } from '@reduxjs/toolkit';
import { ValuePeopleFilter, InitialStateFilterPeopleMenu } from '@/share/InterfaceTypes';
import ENSLAVED_FILTER_MENU from '@/utils/flatfiles/enslaved_filter_menu.json';
import AFRICAN_FILTER_MENU from '@/utils/flatfiles/african_origins_filter_menu.json';
import TEXAS_FILTER_MENU from '@/utils/flatfiles/texas_filter_menu.json';

```
3) Define the initial state for the filter menu object:
```jsx
const initialState: InitialStateFilterPeopleMenu = {
    value: {
        valueEnslaved: ENSLAVED_FILTER_MENU,
        valueAfricanOrigin: AFRICAN_FILTER_MENU,
        valueTexas: TEXAS_FILTER_MENU
    }
};

```
4) Create the Redux slice using the `createSlice` function:
```jsx
export const getFilterPeopleObjectSlice = createSlice({
    name: 'getFilterPeopleObject',
    initialState,
    reducers: {
        getFilterPeopleObject: (state, action: PayloadAction<ValuePeopleFilter>) => {
            state.value = action.payload;
        }
    }
});

```
5) Export the action creators and reducer from the slice:
```jsx
export const { getFilterPeopleObject } = getFilterPeopleObjectSlice.actions;
export default getFilterPeopleObjectSlice.reducer;

```
## State Structure
The state structure of the filter menu object slice is as follows:

```jsx
{
    value: {
        valueEnslaved: <enslaved_filter_menu.json>,
        valueAfricanOrigin: <african_origins_filter_menu.json>,
        valueTexas: <texas_filter_menu.json>
    }
}

```
- `valueEnslaved`: The filter menu object for the enslaved filter, loaded from `enslaved_filter_menu.json`.
- `valueAfricanOrigin`: The filter menu object for the African origins filter, loaded from `african_origins_filter_menu.json`.
- `valueTexas`: The filter menu object for the Texas filter, loaded from `texas_filter_menu.json`.

## Action
This Redux slice defines a single action:

- `getFilterPeopleObject`: Updates the state with a new filter menu object. The payload of this action should be of type `ValuePeopleFilter`.

## Reducer
The reducer function in this slice updates the state with the payload received from the `getFilterPeopleObject` action.

## Example Usage
To use this Redux slice in your application, you can dispatch the `getFilterPeopleObject` action with the desired filter menu object payload:

```jsx
import { useDispatch } from 'react-redux';
import { getFilterPeopleObject } from './path/to/getFilterPeopleObjectSlice';

// Inside a component or action creator
const dispatch = useDispatch();

const filterMenuObject = {
    // Define your filter menu object here
    // ...
};

dispatch(getFilterPeopleObject(filterMenuObject));

```

## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing dataset collections. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.


This will update the state with the new filter menu object and trigger any relevant Redux state updates or subscriptions.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.
Note: Make sure to adjust the import paths according to your project structure.
