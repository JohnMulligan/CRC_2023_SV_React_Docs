# pastEnslavedApiService

This module provides an API service for fetching options related to past enslaved data from an API. It utilizes the Redux Toolkit Query library for data fetching and caching.

## Usage
To use this module, follow the steps below:

`) Install the necessary dependencies. This module requires the following dependencies:

- `@reduxjs/toolkit/query:` a library for efficient data fetching and caching in Redux
- `@vitejs/plugin-react-refresh`: a Vite plugin for React refresh functionality
You can install these dependencies using npm or yarn. Run the following command:
```js
npm install axios @reduxjs/toolkit
```

or 
```js
yarn add axios @reduxjs/toolkit
```
2) Import the necessary modules in your file:
```jsx
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react';
import { AUTHTOKEN, BASEURL } from '../../share/AUTH_BASEURL';
import { Options } from '@vitejs/plugin-react-refresh';

```

Make sure to replace `'../../share/AUTH_BASEURL'` with the actual relative path to your `AUTH_BASEURL` module.

3) Create the pastEnslavedApiService API service:
```jsx
export const pastEnslavedApiService = createApi({
    reducerPath: 'pastEnslavedApiService',
    baseQuery: fetchBaseQuery({ baseUrl: BASEURL }),
    endpoints: (builder) => ({
        getOptions: builder.query({
            query: () => ({
                url: 'past/enslaver/?hierarchical=False',
                method: 'OPTIONS',
                headers: { 'Authorization': AUTHTOKEN }
            }),
            transformResponse: (response: Options) => {
                return response;
            },
        }),
    }),
});

```

The `pastEnslavedApiService` is created using the `createApi` function from Redux Toolkit Query. 
It specifies a `reducerPath` and a `baseQuery` with the `BASEURL`. It also defines an `endpoints` object with a `getOptions` query endpoint.

4) Use the query endpoint in your code:

To fetch the options, you can use the `useGetOptionsQuery` hook provided by the `pastEnslavedApiService`:
```jsx
import { useGetOptionsQuery } from './pastEnslavedApiService';

const MyComponent = () => {
    const { data, error, isLoading } = useGetOptionsQuery();

    if (isLoading) {
        return <div>Loading...</div>;
    }

    if (error) {
        return <div>Error: {error.message}</div>;
    }

    // Use the data retrieved from the API
    console.log(data);

    return <div>Render your component here</div>;
};
```

The `useGetOptionsQuery` hook automatically handles fetching the options and provides the da`ta, `error`, and `isLoading` values for handling the different states of the request.

## API Reference
### pastEnslavedApiService
This is the API service created using the `createApi` function.

### Endpoints
- `getOptions`: Fetches options related to past enslaved data.

### Query Parameters
- None

### Returns
- `{ data, error, isLoading }`: An object containing the `data` (response from the API), `error` (error object if the request fails), and `isLoading` (boolean indicating if the request is still in progress).

## Hooks
- `useGetOptionsQuery()`: A hook for fetching options related to past enslaved data.

### Returns
- `{ data, error, isLoading }`: An object containing the `data` (response from the API), `error` (error object if the request fails), and `isLoading` (boolean indicating if the request is still in progress).

Please note that the documentation assumes the availability of the imported variables `AUTHTOKEN`, `BASEURL`, and `Options`.

Feel free to customize this README file according to your project's specific needs and guidelines.
