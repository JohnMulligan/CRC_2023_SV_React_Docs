# Redux Store: getPeopleDataSetCollectionSlice

This code defines a Redux slice for managing a collection of people data sets. The slice is created using the `createSlice` function from the `@reduxjs/toolkit` library.

## Usage
To use this Redux slice, follow these steps:

1) Import the necessary modules and types:
```jsx
import { BaseFilter, InitialStateDataPeopleSetCollection } from '@/share/InterfactTypesDatasetCollection';
import jsonDataPEOPLECOLLECTIONS from '@/utils/flatfiles/PEOPLE_COLLECTIONS.json';
import { PayloadAction, createSlice } from '@reduxjs/toolkit';

```
2) Define the initial state for the people data set collection:

```jsx
export const initialState: InitialStateDataPeopleSetCollection = {
    value: jsonDataPEOPLECOLLECTIONS,
    textHeader: jsonDataPEOPLECOLLECTIONS[0].headers.label,
    textIntroduce: jsonDataPEOPLECOLLECTIONS[0].headers.text_introduce,
    styleNamePeople: jsonDataPEOPLECOLLECTIONS[0].style_name,
    dataSetValueBaseFilter: [],
    dataSetKeyPeople: '',
    dataSetValuePeople: [],
    blocksPeople: jsonDataPEOPLECOLLECTIONS[0].blocks,
    filterMenuFlatfile: jsonDataPEOPLECOLLECTIONS[0].filter_menu_flatfile,
    tableFlatfile: jsonDataPEOPLECOLLECTIONS[0].table_flatfile
};

```
3) Create the Redux slice using the createSlice function:

```jsx
export const getPeopleDataSetCollectionSlice = createSlice({
    name: 'getPeopleDataSetCollectionSlice',
    initialState,
    reducers: {
        setBaseFilterPeopleDataSetValue: (state, action: PayloadAction<BaseFilter[]>) => {
            state.dataSetValueBaseFilter = action.payload;
        },
        setBaseFilterPeopleDataKey: (state, action: PayloadAction<string>) => {
            state.dataSetKeyPeople = action.payload;
        },
        setBaseFilterPeopleDataValue: (state, action: PayloadAction<string[] | number[]>) => {
            state.dataSetValuePeople = action.payload;
        },
        setDataSetPeopleHeader: (state, action: PayloadAction<string>) => {
            state.textHeader = action.payload;
        },
        setPeopleTextIntro: (state, action: PayloadAction<string>) => {
            state.textIntroduce = action.payload;
        },
        setPeopleStyleName: (state, action: PayloadAction<string>) => {
            state.styleNamePeople = action.payload;
        },
        setPeopleBlocksMenuList: (state, action: PayloadAction<string[]>) => {
            state.blocksPeople = action.payload;
        },
        setPeopleFilterMenuFlatfile: (state, action: PayloadAction<string>) => {
            state.filterMenuFlatfile = action.payload;
        },
        setPeopleTableFlatfile: (state, action: PayloadAction<string>) => {
            state.tableFlatfile = action.payload;
        },
    },
});

```
4) Export the action creators and reducer from the slice:

```jsx
export const {
    setBaseFilterPeopleDataSetValue,
    setBaseFilterPeopleDataKey,
    setBaseFilterPeopleDataValue,
    setDataSetPeopleHeader,
    setPeopleTextIntro,
    setPeopleStyleName,
    setPeopleBlocksMenuList,
    setPeopleFilterMenuFlatfile,
    setPeopleTableFlatfile
} = getPeopleDataSetCollectionSlice.actions;

export default getPeopleDataSetCollectionSlice.reducer;

```

## State Structure

```jsx
{
    value: <jsonDataPEOPLECOLLECTIONS>,
    textHeader: <jsonDataPEOPLECOLLECTIONS[0].headers.label>,
    textIntroduce: <jsonDataPEOPLECOLLECTIONS[0].headers.text_introduce>,
    styleNamePeople: <jsonDataPEOPLECOLLECTIONS[0].style_name>,
    dataSetValueBaseFilter: [],
    dataSetKeyPeople: '',
    dataSetValuePeople: [],
    blocksPeople: <jsonDataPEOPLECOLLECTIONS[0].blocks>,
    filterMenuFlatfile: <jsonDataPEOPLECOLLECTIONS[0].filter_menu_flatfile>,
    tableFlatfile: <jsonDataPEOPLECOLLECTIONS[0].table_flatfile>
}

```
- `value`: The entire people data set collection loaded from the PEOPLE_COLLECTIONS.json file.
- `textHeader`: The label of the header for the current data set in the collection.
- `textIntroduce`: The introduction text for the current data set in the collection.
- `styleNamePeople`: The style name associated with the current data set in the collection.
- `dataSetValueBaseFilter`: An array representing the base filter values for the current data set.
- `dataSetKeyPeople`: The key associated with the current data set in the collection.
- `dataSetValuePeople`: An array of values associated with the current data set in the collection.
- `blocksPeople`: The blocks data associated with the current data set in the collection.
- `filterMenuFlatfile`: The filter menu flatfile associated with the current data set in the collection.
- `tableFlatfile`: The table flatfile associated with the current data set in the collection.

## Actions
This Redux slice defines several actions:

- `setBaseFilterPeopleDataSetValue`: Sets the base filter values for the people data set collection.
- `setBaseFilterPeopleDataKey`: Sets the key for the current data set in the people data set collection.
- `setBaseFilterPeopleDataValue`: Sets the values for the current data set in the people data set collection.
- `setDataSetPeopleHeader`: Sets the header label for the current data set in the people data set collection.
- `setPeopleTextIntro`: Sets the introduction text for the current data set in the people data set collection.
- `setPeopleStyleName`: Sets the style name for the current data set in the people data set collection.
- `setPeopleBlocksMenuList`: Sets the blocks data for the current data set in the people data set collection.
- `setPeopleFilterMenuFlatfile`: Sets the filter menu flatfile for the current data set in the people data set collection.
- `setPeopleTableFlatfile`: Sets the table flatfile for the current data set in the people data set collection.

## Reducer
The reducer function in this slice updates the state with the payload received from the corresponding actions.

## Example Usage
To use this Redux slice in your application, you can dispatch the provided actions with the desired payloads:
```jsx
import { useDispatch } from 'react-redux';
import {
    setBaseFilterPeopleDataSetValue,
    setBaseFilterPeopleDataKey,
    setBaseFilterPeopleDataValue,
    setDataSetPeopleHeader,
    setPeopleTextIntro,
    setPeopleStyleName,
    setPeopleBlocksMenuList,
    setPeopleFilterMenuFlatfile,
    setPeopleTableFlatfile
} from './path/to/getPeopleDataSetCollectionSlice';

// Inside a component or action creator
const dispatch = useDispatch();

// Dispatching actions with the desired payloads
dispatch(setBaseFilterPeopleDataSetValue(baseFilterValues));
dispatch(setBaseFilterPeopleDataKey(dataSetKey));
dispatch(setBaseFilterPeopleDataValue(dataSetValues));
dispatch(setDataSetPeopleHeader(headerLabel));
dispatch(setPeopleTextIntro(introductionText));
dispatch(setPeopleStyleName(styleName));
dispatch(setPeopleBlocksMenuList(blocks));
dispatch(setPeopleFilterMenuFlatfile(filterMenuFlatfile));
dispatch(setPeopleTableFlatfile(tableFlatfile));
```

This will update the state with the new values and trigger any relevant Redux state updates or subscriptions.

Note: Make sure to adjust the import paths according to your project structure.