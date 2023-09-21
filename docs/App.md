# Documentation for the React Application
This documentation provides an overview of the structure and routing configuration of a React application. The application is organized into pages, and it uses React Router for navigation. Additionally, it utilizes the `react-query` library for managing data fetching.

## Application Overview
The React application consists of the following key components:

1) `Routing:` The application uses the `react-router-dom` library for client-side routing. Different routes are mapped to specific pages or components.

2) `ThemeProvider:` The application uses the Material-UI `ThemeProvider` to provide a custom theme (defined in `theme.ts`) for styling components.

3) `QueryClientProvider:` The application uses `react-query` and provides a `QueryClient` to manage data fetching, caching, and state.

4) `Pages`: Each page or major section of the application is represented by a separate component.

5) `Routes:` Routes are defined using the `<Route>` component from `react-router-dom`, specifying the path and the component to render for each route.

## Application Structure
### `App` Component
The `App` component serves as the entry point of the application. It sets up the theme, initializes the `QueryClient`, and defines the application's routes using the `<Routes>` component from `react-router-dom.` It also provides routes to various pages based on the defined paths.

## Pages Components
The application includes several page components, each representing a different section of the application. These page components include:

- `HomePage:` Represents the home page.
- `VoyagesPage:` Represents a page related to voyages data.
- `PastHomePage:` Represents the home page for past data.
- `EnslavedHomePage:` Represents a page related to enslaved individuals.
- `EnslaversHomePage:` Represents a page related to enslavers.
- `DocumentPage:` Represents a page for documents.
- `Blog:` Represents a page for blog posts.
- `BlogDetailsPost:` Represents a page for displaying details of a blog post.
- `AuthorPage:` Represents a page for displaying author information.
- `InstitutionAuthorsPage:` Represents a page for displaying institution authors.


## Routes Configuration
The routes are configured using the `<Route>` component from `react-router-dom.` Each route specifies a path attribute that maps to a URL `path`, and an `element` attribute that defines the component to be rendered for that route.

## Example Usage
```jsx
<Route path="/" element={<HomePage />} />
<Route path={`${VOYAGESPAGE}`} element={<VoyagesPage />} />
<Route path={`${VOYAGESPAGE}${ALLVOYAGESPAGE}`} element={<VoyagesPage />} />
// Additional routes...
```

In the example above, routes are defined for the home page, voyages pages, and other related pages. The `element` attribute specifies which component to render when the corresponding path is matched.

## Conclusion
This documentation provides an overview of the structure and routing configuration of the React application. The application follows best practices for organizing routes and components, making it easy to navigate and maintain.