# Redux Store Configuration Documentation
## Overview
The provided code configures a Redux store for a React application using Redux Toolkit. This store manages the state of the application by combining reducers from various slices and middleware. It also sets up API middleware for handling asynchronous actions using Redux Toolkit's `createAsyncThunk` and `createSlice`.


## Dependencies
- Redux Toolkit: This code utilizes Redux Toolkit, a library that simplifies the setup of Redux store and actions.
- Redux API Middleware: Middleware for handling API requests asynchronously is set up for multiple API services `(voyagesApi, pastEnslavedApiService, pastEnslaversApiService)`.

## Store Configuration
The Redux store is configured using `configureStore` from Redux Toolkit. It includes the following components:

## Reducers
The store combines multiple reducers, each corresponding to a specific slice of the application's state. The reducers are defined for the following slices:


- `getOptionsDataSlice`
- `rangeSliderSlice`
- `getAutoCompleteList`
- `getOptionsFlatMenu`
- `getScrollPageSlice`
- `getTableSlice`
- `getFilterSlice`
- `getColumnsSlice`
- `getDataSetCollectionSlice`
- `getPeopleEnslavedDataSetCollectionSlice`
- `getPeopleEnslaversDataSetCollectionSlice`
- `getScrollEnslavedPageSlice`
- `getScrollEnslaversPageSlice`
- `getFilterPeopleObjectSlice`
- `getOptionsDataPastPeopleEnslavedSlice`
- `getBlogDataSlice`
- `getLanguagesSlice`
- `getCommonGlobalSearchResultSlice`
- `getPastNetworksGraphDataSlice`
- `getNodeEdgesAggroutesMapDataSlice`
- `getCardFlatObjectSlice`
- `getPivotTablesDataSlice`
- `getGeoTreeDataSlice`
- `getDataPathNameSlice`
- `voyagesApi.reducer` (API middleware)
- `pastEnslavedApiService.reducer` (API middleware)
- `pastEnslaversApiService.reducer` (API middleware)
## Middleware
Middleware is configured to handle asynchronous actions, particularly API requests. The following middleware is used:

- Redux Toolkit's `getDefaultMiddleware` is extended to include API middleware for `voyagesApi`, `pastEnslavedApiService`, and `pastEnslaversApiService`. This middleware is used for handling API calls and asynchronous actions.

## Redux Toolkit's `setupListeners`
The `setupListeners` function from Redux Toolkit is used to set up listeners for the API services, allowing the store to react to events such as API requests and responses.

## Exported Types
- `AppDispatch`: A type representing the dispatch function used in the application. It is based on the `dispatch` function of the Redux store.
- `RootState`: A type representing the root state of the Redux store. It is based on the result type of the `store.getState()` function.

## Usage
This configured Redux store can be used throughout the application to manage and access the application's state. Components can dispatch actions to update the state and select data from the state using Redux Toolkit's hooks and selectors.

## Example Usage
```jsx
import { useDispatch, useSelector } from 'react-redux';
import { setOptionsData } from './getOptionsDataSlice';

// Dispatching an action to update the state
const dispatch = useDispatch();
dispatch(setOptionsData({ /* data to update */ }));

// Selecting data from the state
const optionsData = useSelector((state) => state.getOptions.data);
```

Feel free to modify the initial state, actions, and reducer based on your specific requirements.

Note: Make sure to adjust the import paths according to your project structure.
