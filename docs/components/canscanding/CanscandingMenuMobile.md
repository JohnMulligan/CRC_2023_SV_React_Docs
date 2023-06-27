# CanscandingMenuMobile
CanscandingMenuMobile is a React functional component that provides a mobile menu with filter options. It allows users to select filter options and view the corresponding results.

## Dependencies
The component utilizes the following external dependencies:

- Material-UI: Provides UI components such as buttons, dialogs, and icons.
- react-redux: Enables integration with Redux for state management.


## Usage
To use the CanscandingMenuMobile component, follow these steps:

1) Import the necessary dependencies:
```jsx
import { ArrowLeft } from "@mui/icons-material";
import {
  Button,
  Dialog,
  DialogActions,
  DialogContent,
  DialogTitle,
  IconButton,
} from "@mui/material";
import FilterICON from "@/assets/filterICON.svg";
import {
  BLACK,
  DropdownMenuColumnItem,
  DropdownNestedMenuColumnItem,
  StyleDialog,
} from "@/styleMUI";
import {
  ChildrenFilter,
  FilterMenu,
  RangeSliderState,
  TYPES,
  VoyagaesFilterMenu,
  CurrentPageInitialState,
} from "@/share/InterfaceTypes";
import { useDispatch, useSelector } from "react-redux";
import { AppDispatch, RootState } from "@/redux/store";
import { DropdownColumn } from "../fcComponets/ColumnSelectorTable/DropdownColumn";
import { useState, MouseEvent } from "react";
import { setIsChange, setKeyValue } from "@/redux/rangeSliderSlice";
import { setIsOpenDialog } from "@/redux/getScrollPageSlice";
import { PaperDraggable } from "./PaperDraggable";
import AutocompleteBox from "../voyagePage/Results/AutocompletedBox";
import RangeSlider from "../voyagePage/Results/RangeSlider";
import { setIsChangeAuto } from "@/redux/getAutoCompleteSlice";
import { setIsFilter } from "@/redux/getFilterSlice";

```
2) Create an interface for the component props (if needed):
```jsx
interface CanscandingMenuMobileProps {}
```
3) 
Define the CanscandingMenuMobile component:
```jsx
const CanscandingMenuMobile: React.FC<CanscandingMenuMobileProps> = () => {
  // Component logic and state
};
```

4) Inside the component, utilize Redux's useSelector hook to access the required state from the Redux store:

```jsx
const menuOptionFlat: VoyagaesFilterMenu = useSelector(
  (state: RootState) => state.optionFlatMenu.value
);
const { currentPage } = useSelector(
  (state: RootState) => state.getScrollPage as CurrentPageInitialState
);
const { varName } = useSelector(
  (state: RootState) => state.rangeSlider as RangeSliderState
);
const { isOpenDialog } = useSelector(
  (state: RootState) => state.getScrollPage as CurrentPageInitialState
);
const { isFilter } = useSelector((state: RootState) => state.getFilter);
```

5) Export the CanscandingMenuMobile component as the default export:

```jsx
export default CanscandingMenuMobile;
```
## Summary
The CanscandingMenuMobile component provides a mobile menu with filter options. It uses Material-UI components, Redux for state management, and allows users to select filter options and view the corresponding results in a dialog.