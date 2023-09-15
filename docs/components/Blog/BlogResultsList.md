# BlogResultsList

## Introduction
`BlogResultsList` is a React functional component responsible for displaying a list of blog posts based on data fetched from a Redux store. This component provides a paginated view of the blog posts, allows users to click on individual posts to view details, and includes features for searching and filtering blog posts. This README documentation explains the purpose of the component and provides guidance on how to use it within your React application.

## Installation
To use the `BlogResultsList` component, you need to ensure that your React project is set up correctly and that you have the required dependencies installed. Here are the steps to include this component in your project:

1) Import the necessary dependencies and components at the beginning of your file:
```jsx

import { useDispatch, useSelector } from 'react-redux';
import { Link } from 'react-router-dom';
import { useEffect, useState } from 'react';
import HeaderLogoSearch from '../header/HeaderSearchLogo';
import BlogPageButton from './PageButton';
import LOADINGLOGO from '@/assets/sv-logo_v2_notext.svg';
import NavBlog from './NavBarBlog';
import { fetchBlogData } from '@/fetchAPI/blogApi/fetchBlogData';
import { AppDispatch, RootState } from '@/redux/store';
import { setBlogData, setBlogPost } from '@/redux/getBlogDataSlice';
import {
  BlogDataProps,
  InitialStateBlogProps,
} from '@/share/InterfaceTypesBlog';
import { formatTextURL } from '@/utils/functions/formatText';
import { BASEURL } from '@/share/AUTH_BASEURL';
import '@/style/blogs.scss';
import { BLOGPAGE } from '@/share/CONST_DATA';


```

1) Create a functional component named BlogResultsList.
```jsx
const BlogResultsList: React.FC = () => {
  // ...
  // Component structure and logic go here
  // ...
};

```
1) Implement the component structure by arranging the imported components and adding any necessary JSX markup.

2) Return the JSX that represents the structure of the blog results list page.

3) Export the `BlogResultsList` component as the default export of your module.

## Usage
To use the `BlogResultsList` component in your React application, follow these steps:

1) Import the `BlogResultsList` component into the file where you want to display a list of blog posts.

```jsx
import BlogResultsList from './BlogResultsList'; // Adjust the import path as needed

```
1) Place the BlogResultsList component within your JSX to render the list of blog posts.
```jsx
<BlogResultsList />

```

1) Ensure that you have set up your Redux store correctly and that the required data, including blog post information, is available in the Redux state.

## Example
Here's an example of how to use the `BlogResultsList` component within a React application:

```jsx
import React from 'react';
import { Provider } from 'react-redux';
import { createStore } from 'redux';
import rootReducer from './reducers'; // Import your Redux root reducer
import BlogResultsList from './BlogResultsList'; // Adjust the import path as needed

const store = createStore(rootReducer); // Create your Redux store

function App() {
  return (
    <Provider store={store}>
      <div>
        {/* Other components and content */}
        <BlogResultsList />
        {/* Other components and content */}
      </div>
    </Provider>
  );
}

export default App;

```

In this example, the `BlogResultsList` component is used within a Redux Provider to make the Redux store available to the component. Ensure that your Redux store contains the necessary data, including the blog post information, in the appropriate state slices.

## License
This component and its dependencies are subject to their respective licenses. Ensure that you comply with the licenses of any third-party libraries you use.

Feel free to customize and extend the `BlogResultsList` component to suit your specific project requirements. Ensure that your Redux store is correctly configured to provide the required data, and set up your component hierarchy accordingly to integrate it into your application. If you encounter any issues or have questions, please refer to your project's documentation or seek assistance from the development team.