# Documentation for convertToSlug

## Overview
The `convertToSlug` function is a utility function that converts a given string into a URL-friendly slug. It is commonly used to create human-readable URLs from titles, names, or other textual data. This function performs several transformations on the input string to ensure it adheres to URL naming conventions.

## Usage

```jsx
/**
 * Converts a string into a URL-friendly slug.
 *
 * @param {string} str - The input string to be converted.
 * @returns {string} - A URL-friendly slug derived from the input string.
 */
export function convertToSlug(str: string): string {
    // Implementation details...
}
```

## Parameters
- `str (required):` The input string that you want to convert into a slug.
## Return Value
- A URL-friendly slug as a string. This slug is created by performing the following transformations on the input string:
    - Convert the string to lowercase.
    - Remove apostrophes (').
    - Replace non-word characters (e.g., spaces, punctuation) with dashes (-).
    - Remove leading and trailing dashes.

## Example
```jsx
// Example usage of convertToSlug function
const inputString = "This is an Example String! It's Awesome!";
const slug = convertToSlug(inputString);
console.log(slug); // Output: "this-is-an-example-string-its-awesome"
```

In this example, the `convertToSlug` function is used to convert the `inputString` into a URL-friendly slug. The resulting `slug` can be used in URLs or as part of a clean and readable identifier.