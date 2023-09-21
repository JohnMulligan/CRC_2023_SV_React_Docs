# Voyage Graph Grouping Data Fetching

This module provides a function for fetching voyage graph grouping data using axios and Redux Toolkit's `createAsyncThunk`. It utilizes the `AUTHTOKEN` and `BASEURL` constants from the `@/share/AUTH_BASEURL` module.

## Installation
No additional installation is required for this module.

## Usage
Import the necessary modules:

```jsx
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '@/share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```
`fetchVoyageGraphGroupby`

This function fetches voyage graph grouping data based on the provided parameters.

```jsx
export const fetchVoyageGraphGroupby = createAsyncThunk(
    'VoyageGroupby/fetchVoyageScatterGroupby',
    async (formData: FormData) => {
        try {
            const response = await axios.post(
                `${BASEURL}voyage/groupby2`,
                formData,
                {
                    headers: { 'Authorization': AUTHTOKEN },
                }
            );
            return response.data;
        } catch (error) {
            throw new Error('Failed to fetch fetchVoyageScatterGroupby data');
        }
    }
);
```

To use this function, provide the following parameters:

- `formData`: The form data to be sent with the POST request.
The function uses axios to make a POST request to the specified URL `${BASEURL}voyage/groupby2`. It includes the `formData` and sets the request headers with the `AUTHTOKEN`. The response data is returned if the request is successful. If an error occurs, an error message is thrown.


That's it! You can now use the fetchVoyageGraphGroupby function to fetch voyage graph grouping data in your application.