## BlogCardContent

## Introduction
`BlogCardContent` is a React component designed for rendering the content of a blog post. It utilizes the `html-react-parser `library to parse HTML content stored within your Redux state and render it as a React component. This component is typically used to display the main body content of a blog post on a blog detail page.

## Installation
To use the `BlogCardContent` component, you need to ensure that your React project is set up correctly and that you have the required dependencies installed. Here are the steps to include this component in your project:

1) Import the necessary dependencies at the beginning of your file:

```jsx
import ReactHtmlParser from 'html-react-parser';
import { RootState } from '@/redux/store';
import { BlogDataProps } from '@/share/InterfaceTypesBlog';
import { useSelector } from 'react-redux';

```
1) Create a functional component named BlogCardContent.

```jsx
const BlogCardContent = () => {
  // ...
  // Component logic goes here
  // ...
};

```

1) Implement the logic for fetching the blog post content from your Redux state.

2) Use the `ReactHtmlParser` function to parse and render the HTML content within your component.

3) Return the JSX that represents the rendered blog post content.

4) Export the `BlogCardContent` component as the default export of your module.

## Usage
To use the `BlogCardContent` component in your React application, follow these steps:

1) Import the `BlogCardContent` component into the file where you want to display the blog post content.

```jsx
import BlogCardContent from './BlogCardContent'; // Adjust the import path as needed

```
1) Place the `BlogCardContent` component within your JSX to render the blog post content.
```jsx
<BlogCardContent />

```

1)Ensure that you have set up your Redux store correctly and that the required data, including the blog post content, is available in the Redux state.


## Example
Here's an example of how to use the `BlogCardContent` component within a React application:

```jsx

import React from 'react';
import { Provider } from 'react-redux';
import { createStore } from 'redux';
import rootReducer from './reducers'; // Import your Redux root reducer
import BlogCardContent from './BlogCardContent'; // Adjust the import path as needed

const store = createStore(rootReducer); // Create your Redux store

function App() {
  return (
    <Provider store={store}>
      <div>
        {/* Other components and content */}
        <BlogCardContent />
        {/* Other components and content */}
      </div>
    </Provider>
  );
}

export default App;
```

In this example, the `BlogCardContent` component is used within a Redux Provider to make the Redux store available to the component. Ensure that your Redux store contains the necessary data, including the `content` property, in the appropriate state slice.

## License
This component and its dependencies are subject to their respective licenses. Ensure that you comply with the licenses of any third-party libraries you use.

Feel free to customize and extend the `BlogCardContent` component to suit your specific project requirements. Ensure that your Redux store is correctly configured to provide the required data, and set up your component hierarchy accordingly to integrate it into your application. If you encounter any issues or have questions, please refer to your project's documentation or seek assistance from the development team.

