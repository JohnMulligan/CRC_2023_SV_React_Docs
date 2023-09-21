# Documentation for formatTextURL Function

The `formatTextURL` function is a utility function that transforms a given input text into a URL-friendly format. It is typically used to generate clean and readable URLs from text by removing special characters, converting to lowercase, replacing spaces with dashes, and eliminating single-letter words.

## Usage
```jsx
/**
 * Format text into a URL-friendly format.
 *
 * @param {string} inputText - The input text to be formatted.
 * @returns {string} - A URL-friendly formatted text.
 */
export function formatTextURL(inputText: string): string {
    // Implementation details...
}
```

## Parameters
- `inputText` (required): The input text that you want to format into a URL-friendly version.


## Return Value
- A string representing the URL-friendly formatted text.

## Example
```jsx
// Example usage of formatTextURL function
const inputText1 = "Hello World!";
const inputText2 = "Amazing! This is Example Text.";
const inputText3 = "A B C D E F G H I J K L M N O P Q R S T U V W X Y Z";

const formattedText1 = formatTextURL(inputText1); // Output: "hello-world"
const formattedText2 = formatTextURL(inputText2); // Output: "amazing-this-is-example-text"
const formattedText3 = formatTextURL(inputText3); // Output: "b-c-d-e-f-h-i-j-l-m-o-q-t-u-v-w-y"

console.log(formattedText1);
console.log(formattedText2);
console.log(formattedText3);
```

In this example, the `formatTextURL` function is used to format three different input texts into URL-friendly formats. The resulting `formattedText1`, `formattedText2`, and `formattedText3` values represent the formatted text suitable for use in URLs or as identifiers. The function performs various transformations, including lowercase conversion, removal of special characters, replacement of spaces with dashes, and elimination of single-letter words.