# pastEnslaversApiService

## Description
`pastEnslaversApiService` is a JavaScript service created using the Redux Toolkit's `createApi` and `fetchBaseQuery` from the `@reduxjs/toolkit/query/react` package. This service is designed to make API requests related to past enslavers data. It includes an endpoint, getOptions, for fetching options related to past enslaver data.

## Installation
Before using this code, make sure you have the following dependencies installed in your project:

- Redux Toolkit: This code uses Redux Toolkit and `@reduxjs/toolkit/query/react` for managing API requests and state in your Redux store.
- The necessary dependencies to configure your Redux store with Redux Toolkit.

You can install these dependencies using npm or yarn:
```js
npm install @reduxjs/toolkit/query/react
```

## Usage
1) Import the necessary dependencies and constants at the top of your JavaScript file:

```jsx
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react';
import { AUTHTOKEN, BASEURL } from '../../share/AUTH_BASEURL';
import { Options } from '@vitejs/plugin-react-refresh';
```
1) Create the `pastEnslaversApiService` using `createApi`. Define the `baseQuery` configuration to specify the base URL for API requests.

```jsx
export const pastEnslaversApiService = createApi({
    reducerPath: 'pastEnslaversApiService',
    baseQuery: fetchBaseQuery({ baseUrl: BASEURL }),
    endpoints: (builder) => ({
        getOptions: builder.query({
            query: () => ({
                url: '/past/enslaver/?hierarchical=False',
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

1) Use the generated hooks for making API requests. In this case, you can use the `useGetOptionsQuery` hook to fetch options related to past enslaver data:

```jsx
export const { useGetOptionsQuery } = pastEnslaversApiService;
```

1) To use the `useGetOptionsQuery` hook in your React components, you can import it and use it like this:

```jsx
import { useGetOptionsQuery } from './pastEnslaversApiService';

function YourComponent() {
    const { data, error } = useGetOptionsQuery();

    if (error) {
        // Handle the error here.
    }

    if (data) {
        // Handle the data here.
    }

    // Render your component.
}
```

1) Make sure that `AUTHTOKEN` and `BASEURL` are correctly configured with your API's authentication token and base URL.


## Hierarchical Parameter
The API endpoint URL includes the `hierarchical=Fals`e query parameter, which you can customize based on your specific requirements. This parameter may affect the response structure or data returned by the API.

## Contributing
If you would like to contribute to this code or report issues, please feel free to do so on the GitHub repository where this code is hosted.