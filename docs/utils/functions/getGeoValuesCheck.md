# Documentation for getGeoValuesCheck Function

The `getGeoValuesCheck` function is a utility function designed to extract and collect values from a hierarchical data structure represented by an array of `GeoTreeSelectDataProps` objects. It recursively traverses the tree structure to retrieve all values within the tree.
## Usage

```jsx
/**
 * Recursively collect values from a hierarchical data structure.
 *
 * @param {string[]} values - An array to store the collected values.
 * @param {GeoTreeSelectDataProps[]} geo_array - An array of GeoTreeSelectDataProps representing the hierarchical data structure.
 * @returns {string[]} - An array containing all the collected values.
 */
export function getGeoValuesCheck(values: string[], geo_array: GeoTreeSelectDataProps[]): string[] {
    // Implementation details...
}
```

## Parameters
- `values (required):` An array used to store the collected values.
- `geo_array (required):` An array of GeoTreeSelectDataProps objects representing the hierarchical data structure.

## Return Value
- An array of strings containing all the collected values from the hierarchical data structure.


## Example
```js
// Example usage of getGeoValuesCheck function
const geoData = [
    {
        value: "1",
        children: [
            {
                value: "1.1",
                children: [
                    { value: "1.1.1" },
                    { value: "1.1.2" },
                ],
            },
            {
                value: "1.2",
                children: [
                    { value: "1.2.1" },
                    { value: "1.2.2" },
                ],
            },
        ],
    },
    {
        value: "2",
        children: [
            { value: "2.1" },
            { value: "2.2" },
        ],
    },
];

const collectedValues = getGeoValuesCheck([], geoData);

console.log(collectedValues);
```

In this example, the `getGeoValuesCheck` function is used to collect values from the geoData array, which represents a hierarchical data structure. The resulting `collectedValues` array contains all the values from the structure. The function recursively traverses the hierarchy to gather the values.