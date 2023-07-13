# HeaderEnslavedNavBar Component

The `HeaderEnslavedNavBar` component is a React functional component that represents the navigation bar for the Enslaved dataset. It includes various dependencies, components, Redux state management, and event handlers.

## Dependencies
The component imports the following dependencies:

- `@mui/material`: Provides components such as AppBar, Box, IconButton, Hidden, Divider, Toolbar, Button, Menu, Typography.
- `@mui/icons-material`: Provides the MenuIcon.
- `react`, `react-redux`, `react-router-dom`: Dependencies for React, Redux, and routing.
- `@/styleMUI`, `@/share/InterfactTypesDatasetCollection`, `@/share/CONST_DATA`, `@/utils/functions/getColorStyle`, `@/assets/filterICON.svg`, `@/style/Nav.scss`: Custom dependencies specific to the project.
- `@/components/canscanding/CanscandingMenuMobile, @/components/canscanding/CanscandingMenu`: Custom components for a mobile menu.

## Usage
To use the HeaderEnslavedNavBar component, follow these steps:

- Import the necessary dependencies and components:

```jsx
import { MouseEventHandler, useState } from 'react';
import { AppBar, Box, IconButton, Hidden, Divider } from '@mui/material';
import MenuIcon from '@mui/icons-material/Menu';
import Toolbar from '@mui/material/Toolbar';
import { MenuListDropdownStyle } from '@/styleMUI';
import { Button, Menu, Typography } from '@mui/material';
import FilterICON from '@/assets/filterICON.svg';
import { AppDispatch, RootState } from '@/redux/store';
import { useDispatch, useSelector } from 'react-redux';
import { Link } from 'react-router-dom';
import '@/style/Nav.scss';
import { setIsFilter } from '@/redux/getFilterSlice';
import {
  getColorNavbarEnslavedBackground,
  getColorBoxShadowEnslaved,
  getColorBTNBackgroundEnslaved,
  getColorBTNHoverEnslavedBackground,
} from '@/utils/functions/getColorStyle';
import {
  BaseFilter,
  DataSetCollectionProps,
} from '@/share/InterfactTypesDatasetCollection';
import { ALLENSLAVED, EnslavedTitle } from '@/share/CONST_DATA';
import CanscandingMenuMobile from '@/components/canscanding/CanscandingMenuMobile';
import CanscandingMenu from '@/components/canscanding/CanscandingMenu';
import { DrawerMenuPeopleBar } from '../../Header/DrawerMenuPeopleBar';
import { ColumnSelector } from '@/components/FunctionComponents/ColumnSelectorTable/ColumnSelector';
import {
  setBaseFilterPeopleDataKey,
  setBaseFilterPeopleDataSetValue,
  setBaseFilterPeopleDataValue,
  setDataSetPeopleHeader,
  setPeopleBlocksMenuList,
  setPeopleFilterMenuFlatfile,
  setPeopleStyleName,
  setPeopleTableFlatfile,
  setPeopleTextIntro,
} from '@/redux/getPeopleDataSetCollectionSlice';
import { setPathName } from '@/redux/getDataSetCollectionSlice';

```

- Implement the `HeaderEnslavedNavBar` component:
```jsx
const HeaderEnslavedNavBar: React.FC = () => {
  // Redux state and dispatch
  const dispatch: AppDispatch = useDispatch();
  const { currentEnslavedPage } = useSelector(
    (state: RootState) => state.getScrollEnslavedPage
  );
  const { value, textHeader, styleNamePeople, tableFlatfile } = useSelector(
    (state: RootState) => state.getPeopleDataSetCollection
  );
  const { isFilter } = useSelector((state: RootState) => state.getFilter);
  const [anchorEl, setAnchorEl] = useState<null | HTMLElement>(null);
  const [anchorFilterMobileEl, setAnchorFilterMobileEl] =
    useState<null | HTMLElement>(null);

  // Event handlers
  const handleSelectEnslavedDataset = (
    base_filter: BaseFilter[],
    textHeder: string,
    textIntro: string,
    styleName: string,
    blocks: string[],
    filter_menu_flatfile: string,
    table_flatfile: string
  ) => {
    // ... implementation ...
  };

  const handleMenuFilterMobileClose = () => {
    // ... implementation ...
  };

  const handleMenuClose = () => {
    // ... implementation ...
  };

  const handleMenuOpen: MouseEventHandler<HTMLButtonElement> = (event) => {
    // ... implementation ...
  };

  // Render the component
  return (
    <Box
      sx={{
        display: 'flex',
      }}
    >
      <AppBar
        component="nav"
        style={{
          // ... app bar styles ...
        }}
      >
        <Toolbar sx={{ display: 'flex', alignItems: 'center' }}>
          <Hidden mdUp>
            <IconButton
              edge="start"
              color="inherit"
              aria-label="menu"
              onClick={handleMenuOpen}
              sx={{ mr: 2, display: { md: 'none' } }}
            >
              <MenuIcon />
            </IconButton>
          </Hidden>
          <Typography
            component="div"
            sx={{
              // ... typography styles ...
            }}
          >
            {/* ... header content ... */}
          </Typography>
          <CanscandingMenuMobile />
          <Box
            className="menu-nav-bar-select-box"
            sx={{
              // ... select box styles ...
            }}
          >
            <Box className="menu-nav-bar-select" style={{ color: '#000000' }}>
              Select dataset
            </Box>
            {value.map((item: DataSetCollectionProps, index: number) => {
              const {
                base_filter,
                headers,
                style_name,
                blocks,
                table_flatfile,
                filter_menu_flatfile,
              } = item;
              return (
                <Button
                  key={`${item}-${index}`}
                  onClick={() =>
                    handleSelectEnslavedDataset(
                      base_filter,
                      headers.label,
                      headers.text_introduce,
                      style_name,
                      blocks,
                      filter_menu_flatfile,
                      table_flatfile
                    )
                  }
                  sx={{
                    // ... button styles ...
                  }}
                >
                  <div>{headers.label}</div>
                </Button>
              );
            })}
          </Box>
        </Toolbar>
        <Hidden mdDown>
          {currentEnslavedPage !== 1 && isFilter && <CanscandingMenu />}
        </Hidden>
        <Box component="nav">
          <Menu
            anchorEl={anchorEl}
            open={Boolean(anchorEl)}
            onClick={handleMenuClose}
          >
            {/* ... menu content ... */}
          </Menu>
        </Box>
      </AppBar>
      <Menu
        anchorEl={anchorFilterMobileEl}
        open={Boolean(anchorFilterMobileEl)}
        onClick={handleMenuFilterMobileClose}
      >
        <MenuListDropdownStyle>
          <ColumnSelector />
        </MenuListDropdownStyle>
      </Menu>
    </Box>
  );
};

export default HeaderEnslavedNavBar;

```

The `HeaderEnslavedNavBar` component is a functional component that represents the navigation bar for the Enslaved dataset. It includes various components, Redux state management, and event handlers.

The component renders an `AppBar` from Material-UI as the navigation bar. It includes a `Toolbar` with a responsive menu icon (`MenuIcon`) for mobile devices. The navigation bar displays the dataset header, a filter button, and a dropdown menu for selecting the dataset.

The component uses `Redux` to manage the state of the dataset and filter. It dispatches actions to update the `Redux` store based on user interactions. The dropdown menu and filter button have event handlers to handle user actions and update the state accordingly.

By customizing the styles and behavior of the `HeaderEnslavedNavBar` component, you can create a navigation bar tailored to your application or website's specific needs.