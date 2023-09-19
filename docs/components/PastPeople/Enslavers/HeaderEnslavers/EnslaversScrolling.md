# EnslaversScrolling Component

The `EnslaversScrolling` component is a React functional component that represents a scrolling page for the Enslaved dataset. It includes various dependencies, Redux state management, and event handlers.

## Dependencies

- `@mui/material`: Provides components such as `Grid` and `Hidden` for layout purposes.
- `@mui/material/styles`: Provides the `useTheme` hook for accessing the current theme.
- `@mui/material/useMediaQuery`: Provides the `useMediaQuery` hook for handling media queries.
- `framer-motion`: Provides motion-related features for animations.
- `react-redux`: Provides the useDispatch and useSelector hooks for Redux state management.
- `@/redux/getScrollEnslavedPageSlice`: Imports Redux actions for setting the current page of the Enslaved dataset scrolling page.
- `@/redux/store`: Imports the Redux store and provides the - `AppDispatch` and `RootState` types.
- `@/styleMUI`: Imports custom Material-UI styles for buttons.
- `@/utils/functions/getColorStyle`: Imports utility functions for getting color styles.
- `./EnslavedPage`: Imports the `EnslavedPage` component.
- `./EnslavedTable`: Imports the `EnslavedTable` component.
- `@/style/page.scss`: Custom styles specific to the page.

## Usage
To use the `EnslaversScrolling` component, follow these steps:

- Import the necessary dependencies and components:
```jsx
import { Grid, Hidden } from '@mui/material';
import { useTheme } from '@mui/material/styles';
import useMediaQuery from '@mui/material/useMediaQuery';
import { motion } from 'framer-motion';
import { useDispatch, useSelector } from 'react-redux';
import { setCurrentEnslavedPage } from '@/redux/getScrollEnslavedPageSlice';
import { AppDispatch, RootState } from '@/redux/store';
import { ButtonNav } from '@/styleMUI';
import {
  getColorBTNBackgroundEnslaved,
  getColorBoxShadowEnslaved,
} from '@/utils/functions/getColorStyle';
import EnslavedPage from './EnslavedPage';
import EnslavedTable from './EnslavedTable';
import '@/style/page.scss';

```
- Implement the `EnslaversScrolling` component:
```jsx
const EnslaversScrolling = () => {
  // Redux state and dispatch
  const dispatch: AppDispatch = useDispatch();
  const theme = useTheme();
  const { isFilter } = useSelector((state: RootState) => state.getFilter);
  const { styleNamePeople, blocksPeople } = useSelector(
    (state: RootState) => state.getPeopleDataSetCollection
  );
  const { currentEnslavedPage } = useSelector(
    (state: RootState) => state.getScrollEnslavedPage
  );
  const newBlock = [...blocksPeople].reverse();
  const isSmallScreen = useMediaQuery(theme.breakpoints.up('lg'));
  const totalPageCount = newBlock?.length;

  // Event handler
  const handlePageNavigation = (page: number) => {
    dispatch(setCurrentEnslavedPage(page));
  };
  
  // Display the page content
  const displayPage = (
    <motion.div
      initial={'initial'}
      animate={'animate'}
      variants={
        currentEnslavedPage - 1 > -1
          ? pageVariantsFromTop
          : pageVariantsFromBottom
      }
      transition={{ duration: 0.5, ease: 'easeOut' }}
    >
      {currentEnslavedPage === 1 && <EnslavedPage />}
      {currentEnslavedPage === 2 && <EnslavedTable />}
    </motion.div>
  );

  // Render the component
  return (
    <div
      style={{
        position: 'relative',
        top: !isSmallScreen
          ? 130
          : currentEnslavedPage !== 1 && isFilter
          ? 230
          : 170,
        padding: currentEnslavedPage !== 1 ? '0 20px' : '',
      }}
      id="content-container"
    >
      <Hidden>
        <div className="navbar-wrapper">
          <nav className="nav-button-enslaved">
            {newBlock.map((page, index) => {
              const buttonIndex = totalPageCount - index;
              return (
                <ButtonNav
                  key={`${page}-${buttonIndex}`}
                  onClick={() => handlePageNavigation(buttonIndex)}
                  style={{
                    width: '80px',
                    height: '32',
                    backgroundColor:
                      getColorBTNBackgroundEnslaved(styleNamePeople),
                    boxShadow: getColorBoxShadowEnslaved(styleNamePeople),
                    fontSize: currentEnslavedPage === buttonIndex ? 15 : 14,
                    color:
                      currentEnslavedPage === buttonIndex ? 'white' : 'black',
                    fontWeight: currentEnslavedPage === buttonIndex ? 900 : 600,
                  }}
                  variant={
                    currentEnslavedPage === buttonIndex
                      ? 'contained'
                      : 'outlined'
                  }
                >
                  {page.toUpperCase()}
                </ButtonNav>
              );
            })}
          </nav>
        </div>
      </Hidden>
      <Grid id="content-container">{displayPage}</Grid>
    </div>
  );
};

export default EnslaversScrolling;


```

The `EnslaversScrolling` component is a functional component that represents a scrolling page for the Enslaved dataset. It includes various components, Redux state management, and event handlers.

The component renders the page content based on the currentEnslavedPage state. It includes a navigation bar with buttons for navigating between different sections of the page. The page content is displayed using the `motion.div` component from Framer Motion, allowing for animated transitions between sections. The component also adjusts the positioning and padding based on the screen size and currentEnslavedPage state.

By customizing the content and styles of the `EnslaversScrolling` component, you can create a scrolling page tailored to display information about the Enslaved dataset in your application or website.