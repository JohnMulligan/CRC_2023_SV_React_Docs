# getRowsPerPage Function

This function is used to determine the number of rows per page in a table based on the dimensions of the window. It utilizes a predefined set of breakpoints to determine the appropriate number of rows based on the window width and height.

## Usage
To use this function, follow these steps:

1) Define the getRowsPerPage function:

```jsx
const breakpoints = [
    { width: 1366, height: 768, rowsPerPage: 10 },       // Desktops and laptops: 1366x768
    { width: 1920, height: 1080, rowsPerPage: 12 },     // Desktops and laptops: 1920x1080
    { width: 2560, height: 1440, rowsPerPage: 15 },     // Desktops and laptops: 2560x1440
    { width: 768, height: 1024, rowsPerPage: 8 },       // Tablets: 768x1024
    { width: 1536, height: 2048, rowsPerPage: 20 },      // Tablets: 1536x2048
    { width: 320, height: 480, rowsPerPage: 5 },        // Mobile phones: 320x480
    { width: 375, height: 667, rowsPerPage: 5 },        // Mobile phones: 375x667
    { width: 414, height: 736, rowsPerPage: 5 },        // Mobile phones: 414x736
    { width: 360, height: 640, rowsPerPage: 5 },        // Mobile phones: 360x640
];

export const getRowsPerPage = (windowWidth: number, windowHeight: number) => {
    const breakpoint = breakpoints.find((bp) => windowWidth <= bp.width && windowHeight <= bp.height);
    return breakpoint ? breakpoint.rowsPerPage : 20;
};
```
## Parameters
The `getRowsPerPage` function accepts two parameters:

- `windowWidth`: A number representing the width of the window or viewport.
- `windowHeight`: A number representing the height of the window or viewport.

## Return Value
The function returns a number representing the recommended number of rows per page based on the window dimensions. It determines the appropriate number of rows by finding the first breakpoint in the predefined `breakpoints` array where the window width is less than or equal to the breakpoint width and the window height is less than or equal to the breakpoint height. If no matching breakpoint is found, a default value of 20 rows per page is returned.

## Example Usage
Here's an example of how you can use the `getRowsPerPage` function:
```jsx
const windowWidth = 1366;   // Example window width
const windowHeight = 768;   // Example window height

const rowsPerPage = getRowsPerPage(windowWidth, windowHeight);
console.log(rowsPerPage);

```

This will determine the number of rows per page based on the provided window dimensions and log the result to the console.

Note: You can adjust the `windowWidth` and `windowHeight` values to match your specific use case.

Note: The predefined `breakpoints` array can be customized or expanded to suit your application's specific needs and desired breakpoints.

Note: Make sure to adjust the import paths according to your project structure.