# Fetch API Service Voyages API
This module provides a ```voyagesApi``` function and hook for making API requests to retrieve options data related to voyages. It utilizes Redux Toolkit's query package and axios for handling the HTTP requests.

## Installation
To use the Voyages API module, make sure you have the following dependencies installed:

```
npm install @reduxjs/toolkit
npm install @reduxjs/toolkit/query react-query
npm install axios

```

## Usage
Import the necessary functions and constants:

```jsx
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '../share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```

Create the voyagesApi object using the createApi function:

```jsx
export const voyagesApi = createApi({
    reducerPath: "voyagesApi",
    baseQuery: fetchBaseQuery({ baseUrl: BASEURL }),
    endpoints: (builder) => ({
        getOptions: builder.query({
            query: () => ({
                url: "voyage/?hierarchical=false",
                method: "OPTIONS",
                headers: { 'Authorization': AUTHTOKEN }
            }),
            transformResponse: (response: Options) => {
                return response
            },
        })
    })
});
```

The ```voyagesApi``` object is now configured to make API requests. It has an endpoint called getOptions that fetches options data related to voyages. The ``transformResponse`` function is used to handle the response received from the API.

To use the `getOptions` endpoint in your React components, destructure the `useGetOptionsQuery` hook:

```jsx 
import { useGetOptionsQuery } from "@/fetchAPI/fetchApiService";
```

You can then use the useGetOptionsQuery hook in your components to fetch the options data:

```jsx
const datas = useSelector((state: RootState | any) => state.getOptions?.value);

const { data: options_flat, isLoading, isError, isSuccess} = useGetOptionsQuery(datas);
  ```

   
  ```jsx 
  const Scatter = () => {
    const { data, isLoading, isError } = useGetOptionsQuery();

    if (isLoading) {
    return <div className="spinner"></div>;
  }

    if (isError) {
        return <div>Error occurred while fetching options data.</div>;
    }

    // Use the fetched options data
    // ...
};
```
The data property contains the fetched options data, isLoading indicates if the data is currently being fetched, and isError indicates if an error occurred during the fetch.

That's it! You can now use the Voyages API module to fetch options data for your voyages-related functionality.