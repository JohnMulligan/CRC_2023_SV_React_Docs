# CRC_2023_SV_React_Docs

This documentation will guide you through the process of setting up a Vite React app with TypeScript, Redux Toolkit, and Material UI. Follow the steps below to get started.

## Prerequisites
Make sure you have Node.js and npm (Node Package Manager) installed on your machine. You can download and install them from the official Node.js website: https://nodejs.org.
 
**Step 1: Create a new Vite React App**

Open your terminal or command prompt and run the following command to create a new Vite React app with TypeScript template:

```
npx create-vite@latest my-app --template react-ts
```

This command will create a new directory called range-slider app with the basic structure and dependencies for a Vite React app with TypeScript.


**Step 2: Install Redux Toolkit and Material UI**

Change to the project directory:
```
cd my-app
```

Install Redux Toolkit and Material UI packages using the following command:
```
npm install @reduxjs/toolkit react-redux @mui/material @emotion/react @emotion/styled
```

**Step 3: Configure Redux Toolkit**
In the ```src``` directory, create a new directory called ```redux```. Inside the ```redux``` directory, create a file called ```store.ts```. 
This file will contain the configuration for your Redux store.

Add the following code to store.ts:

```javascript
import { configureStore } from "@reduxjs/toolkit";
import getOptionsReducer from './opptionsDataSlice';
import getRangeSliderReducer from './getRangeSliderSlice';
import { voyagesApi } from '../fetchAPI/fetchApiService';

const store = configureStore({
    reducer: {
        getOptions: getOptionsReducer,
        getRangeSlider: getRangeSliderReducer,
        [voyagesApi.reducerPath]: voyagesApi.reducer
    },
    middleware: (getDefaultMiddleware) =>
        getDefaultMiddleware({
            serializableCheck: false,
        }).concat(voyagesApi.middleware)
});

export default store;
```

**Step 4: Set Up Redux Slices**
In the ```src``` directory, create a new directory called ```redux```. This directory will contain your Redux "slices" - individual pieces of state and logic managed by Redux Toolkit.

Create a sample feature slice by creating a file called ```optionsDataSlice.ts```  inside the ```redux``` directory. Add the following code to ```optionsDataSlice.ts```:
```javascript
import { createSlice, PayloadAction } from "@reduxjs/toolkit";
import { OptionsDataState } from '../share/TableRangeSliderType'


const initialState: OptionsDataState = {
    value: {},
};

export const optionsDataSlice = createSlice({
    name: "optionsData",
    initialState,
    reducers: {
        getOptions: (state, action: PayloadAction<Record<string, unknown>>) => {
            state.value = action.payload;
        },
    },
});

export const { getOptions } = optionsDataSlice.actions;
export default optionsDataSlice.reducer;

```

**Step 5: Configure Material UI**

In the ```src``` directory, create a file called App.tsx and replace its contents with the following code:

```javascript
import TableRangeSlider from './components/TableRangeSlider'
import { QueryClient, QueryClientProvider } from "react-query";
import { Provider } from 'react-redux';
import store from './redux/store';

function App() {

  const queryClient = new QueryClient()

  return (
    <Provider store={store}>
      <QueryClientProvider client={queryClient}>
        <HOME />
      </QueryClientProvider>
    </Provider>
  )
}
export default App;


```
