# Flat Options Data Fetching

This module provides a function for fetching and processing flat options data. It uses the Options and VoyageOptionsValue interfaces from the @/share/InterfaceTypes module.

## Installation
No additional installation is required for this module.

## Usage
Import the necessary interfaces:
```jsx
import { Options, VoyageOptionsValue } from "@/share/InterfaceTypes";
```

`fetchOptionsFlat`

This function fetches and processes flat options data based on the provided parameters.

```jsx
export const fetchOptionsFlat = (
    isSuccess: boolean,
    options_flat: Record<string, unknown> | undefined,
    setOptionsFlat: (value: React.SetStateAction<Options>) => void
) => {
    if (isSuccess && options_flat) {
        const options: Options = {};

        Object.entries(options_flat).forEach(([key, value]) => {
            options[key] = value as VoyageOptionsValue;
        });

        setOptionsFlat(options);
        return options;
    }
};
```

To use this function, provide the following parameters:
- `isSuccess`: A boolean value indicating whether the fetch operation was successful.
- `options_flat:` The flat options data in the form of a Record<string, unknown> object.
- `setOptionsFlat:` A state setter function that sets the processed options data.

If the fetch operation is successful and `options_flat` is defined, the function iterates over the entries of `options_flat`. It assigns each key-value pair to the `options` object, ensuring the value is cast to `VoyageOptionsValue`. Then, it sets the processed options data using the `setOptionsFlat` state setter function. Finally, it returns the processed options data.

That's it! You can now use the `fetchOptionsFlat` function to fetch and process flat options data in your application.
