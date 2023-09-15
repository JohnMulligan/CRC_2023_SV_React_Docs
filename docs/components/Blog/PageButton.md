# `BlogPageButton`

## Introduction
`BlogPageButton` is a React functional component designed to provide a pagination control feature for a list of blog posts. This component allows users to navigate between different pages of blog post results. It displays the current page number, total number of pages, and provides buttons for navigating to the first, previous, next, and last pages. This README documentation explains the purpose of the component and provides guidance on how to use it within your React application.

## Installation
To use the `BlogPageButton` component, you need to ensure that your React project is set up correctly and that you have the required dependencies installed. Here are the steps to include this component in your project:

1) Import the necessary dependencies and components at the beginning of your file:

```jsx
import { BlogDataProps } from '@/share/InterfaceTypesBlog';
import { Link } from 'react-router-dom';

```

1) Create an interface named PageButtonBlogProp to define the props required by the BlogPageButton component.

```jsx
interface PageButtonBlogProp {
  setCurrentBlogPage: React.Dispatch<React.SetStateAction<number>>;
  currentBlogPage: number;
  imagesPerPage: number;
  BlogData: BlogDataProps[];
}
```

1) Create the BlogPageButton component using the defined props.

```jsx
const BlogPageButton = (props: PageButtonBlogProp) => {
  // ...
  // Component structure and logic go here
  // ...
};
```
1) Implement the component structure by arranging the JSX markup and adding the necessary logic to handle pagination.

2) Return the JSX that represents the pagination control for the list of blog posts.

3) Export the BlogPageButton component as the default export of your module.

## Usage
To use the `BlogPageButton` component in your React application, follow these steps:

1) Import the `BlogPageButton` component into the file where you want to display pagination controls for a list of blog posts.

```jsx
import BlogPageButton from './BlogPageButton'; // Adjust the import path as needed

```

1) Place the `BlogPageButton` component within your JSX to render the pagination controls.

```jsx
<BlogPageButton
  setCurrentBlogPage={setCurrentBlogPage}
  currentBlogPage={currentBlogPage}
  imagesPerPage={imagesPerPage}
  BlogData={BlogData}
/>
```
1) Ensure that you have set up the necessary state and data in your component to provide the required props to the `BlogPageButton` component.

## Example
Here's an example of how to use the `BlogPageButton` component within a React application:

```jsx
import React, { useState } from 'react';
import BlogPageButton from './BlogPageButton'; // Adjust the import path as needed

function BlogList() {
  // Initialize state and data for the blog list
  const [currentBlogPage, setCurrentBlogPage] = useState(1);
  const imagesPerPage = 10; // Number of blog post images per page
  const BlogData = [/* ... */]; // An array of blog post data

  return (
    <div>
      {/* Render the list of blog posts */}
      {/* ... */}
      {/* Render the BlogPageButton component */}
      <BlogPageButton
        setCurrentBlogPage={setCurrentBlogPage}
        currentBlogPage={currentBlogPage}
        imagesPerPage={imagesPerPage}
        BlogData={BlogData}
      />
    </div>
  );
}

export default BlogList;

```

In this example, the `BlogPageButton` component is used within a component that renders a list of blog posts. Ensure that you provide the appropriate data and state to the component to enable pagination functionality.

## License
This component is subject to its respective license. Ensure that you comply with the license terms when using this component.

Feel free to customize and extend the `BlogPageButton` component to suit your specific project requirements. Ensure that your component's state and data are correctly configured to enable pagination, and set up your component hierarchy accordingly to integrate it into your application. If you encounter any issues or have questions, please refer to your project's documentation or seek assistance from the development team.