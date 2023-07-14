# HomePage
This is a React functional component named `HomePage` that represents the home page for a project related to voyages and enslaved people. It provides a layout with various sections and functionality for searching, navigating, and accessing resources.

## Dependencies
This code has the following dependencies:

- `React library:` This code uses React to define and render the component.
- `react-router-dom:` This code uses React Router for handling navigation and linking to different routes.
- `react-redux:` This code uses Redux for managing the application state.

## Usage
To use this component, follow these steps:

1) Make sure you have the required dependencies installed.
2) Import the necessary components, assets, and styles:
- `SearchIcon` from the `@mui/icons-material/Search` module.
- `MenuButtonHomePage` from the `@/components/Home/Menu` module.
- `Link` from the `react-router-dom`module.
- `Search`, `SearchIconWrapper`, and `StyledInputBase` from the `@/styleMUI` module.
- Assets from various paths `(@/assets/...)`.
- Styles from the `@/style/homepage.scss` file.
3) Use the `HomePage` component in your application by rendering it as part of your page structure.
4) Customize the imported components, assets, and styles or add additional components and functionality as needed.

## Example
```jsx
import React from 'react';
import voyageLogo from '@/assets/logo-voyage.svg';
import voyageText from '@/assets/slave-text.svg';
import SearchIcon from '@mui/icons-material/Search';
import voyageIcon from '@/assets/voyage-cycle.svg';
import peopleIcon from '@/assets/people-cycle.svg';
import documentIcon from '@/assets/documents.svg';
import resourceIcon from '@/assets/resources.svg';
import { Search, SearchIconWrapper, StyledInputBase } from '@/styleMUI';
import MenuButtonHomePage from '@/components/Home/Menu';
import { Link } from 'react-router-dom';
import '@/style/homepage.scss';
import { AppDispatch } from '@/redux/store';
import { useDispatch } from 'react-redux';
import { ALLENSLAVED, ALLVOYAGES } from '@/share/CONST_DATA';
import { setPathName } from '@/redux/getDataSetCollectionSlice';

const MyHomePage: React.FC = () => {
  const dispatch: AppDispatch = useDispatch();

  return (
    <div>
      {/* Render the MenuButtonHomePage component */}
      <MenuButtonHomePage />

      <div className="home-voyagepage-content">
        {/* Header section */}
        <div className="header-logo-slave-voyages">
          {/* Render the voyageLogo image */}
          <div className="voyageLogo-img">
            <img src={voyageLogo} alt="voyageLogo" />
          </div>

          <div className="voyage-text-box">
            {/* Render the voyageText image */}
            <div>
              <img src={voyageText} alt="voyageText" />
            </div>

            <div className="voyage-description">
              Explore the origins and forced relocations of more than 12 million
              Enslaved Africans across the world
            </div>
          </div>
        </div>

        {/* Search box */}
        <div className="voyages-search-box">
          <Search className="voyages-search-box-content">
            <SearchIconWrapper>
              {/* Render the SearchIcon */}
              <SearchIcon />
            </SearchIconWrapper>
            <StyledInputBase
              placeholder=""
              inputProps={{ 'aria-label': 'search' }}
            />
          </Search>
        </div>

        {/* Voyages, People, Places section */}
        <div className="voyages-people-places">
          {/* Voyages */}
          <div className="voyage-page-box">
            <div className="voyages-people-places-title">Voyages</div>
            {/* Link to the VoyagesPage and dispatch an action */}
            <Link
              to="/VoyagesPage"
              onClick={() => dispatch(setPathName(ALLVOYAGES))}
            >
              {/* Render the voyageIcon */}
              <img src={voyageIcon} alt="voyages" />
            </Link>
            <div className="voyages-people-places-subtitle">
              Search by vessel
            </div>
          </div>

          {/* People */}
          <div className="people-page-box">
            <div className="voyages-people-places-title">People</div>
            {/* Link to the PastHomePage and dispatch an action */}
            <Link
              to="/PastHomePage"
              onClick={() => dispatch(setPathName(ALLENSLAVED))}
            >
              {/* Render the peopleIcon */}
              <img src={peopleIcon} alt="voyages" />
            </Link>
            <div className="voyages-people-places-subtitle">Find a person</div>
          </div>

          {/* Documents */}
          <div className="place-page-box">
            <div className="voyages-people-places-title">Documents</div>
            <Link to="#">
              {/* Render the documentIcon */}
              <img src={documentIcon} alt="voyages" width={129} />
            </Link>
            <div className="voyages-people-places-subtitle">
              Read Primary Sources
            </div>
          </div>

          {/* Writing */}
          <div className="place-page-box">
            <div className="voyages-people-places-title">Writing</div>
            <Link to="#">
              {/* Render the resourceIcon */}
              <img src={resourceIcon} alt="voyages" width={129} />
            </Link>
            <div className="voyages-people-places-subtitle">
              Lesson Plans, Essays, and More
            </div>
          </div>
        </div>

        {/* Document and Resources section */}
        <div className="document-resources-container">
          <div className="about-project">
            <div className="about-project-btn">About the Project</div>
          </div>
        </div>
      </div>
    </div>
  );
};

export default MyHomePage;

```

In the above example, the `HomePage` component is used within a parent component named `MyHomePage`. The imported components, assets, and styles are rendered within the `MyHomePage` component, providing the necessary structure and functionality for the project's home page.

Please note that this code assumes the presence of specific module paths `(@/components/...`, `@/assets/...`, `@/styleMUI`, `@/redux/...`, `@/share/..`.) and a specific style file `(@/style/homepage.scss)`. Ensure that these paths are correctly configured in your project before using this code.