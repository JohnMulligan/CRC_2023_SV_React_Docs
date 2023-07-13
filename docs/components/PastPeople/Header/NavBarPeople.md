# NavBarPeople Component
The `NavBarPeople` component is a navigation bar component that provides a menu and toolbar for navigating through different sections of a web application. It utilizes the Material-UI library for styling and icons.

## Usage
To use the `NavBarPeople` component, follow these steps:

- Import the necessary components and icons from the Material-UI library:

```jsx
import { MouseEventHandler, useState } from 'react';
import { AppBar, Box, IconButton, Hidden, Typography } from '@mui/material';
import MenuIcon from '@mui/icons-material/Menu';
import Toolbar from '@mui/material/Toolbar';
import { MenuListDropdownStyle } from '@/styleMUI';
import { Button, Menu } from '@mui/material';
import { useNavigate } from 'react-router-dom';
import { DrawerMenuPeopleBar } from './DrawerMenuPeopleBar';
import '@/style/Nav.scss';
import { POPELETILET } from '@/share/CONST_DATA';
```
- Define the `NavBarPeople` component:

```jsx
export default function NavBarPeople() {
  const navigate = useNavigate();
  const [anchorEl, setAnchorEl] = useState<null | HTMLElement>(null);

  const [anchorFilterMobileEl, setAnchorFilterMobileEl] =
    useState<null | HTMLElement>(null);

  const handleMenuFilterMobileClose = () => {
    setAnchorFilterMobileEl(null);
  };

  const handleMenuClose = () => {
    setAnchorEl(null);
  };

  const handleMenuOpen: MouseEventHandler<HTMLButtonElement> = (event) => {
    setAnchorEl(event.currentTarget);
  };

  const handleSelectMenuItems = (item: string) => {
    // Define the logic for navigating to the desired path based on the value of 'item'
    if (item === 'About') {
      navigate('/PastHomePage');
    } else if (item === 'Enslaved') {
      navigate('/PastHomePage/enslaved');
    } else if (item === 'Enslavers') {
      navigate('/PastHomePage/enslaver');
    } else {
      navigate('/');
    }
  };

  return (
    <Box
      sx={{
        display: 'flex',
      }}
    >
      <AppBar
        component="nav"
        style={{
          backgroundColor: '#ffffff',
          fontSize: 12,
          boxShadow: 'none',
          marginTop: '3rem',
        }}
      >
        <Toolbar sx={{ display: 'flex', alignItems: 'center' }}>
          <Hidden mdUp>
            <IconButton
              edge="start"
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
              flexGrow: 1,
              width: { xs: 200, sm: 220 },
              fontWeight: { sm: 600, md: 500 },
            }}
          >
            <div className="people-header">{POPELETILET}</div>
          </Typography>
          <Box
            className="menu-nav-bar-select-box"
            sx={{
              display: {
                xs: 'none',
                sm: 'none',
                md: 'block',
                lg: 'block',
                textAlign: 'center',
                paddingRight: 40,
                fontWeight: 600,
                fontSize: 20,
              },
            }}
          >
            {PEOPLE[0].header?.map((item, index) => {
              return (
                <Button
                  onClick={() => handleSelectMenuItems(item)}
                  key={`${item}-${index}`}
                  sx={{
                    color: '#000000',
                    fontWeight: 600,
                    fontSize: 20,
                    margin: '0 2px',
                    textTransform: 'none',
                    fontFamily: 'Cormorant Garamond',
                  }}
                >
                  <div>{item}</div>
                </Button>
              );
            })}
          </Box>
        </Toolbar>
        <Box component="nav">
          <Menu
            anchorEl={anchorEl}
            open={Boolean(anchorEl)}
            onClick={handleMenuClose}
          >
            <DrawerMenuPeopleBar
              value={PEOPLE[0]?.header}
              handleSelectMenuItems={handleSelectMenuItems}
            />
          </Menu>
        </Box>
      </AppBar>
    </Box>
  );
}
```

- Use the `NavBarPeople` component in your application:
```jsx
<NavBarPeople />
```

In the above example, the `NavBarPeople` component will be rendered in the application's layout or header section.

Feel free to customize the component's styling and functionality to fit your specific use case.