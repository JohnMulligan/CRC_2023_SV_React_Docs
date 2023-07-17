# Redux Store: getDataSetCollectionSlice


This documentation provides an overview of the code presented, which defines a Redux slice for managing dataset collections in an application. Follow the guide below to understand how to use and customize this code.

## Prerequisites
Before using this code, ensure that you have the following dependencies installed:

- `@reduxjs/toolkit`: A Redux utility library that simplifies the process of creating Redux stores, actions, and reducers.

## Getting Started
To use this code in your Redux-based application, follow these steps:

1) Import the necessary types and the JSON data file:
```jsx
import { BaseFilter, InitialStateDataSetCollection } from '@/share/InterfactTypesDatasetCollection';
import jsonDataVoyageCollection from '@/utils/flatfiles/VOYAGE_COLLECTIONS.json';

```
2) Define the initial state of the dataset collection:

```jsx
export const initialState: InitialStateDataSetCollection = {
    value: jsonDataVoyageCollection,
    textHeader: jsonDataVoyageCollection[0].headers.label,
    textIntroduce: jsonDataVoyageCollection[0].headers.text_introduce,
    styleName: jsonDataVoyageCollection[0].style_name,
    dataSetValueBaseFilter: [],
    dataSetKey: '',
    dataSetValue: [],
    blocks: jsonDataVoyageCollection[0].blocks,
    pathName: ''
};

```

3) Create a Redux slice using createSlice:
```jsx
export const getDataSetCollectionSlice = createSlice({
    name: 'getDataSetCollection',
    initialState,
    reducers: {
        setBaseFilterDataSetValue: (state, action: PayloadAction<BaseFilter[]>) => {
            state.dataSetValueBaseFilter = action.payload;
        },
        setBaseFilterDataKey: (state, action: PayloadAction<string>) => {
            state.dataSetKey = action.payload;
        },
        setBaseFilterDataValue: (state, action: PayloadAction<string[] | number[]>) => {
            state.dataSetValue = action.payload;
        },
        setDataSetHeader: (state, action: PayloadAction<string>) => {
            state.textHeader = action.payload;
        },
        setTextIntro: (state, action: PayloadAction<string>) => {
            state.textIntroduce = action.payload;
        },
        setStyleName: (state, action: PayloadAction<string>) => {
            state.styleName = action.payload;
        },
        setBlocksMenuList: (state, action: PayloadAction<string[]>) => {
            state.blocks = action.payload;
        },
        setPathName: (state, action: PayloadAction<string>) => {
            state.pathName = action.payload;
        },
    },
});

```

4) Export the actions and reducer:
```jsx
export const { setBaseFilterDataSetValue, setPathName, setBlocksMenuList, setBaseFilterDataValue, setBaseFilterDataKey, setDataSetHeader, setTextIntro, setStyleName } = getDataSetCollectionSlice.actions;
export default getDataSetCollectionSlice.reducer;

```

## Actions
The following actions are available for manipulating the state related to dataset collections:

- `setBaseFilterDataSetValue`: Sets the base filter dataset values in the state based on the provided payload of type `BaseFilter[]`.
- `setBaseFilterDataKey`: Sets the base filter dataset key in the state based on the provided payload of type `string`.
- `setBaseFilterDataValue`: Sets the base filter dataset values in the state based on the provided payload of type `string[]` or number[].
- `setDataSetHeader`: Sets the dataset collection header text in the state based on the provided payload of type `string`.
- `setTextIntro`: Sets the dataset collection introduction text in the state based on the provided payload of type `string`.
- `setStyleName`: Sets the dataset collection style name in the state based on the provided payload of type `string`.
- `setBlocksMenuList`: Sets the dataset collection blocks in the state based on the provided payload of type `string[]`.
- `setPathName`: Sets the dataset collection path name in the state based on the provided payload of type `string`.

## Reducer
The reducer returned by this code manages the state of the dataset collection. It handles the actions defined in the slice and updates the state accordingly.

```jsx
export default getDataSetCollectionSlice.reducer;

```
## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing dataset collections. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.