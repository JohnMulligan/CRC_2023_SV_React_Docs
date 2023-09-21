# fetchInstitutionDataAPI

## Description
This is a Redux async thunk function for fetching auto-completed blog data from a backend API using Axios. It is intended for use in a Redux store to manage the state of auto-completed blog data in your application.

## Installation
Before using this code, make sure you have the following dependencies installed in your project:

- Redux: This code assumes you have a Redux store set up in your application.
- Axios: Axios is used for making HTTP requests and is required for sending the request to the backend API.
- Redux Toolkit: This code uses `createAsyncThunk` from Redux Toolkit for managing asynchronous actions.

You can install these dependencies using npm or yarn:
```js
npm install axios redux @reduxjs/toolkit
```

## Usage
1) Import the necessary dependencies and constants at the top of your Redux slice or wherever you intend to use this thunk:

```js
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '../../share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```
1) Create the fetchInstitutionDataAPI async thunk function using createAsyncThunk:

```jsx
export const fetchInstitutionDataAPI = createAsyncThunk(
    'BlogData/InstitutionDataAPI',
    async (formData?: FormData) => {
        try {
            const response = await axios.post(
                `${BASEURL}/blog/institution`,
                formData,
                {
                    headers: { 'Authorization': AUTHTOKEN },
                }
            );
            return response.data;
        } catch (error) {
            throw new Error('Failed to fetch fetchInstitutionDataAPI data');
        }
    }
);

```

1) Use this thunk action in your Redux slice to fetch auto-completed blog data from the backend API. For example, you can dispatch it like this:
```jsx
import { fetchInstitutionDataAPI } from './yourSlice';

// ...

dispatch(fetchInstitutionDataAPI(formData)).then((result) => {
    // Handle the result (success or error) here.
});
```

1) Make sure you have Redux set up to handle the state changes triggered by this thunk. You can define reducers and use the `createSlice` function from Redux Toolkit to manage your state.

2) Ensure that `AUTHTOKEN` and `BASEURL` are correctly configured with your API authentication token and base URL.

## Error Handling
This async thunk handles errors by throwing an error if the request to the backend API fails. You can catch this error when dispatching the thunk and handle it appropriately in your application.

## Contributing
If you would like to contribute to this code or report issues, please feel free to do so on the GitHub repository where this code is hosted.