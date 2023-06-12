# AutoComplete API
This module provides a function for making an asynchronous API request to fetch autocomplete data for a given key option. It uses axios and Redux Toolkit's createAsyncThunk for handling the HTTP request.

## Installation
To use the AutoComplete API module, make sure you have axios and Redux Toolkit installed:

```js
npm install axios
npm install @reduxjs/toolkit
```

## Usage
Import the necessary functions and constants:

```jsx 
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '../share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```
Create the fetchAutoComplete thunk using the createAsyncThunk function:

```jsx 
export const fetchAutoComplete = createAsyncThunk(
    'autoComplete/fetchAutoCompleteLists',
    async (keyOptions: FormData) => {
        try {
            const response = await axios.post(
                `${BASEURL}voyage/autocomplete2`,
                keyOptions,
                {
                    headers: { 'Authorization': AUTHTOKEN },
                }
            );
            return response.data;
        } catch (error) {
            throw new Error('Failed to fetch AutoCompleteLists data');
        }
    }
);

```

The ``fetchAutoComplete`` thunk is now configured to make an API request to fetch autocomplete data. It uses axios to send a POST request to the specified URL with the provided key options in the request body. 
The `AUTHTOKEN` is added to the request headers for authorization.

To use the ``fetchAutoComplete`` thunk in your Redux store, dispatch it like any other Redux action:

Example:
```jsx

import { useDispatch } from 'react-redux';
import { fetchAutoComplete } from './path/to/your/file';

const AutocompleteBox = () => {
    const dispatch = useDispatch();

      useEffect(() => {
    const formData: FormData = new FormData();
    formData.append(varName, autoValue);
    dispatch(fetchAutoComplete(formData))
      .unwrap()
      .then((response: any) => {
        if (response) {
          setAutoLists(response?.results);
        }
      })
      .catch((error: Error) => {
        console.log("error", error);
      });
  }, [dispatch, varName, autoValue]);
};
```

You can then handle the fetched autocomplete data in your Redux reducers or handle it in your components as needed.

That's it! You can now use the AutoComplete API module to fetch autocomplete data for your application.