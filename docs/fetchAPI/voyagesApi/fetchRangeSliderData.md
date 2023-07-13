# Fetch Range Slider Data
This module encapsulates the logic for sending HTTP requests and demonstrates how to fetch range slider data using axios and Redux Toolkit's createAsyncThunk. It also handles request headers and parses the response data. The response data will be in the form of a variable with the key and corresponding min and max values.


## Installation
To use this code, make sure you have the following dependencies installed:

axios: "^0.21.4"
@reduxjs/toolkit: "^1.6.1"
You can install these dependencies by running the following command:

```npm install axios @reduxjs/toolkit```

## Usage
1) Import the required modules and constants:

```jsx 
import axios from 'axios';
import { AUTHTOKEN, BASEURL } from '@/share/AUTH_BASEURL';
import { createAsyncThunk } from '@reduxjs/toolkit';
```

2)  Define the fetchRangeSliderData async thunk:

```jsx
export const fetchRangeSliderData = createAsyncThunk(
    'rangeSlider/fetchRangeData',
    async (formData: FormData) => {
        try {
            const response = await axios.post(
                `${BASEURL}voyage/aggregations`,
                formData,
                {
                    headers: { 'Authorization': AUTHTOKEN },
                }
            );

            return response.data;
        } catch (error) {
            throw new Error('Failed to fetch range slider data');
        }
    }
);
```
This async thunk sends a POST request to ${BASEURL}voyage/aggregations with the provided formData and includes the AUTHTOKEN in the request headers. It returns the response data upon success or throws an error if the request fails.

3) You can now use the fetchRangeSliderData async thunk in your Redux actions or slices to fetch range slider data.
```jsx
import { fetchRangeSliderData } from './path/to/fetchRangeSliderData';

// Dispatch the async thunk
dispatch(fetchRangeSliderData(formData))
    .then((data) => {
        // Handle successful response data
    })
    .catch((error) => {
        // Handle error
    });
```

Make sure to replace path/to/fetchRangeSliderData with the actual path to the file where you have defined the fetchRangeSliderData async thunk.

### Contributing
Contributions are welcome! If you find any issues or want to add new features, please submit a pull request.