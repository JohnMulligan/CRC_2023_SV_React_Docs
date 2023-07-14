# fetchPastEnslavedRangeSliderData
This function is an asynchronous action creator that fetches voyage options with pagination from an API. It is designed to be used with the Redux Toolkit library.

## Usage
To use this function, follow the steps below:

1) Install the necessary dependencies. This function requires the following dependencies:

- `axios`: a popular HTTP client library
- `reduxjs/toolkit`: a library for efficient Redux development
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
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '@/share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```
Make sure to replace `'@/share/AUTH_BASEURL'` with the actual path to your `AUTH_BASEURL` module.

3) Define the `fetchPastEnslavedRangeSliderData` function:
```jsx
export const fetchPastEnslavedRangeSliderData = createAsyncThunk(
    'rangeSlider/fetchPastEnslavedRangeSliderData',
    async (formData: FormData) => {
        try {
            const response = await axios.post(
                `${BASEURL}past/enslaved/aggregations`,
                formData,
                {
                    headers: { 'Authorization': AUTHTOKEN },
                }
            );

            return response.data;
        } catch (error) {
            throw new Error('Failed to fetchPastEnslavedRangeSliderData data');
        }
    }
);

```

The `fetchPastEnslavedRangeSliderData` function is an asynchronous action creator. It takes a `formData` parameter of type `FormData` and returns a promise that resolves to the response from the API.
4)Use the function in your Redux logic:
You can dispatch the `fetchPastEnslavedRangeSliderData` action using Redux Toolkit's `dispatch` function:
```jsx
import { useDispatch } from 'react-redux';

const dispatch = useDispatch();

// Dispatch the action
dispatch(fetchPastEnslavedRangeSliderData(formData));
```

Replace formData with the actual form data you want to send in the POST request.

## API Reference
`fetchPastEnslavedRangeSliderData(formData: FormData): Promise<AxiosResponse>`
This asynchronous action creator fetches voyage options with pagination from an API. It sends a POST request to the specified `BASEURL` with the provided `formData` and includes the `AUTHTOKEN` in the request headers for authorization.

### Parameters
- `formData (FormData)`: The form data to be sent in the POST request.
### Returns
- `Promise<AxiosResponse>`: A promise that resolves to the response from the API. The response object follows the structure of the `AxiosResponse` interface from the Axios library.
### Throws
- `Error`: Throws an error if the API request fails with the message "Failed to fetchPastEnslavedRangeSliderData data".
Please note that the documentation assumes the availability of the imported variables `AUTHTOKEN`, `BASEURL`, and `FormData`.

Feel free to customize this README file according to your project's specific needs and guidelines.