# Options Data Fetching
This module provides functions for fetching options data and filtering it based on specific field types. It uses the Flatlabel, Options, VoyageOptionsValue, and TYPES interfaces from the @/share/InterfaceTypes module.

## Installation
No additional installation is required for this module.

## Usage
Import the necessary interfaces and constants:

```jsx 
import { Flatlabel, Options, VoyageOptionsValue, TYPES } from '@/share/InterfaceTypes';
```

``fetchOptionsData``

This function fetches options data and filters it to include only fields of type `CharField`.

```jsx
export const fetchOptionsData = async (data: Options) => {
    const options: Flatlabel[] = [];

    Object.entries(data).forEach(([key, value]: [string, VoyageOptionsValue], index: number) => {
        const charField = value.type.replace(/'>/g, "").split(".");
        charField.forEach((type) => {
            if (type === TYPES.CharField) {
                options.push({ key, label: value.flatlabel, id: index, type: type } as Flatlabel);
            }
        });
    });

    return options;
};
```

To use this function, pass the `Options` data as an argument. It will iterate over the data, extract the field type, and filter out only the fields of type `CharField`. The resulting `Flatlabel` objects are collected in the `options` array and returned.

`fetchOptionsDataIntegerField`

This function fetches options data and filters it to include fields of type `IntegerField` or `DecimalField`.

```jsx
export const fetchOptionsDataIntegerField = async (data: Options) => {
    const options: Flatlabel[] = [];

    Object.entries(data).forEach(([key, value]: [string, VoyageOptionsValue], index: number) => {
        const fieldTypes = [TYPES.IntegerField, TYPES.DecimalField];
        const fieldFound = value.type.replace(/'>/g, "").split(".").find((type) => fieldTypes.includes(type));
        if (fieldFound) {
            options.push({ key, label: value.flatlabel, id: index, type: fieldFound } as Flatlabel);
        }
    });

    return options;
};
```
To use this function, pass the `Options` data as an argument. It will iterate over the data, extract the field types, and filter out only the fields of type `IntegerField` or `DecimalField`. The resulting `Flatlabel` objects are collected in the `options` array and returned.

That's it! You can now use these functions to fetch options data and filter it based on specific field types in your application.