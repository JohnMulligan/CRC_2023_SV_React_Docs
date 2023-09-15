# BlogCardHeaderBody ReadMe

## Introduction
`BlogCardHeaderBody` is a React component that is designed to display detailed information about a blog post, such as its title, subtitle, authors, publication date, tags, and social media sharing options. This component is typically used within a blog post detail page to provide readers with additional context and options for sharing the content.

## Installation
To use the `BlogCardHeaderBody` component, you need to ensure that your React project is set up correctly and that you have the required dependencies installed. Here are the steps to include this component in your project:

1) Import the necessary dependencies at the beginning of your file:
```jsx
import { fetchBlogData } from '@/fetchAPI/blogApi/fetchBlogData';
import { setBlogPost } from '@/redux/getBlogDataSlice';
import { AppDispatch, RootState } from '@/redux/store';
import { InitialStateBlogProps } from '@/share/InterfaceTypesBlog';
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
import {
  faWhatsapp,
  faSquareFacebook,
  faTwitterSquare,
  faLinkedin,
} 


from '@fortawesome/free-brands-svg-icons';
import { faSquareEnvelope } from '@fortawesome/free-solid-svg-icons';
import { useEffect } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { Link, useParams } from 'react-router-dom';
import { BASEURL } from '@/share/AUTH_BASEURL';
import { BLOGPAGE } from '@/share/CONST_DATA';
import { convertToSlug } from '@/utils/functions/convertToSlug';
```
1) Create a functional component named BlogCardHeaderBody.

```jsx
const BlogCardHeaderBody = () => {
  // ...
  // Component logic goes here
  // ...
};
```

1) Implement the logic for fetching blog post data, formatting dates, and rendering the blog post details.

2) Return the JSX that represents the blog post details.

3) Export the `BlogCardHeaderBody` component as the default export of your module.

## Usage
To use the `BlogCardHeaderBody` component in your React application, follow these steps:

1) Import the `BlogCardHeaderBody` component into the file where you want to display a detailed blog post.

```jsx 
import BlogCardHeaderBody from './BlogCardHeaderBody'; // Adjust the import path as needed
```
1) Use the `BlogCardHeaderBody` component within your JSX to display the blog post details.

```jsx 
<BlogCardHeaderBody />
```

1) Ensure that you have the necessary Redux store, router, and API endpoints set up to provide data to this component. You should also have FontAwesome icons available for social media sharing.


## Example
Here's an example of how to use the `BlogCardHeaderBody` component within a React application:

```jsx
import React from 'react';
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';
import BlogCardHeaderBody from './BlogCardHeaderBody'; // Adjust the import path as needed

function App() {
  return (
    <Router>
      <div>
        <Switch>
          <Route path="/blog/:ID">
            <BlogCardHeaderBody />
            {/* Add additional components and routes as needed */}
          </Route>
          {/* Add other routes as needed */}
        </Switch>
      </div>
    </Router>
  );
}
export default App;
```


In this example, the `BlogCardHeaderBody` component is used within a route that matches a blog post's ID in the URL. You should adapt this example to fit your application's routing structure and data fetching mechanisms.

## License
This component and its dependencies are subject to their respective licenses. Ensure that you comply with the licenses of any third-party libraries you use.

Feel free to customize and extend the `BlogCardHeaderBody` component to suit your specific project requirements. Make sure to configure your Redux store, API endpoints, and routing to provide the necessary data to this component for it to function correctly. If you encounter any issues or have questions, please refer to your project's documentation or seek assistance from the development team.