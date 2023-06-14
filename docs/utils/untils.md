# Utils Folder
The "utils" folder in this application contains utility functions and helper modules that provide various commonly used functionalities across different parts of the application. These utilities serve to improve code organization, reusability, and maintainability.

```
|-utils.md   |-getEnumColumnParams.ts
|            |-createRowData.ts
|            |-transatlantic_voyages_filter_menu.json
|            |-transatlantic_voyages_filter_menuTEST.json
|            |-VOYAGE_BARGRAPH_OPTIONS.json
|            |-VOYAGE_SCATTER_OPTIONS.json 

```

The folder contains multiple utility files, each focusing on a specific area or functionality. This modular approach allows for easier maintenance and separation of concerns.

- ```getEnumColumnParams.ts```
This file includes utility functions related to the table column with cellRenderer 

- ```transatlantic_voyages_filter_menu.json && transatlantic_voyages_filter_menuTEST.json```

This file file provides utility datas as json for working with voyages filter and displays on the menu bar, will call from the function 
<code>getOptionsFlatObjSlice</code>
in the reduce reducer.

## Usage
```js
import { createSlice } from "@reduxjs/toolkit"
import jsonData from '@/utils/transatlantic_voyages_filter_menu.json'
import jsonData from '@/utils/transatlantic_voyages_filter_menuTEST.json'
const initialState = {
    value: jsonData
};
export const getOptionsFlatObjSlice = createSlice({
    name: "menuOptionFlat",
    initialState,
    reducers: {
        getOptionsFlatMenu: (state, action) => {
            state.value = action.payload;
        }
    }
})

export const { getOptionsFlatMenu } = getOptionsFlatObjSlice.actions;
export default getOptionsFlatObjSlice.reducer;

```
## Display at the menu bar
![getOptionsFlatMenu](../assets/menu.png)


- ```VOYAGE_BARGRAPH_OPTIONS.json && VOYAGE_SCATTER_OPTIONS.json```
This file file provides utility datas as json to display with BarGraph and Scatter as the dropdown selection menu
<code>getOptionsFlatObjSlice</code>
in the <code>BarGraph.tsx</code> and  <code>Scatter.tsx</code>


- <code>Scatter.tsx</code>
![Scatter](../assets/scatterDropdown.png)

- <code>BarGraph.tsx</code> 
![Scatter](../assets/barGraphDropdown.png)


<br>
<h3> Contribution </h3>
If you would like to contribute to the "utils" folder by adding more utility functions or improving existing ones, please follow the contribution guidelines outlined in the project's main README file.