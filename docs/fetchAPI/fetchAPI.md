# Fetch API Folder

This Readme file provides an explanation of the Fetch API folder and how to use it in the application.

## Introduction
The Fetch API folder contains modules and utilities related to making HTTP requests using the Fetch API. The Fetch API provides a modern and flexible way to interact with server resources asynchronously.


## Folder Structure
```
fetchAPI
|──pastEnslavedApi
    ├── fetchPastEnslavedApiService.ts
    ├── fetchPastEnslavedAutoCompleted.ts
    ├── fetchPastEnslavedOptionsList.ts
    ├── fetchPastEnslavedSortedTableData
    ├── fetchPastEnslavedRangeSliderData.ts
|──voyagesApi
    ├── fetchApiService.ts
    ├── fetchAutoCompleted.ts
    ├── fetchOptionsData.ts
    ├── fetchOptionsFlat.ts
    ├── fetchRangeSliderData.ts 
    ├── fetchVoyageGroupby.ts
    ├── fetchVoyageOptionsPagination.ts
    ├── fetchVoyagesOptionsApi.ts
    └── fetchVoyageSortedData.ts


```
- ```fetchApiService.ts```
This module encapsulates the ```voyagesApi``` function
logic for sending HTTP requests and demonstrates how to fetch options data using axios and Redux Toolkit's by OPTIONS requests
createAsyncThunk. It also handles request headers and parses the response data. The response data will be in the form of objects with key variable name and type, label and flatlabel.

- ```fetchAutoCompleted.ts```
This module provides a function for making an asynchronous API request to fetch autocomplete data for a given key option. It uses axios and Redux Toolkit's createAsyncThunk for handling the HTTP request.

- ```fetchOptionsData.ts```
This module provides functions for fetching options data and filtering it based on specific field types. It uses the Flatlabel, Options, VoyageOptionsValue, and TYPES interfaces from the @/share/InterfaceTypes module.

- ```fetchOptionsFlat.ts```
This module provides a function for fetching and processing flat options data. It uses the `Options` and `VoyageOptionsValue` interfaces from the `@/share/InterfaceTypes` module.

- ```fetchRangeSliderData.ts ```
This module encapsulates the logic for sending HTTP requests and demonstrates how to fetch range slider data using axios and Redux Toolkit's createAsyncThunk. It also handles request headers and parses the response data. The response data will be in the form of a variable with the key and corresponding min and max values.

- ```fetchVoyageGroupby.ts ```
This module provides a function for fetching voyage graph grouping data using axios and Redux Toolkit's `createAsyncThunk`. It utilizes the `AUTHTOKEN` and `BASEURL` constants from the `@/share/AUTH_BASEURL` module.

## Installation
To use the Fetch API folder in your application, follow these steps:

1) Copy the Fetch API folder into your project directory.

2) Install the required dependencies. The Fetch API folder might depend on libraries such as axios or others. Make sure to install these dependencies based on the specific requirements of the Fetch API folder.

3) Import the necessary modules and functions into your application files where you need to make API requests.

## Usage
Here is an example of how to use the Fetch API folder to make an API request:

```jsx
import { fetchRangeSliderData } from '@/fetchAPI/fetchAggregationsSlider';

  useEffect(() => {
    const formData: FormData = new FormData();
    formData.append("aggregate_fields", varName);
    dispatch(fetchRangeSliderData(formData))
      .unwrap()
      .then((response: any) => {
        if (response) {
          const initialValue: number[] = [
            response[varName].min,
            response[varName].max,
          ];
          dispatch(setKeyValue(varName));
          dispatch(
            setRangeValue({
              ...rangeValue,
              [varName]: initialValue as number[],
            })
          );
        }
      })
      .catch((error: any) => {
        console.log("error", error);
      });
  }, [dispatch, varName]);

```

In this example, we import the fetchRangeSliderData function from fetchRangeSliderData.ts and We then use the fetchRangeSliderData function to make a POST request to the specified user endpoint and handle the response or error accordingly.

Please refer to the individual files within the Fetch API folder for more detailed documentation and usage examples.


## Contributing
Contributions to the Fetch API folder are welcome. If you find any issues or want to add new features, please submit a pull request.