# Header Navigation Bar Menu Component

This component represents the header navigation bar menu of the application. It provides a menu with navigation items, a filter search option, and a responsive mobile menu.

## Installation
No additional installation is required for this component.

## Usage
Import the necessary modules:

```jsx
import { MouseEventHandler, useState } from "react";
import {
  AppBar,
  Box,
  CssBaseline,
  List,
  IconButton,
  Hidden,
} from "@mui/material";
import ListItem from "@mui/material/ListItem";
import ListItemButton from "@mui/material/ListItemButton";
import ListItemText from "@mui/material/ListItemText";
import MenuIcon from "@mui/icons-material/Menu";
import Toolbar from "@mui/material/Toolbar";
import { StyleDiver } from "@/styleMUI";
import { Button, Menu, MenuItem, Typography } from "@mui/material";
import FilterICON from "@/assets/filterICON.svg";
import { RootState } from "@/redux/store";
import { HeaderNavBarMenuProps } from "@/share/InterfaceTypes";
import CanscandingMenu from "../canscanding/CanscandingMenu";
import { useSelector } from "react-redux";
import { currentPageInitialState } from "@/share/InterfaceTypes";
import "@/style/Nav.scss";
```

``HeaderNavBarMenu``

This component represents the header navigation bar menu.

```jsx
export default function HeaderNavBarMenu(props: HeaderNavBarMenuProps) {
  // Component logic goes here
}
```

## Props
- `currentPage`: The current page state from Redux store.
- `isFilter`: The filter state.
- `setIsFilter`: Function to set the filter state.

## Component Structure
The component structure includes an `AppBar` component from MUI, which contains the navigation menu, filter search option, and mobile menu. It also uses other MUI components such as `IconButton`, `Typography`, `Button`, and `Menu` for styling and functionality.

## Component Logic

The component logic includes the following:

- Accessing the `currentPage` and `isFilter` states from the Redux store using the `useSelector` hook.
- Managing the state of the mobile menu with the `anchorEl` and `setAnchorEl` hooks.
- Handling menu open and close events with the `handleMenuOpen` and `handleMenuClose` functions.
- Handling the selection of a menu item with the `handleSelectMenu` function.
- Rendering the navigation items, filter search option, and mobile menu using JSX.

## Example Usage
```jsx
import HeaderNavBarMenu from "./HeaderNavBarMenu";

function App() {
  return (
    <div>
      {/* Other components */}
      <HeaderNavBarMenu />
      {/* Other components */}
    </div>
  );
}

export default App;
```

![aggregation](../../assets/headNav.png)

That's it! You can now use the HeaderNavBarMenu component to display the header navigation bar menu in your application.