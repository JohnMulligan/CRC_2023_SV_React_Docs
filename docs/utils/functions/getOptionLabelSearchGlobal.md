# Documentation for getOptionLabelSearchGlobal and shouldDisable Functions

The `getOptionLabelSearchGlobal` and shouldDisable functions are utility functions used for formatting and handling global search results in user interfaces.

### `getOptionLabelSearchGlobal Function`

## Usage
```jsx
/**
 * Get the label for a global search option based on its type and results count.
 *
 * @param {GlobalSearchProp} option - The GlobalSearchProp object representing the search option.
 * @returns {React.ReactNode} - The formatted label for the search option.
 */
export const getOptionLabelSearchGlobal = (option: GlobalSearchProp): React.ReactNode => {
    // Implementation details...
};
```

## Parameters
- `option (required):` A `GlobalSearchProp` object representing the search option for which you want to generate a label.

## Return Value
- A React node representing the formatted label for the search option.
#### `shouldDisable` Function

## Usage
```jsx
/**
 * Determine whether a global search option should be disabled based on its results count.
 *
 * @param {GlobalSearchProp} option - The GlobalSearchProp object representing the search option.
 * @returns {boolean} - A boolean indicating whether the option should be disabled.
 */
export const shouldDisable = (option: GlobalSearchProp): boolean => {
    // Implementation details...
};
```

## Parameters
`option (required):` A `GlobalSearchProp` object representing the search option for which you want to determine whether it should be disabled.

## Return Value
A boolean value indicating whether the search option should be disabled `(true)` or not `(false)`.

## Example
```jsx
// Example usage of getOptionLabelSearchGlobal and shouldDisable functions
const searchOption = {
    type: 'post',
    results_count: 5,
};

const label = getOptionLabelSearchGlobal(searchOption);
const isDisabled = shouldDisable(searchOption);

console.log("Search Option Label:", label);
console.log("Is Disabled:", isDisabled);
```
In this example, the `getOptionLabelSearchGlobal` function is used to generate a formatted label for a search option, and the `shouldDisable` function is used to determine whether the option should be disabled based on its results count. The `label` variable contains the formatted label, and the `isDisabled` variable indicates whether the option is disabled or not. These functions are typically used in user interfaces to display and manage search results.