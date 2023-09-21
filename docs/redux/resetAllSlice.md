# resetAllSlice

## Overview
The provided code defines a Redux action named `resetAllSlice`, which is responsible for dispatching reset actions to reset multiple Redux slices to their initial states. This action is typically used when you want to reset the entire state of your Redux store or specific slices.

## Dependencies
- Redux Toolkit: This code utilizes Redux Toolkit, a library that simplifies the setup of Redux store and actions.

## Action Function: `resetAll`
The `resetAll` action is a function that dispatches reset actions for multiple Redux slices to reset their states. The dispatched actions include the following:

### Reset Actions Dispatched

1) `resetOptionsData:` Resets the state managed by the `getOptionsDataSlice`.
2) `resetGeoTreeData:` Resets the state managed by the `getGeoTreeDataSlice`.
3) `resetRangeSliderData:` Resets the state managed by the `rangeSliderSlice`.
4) `resetAutoCompleteData:` Resets the state managed by the `getAutoCompleteSlice`.
5) `resetDataSetCollectionData:` Resets the state managed by the `getDataSetCollectionSlice`.
6) `resetVoyagesFilter:` Resets the state managed by the `getFilterSlice`.
4) `resetFilterPeopleData:` Resets the state managed by the `getFilterPeopleObjectSlice`.
8) `resetNodeEdgesAggroutesMapData:` Resets the state managed by the `getNodeEdgesAggroutesMapDataSlice`.
9) `resetOptionDataPastEnslaved:` Resets the state managed by the `getOptionsDataPastPeopleEnslavedSlice`.
10) `resetOptionPlatObjectData:` Resets the state managed by the `getOptionsFlatObjSlice`.
11)` resetPeopleEnslavedDataSetCollection:` Resets the state managed by the `getPeopleEnslavedDataSetCollectionSlice`.
12) `resetPeopleEnslaversDataSetCollection:` Resets the state managed by the `getPeopleEnslaversDataSetCollectionSlice`.
13) `resetScroolVoyages:` Resets the state managed by the `getScrollPageSlice`.
14) `resetScroolEnslaved:` Resets the state managed by the `getScrollEnslavedPageSlice`.
15) `resetScroolEnslavers:` Resets the state managed by the `getScrollEnslaversPageSlice`.

## Usage
The `resetAll` action can be dispatched within your Redux store to reset multiple slices simultaneously. It can be useful when you want to reset the entire state or a specific subset of your application's state.

## Example Dispatch

```jsx
import { useDispatch } from 'react-redux';
import { resetAll } from './resetAllSlices';

// Dispatching the resetAll action to reset multiple Redux slices
const dispatch = useDispatch();
dispatch(resetAll());
```

## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing data list collections. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.

Note: Make sure to adjust the import paths according to your project structure.
