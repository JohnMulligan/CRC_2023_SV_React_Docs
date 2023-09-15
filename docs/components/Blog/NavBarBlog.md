# NavBarBlog 

## Introduction
`NavBarBlog` is a React functional component responsible for rendering the navigation bar for a blog page. This component includes features such as displaying the blog title, providing language selection options, and enabling global search functionality. This README documentation explains the purpose of the component and provides guidance on how to use it within your React application.

## Installation
To use the `NavBarBlog` component, you need to ensure that your React project is set up correctly and that you have the required dependencies installed. Here are the steps to include this component in your project:

1) Import the necessary dependencies and components at the beginning of your file:
```jsx
import { useSelector } from 'react-redux';
import { RootState } from '@/redux/store';
import '@/style/blogs.scss';
import { InitialStateBlogProps } from '@/share/InterfaceTypesBlog';
import { Link, useParams } from 'react-router-dom';
import { BLOGPAGE } from '@/share/CONST_DATA';
import LanguagesDropdown from '../FunctionComponents/LanguagesDropdown';
import AutoCompletedSearhBlog from './AutoCompletedSearhBlog';
import GlobalSearchButton from '../FunctionComponents/GlobalSearchButton';

```

1) Create a functional component named `NavBarBlog`.
```jsx
const NavBarBlog: React.FC = () => {
  // ...
  // Component structure and logic go here
  // ...
};

```

1) Implement the component structure by arranging the imported components and adding any necessary JSX markup.

2) Return the JSX that represents the navigation bar for the blog page.

3) Export the `NavBarBlog` component as the default export of your module.


## Usage
To use the `NavBarBlog` component in your React application, follow these steps:

1) Import the `NavBarBlog` component into the file where you want to display the navigation bar for your blog page.


```jsx
import NavBarBlog from './NavBarBlog'; // Adjust the import path as needed

```

1) Place the `NavBarBlog` component within your JSX to render the navigation bar.
```jsx
<NavBarBlog />

```

1) Ensure that you have set up your Redux store correctly and that the required data, including the blog post information and search input value, is available in the Redux state.


## Example
Here's an example of how to use the NavBarBlog component within a React application:

```jsx
import HeaderLogoSearch from '../header/HeaderSearchLogo';
import NavBlog from './NavBarBlog'; // Add  <NavBlog /> into the BlogDetailsPost component
import BlogCardHeaderBody from './BlogCardHeaderBody';
import '@/style/blogs.scss';
import { Divider } from '@mui/material';
import BlogCardContent from './BlogCardContent';

const BlogDetailsPost: React.FC = () => {
  return (
    <>
      <HeaderLogoSearch />
      <NavBlog />
      <div className="container-new">
        <div className="row-next">
          <div className="card-content">
            <BlogCardHeaderBody />
            <Divider />
            <BlogCardContent />
          </div>
        </div>
      </div>
    </>
  );
};
export default BlogDetailsPost;


```

In this example, the `NavBarBlog` component is used within a Redux Provider to make the Redux store available to the component. Ensure that your Redux store contains the necessary data, including the blog post information and search input value, in the appropriate state slices.

## License
This component and its dependencies are subject to their respective licenses. Ensure that you comply with the licenses of any third-party libraries you use.

Feel free to customize and extend the `NavBarBlog` component to suit your specific project requirements. Ensure that your Redux store is correctly configured to provide the required data, and set up your component hierarchy accordingly to integrate it into your application. If you encounter any issues or have questions, please refer to your project's documentation or seek assistance from the development team.