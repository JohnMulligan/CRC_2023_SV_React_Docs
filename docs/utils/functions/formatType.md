# Documentation for formatType Function

The `formatType` function is a utility function designed to format a given type string into a more human-readable format. It provides enhanced readability by appending appropriate labels to specific types, such as "enslaved" and "blog."

## Usage
```jsx
/**
 * Format a type string into a more human-readable format.
 *
 * @param {string} type - The type string to be formatted.
 * @returns {string} - A human-readable formatted type string.
 */
export const formatType = (type: string): string => {
    // Implementation details...
};
```

## Parameters
- `type (required):` The type string that you want to format.

## Return Value
- A string representing the human-readable formatted type string.

## Example
```jsx
// Example usage of formatType function
const type1 = "enslaved";
const type2 = "blog";
const type3 = "article";

const formattedType1 = formatType(type1); // Output: "enslaved people"
const formattedType2 = formatType(type2); // Output: "blog posts"
const formattedType3 = formatType(type3); // Output: "article"

console.log(formattedType1);
console.log(formattedType2);
console.log(formattedType3);
```

In this example, the `formatType` function is used to format three different types. The resulting `formattedType1`, `formattedType2`, and `formattedType3` values represent the formatted type strings. The function appends appropriate labels, such as "people" for "enslaved" and "posts" for "blog," to provide a more meaningful and readable representation of the types.