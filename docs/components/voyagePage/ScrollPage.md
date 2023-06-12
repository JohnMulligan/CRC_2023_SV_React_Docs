# Scroll Page Component

This component represents the scrollable pages in the application.

## Installation
No additional installation is required for this component.

## Usage
Import the necessary modules:
```jsx
import { useEffect, FunctionComponent } from "react";
import { Grid, Hidden } from "@mui/material";
import { useTheme } from "@mui/material/styles";
import useMediaQuery from "@mui/material/useMediaQuery";
import { motion } from "framer-motion";
import { useDispatch, useSelector } from "react-redux";
import { setCurrentPage, setIsOpenDialog } from "@/redux/getScrollPageSlice";
import { AppDispatch, RootState } from "@/redux/store";
import { currentPageInitialState } from "@/share/InterfaceTypes";
import { ButtonNav } from "@/styleMUI";
import VoyagesPage from "./VoyagePage";
import "@/style/page.scss";
import Scatter from "./Results/Scatter";
import BarGraph from "./Results/BarGraph";
```

`ScrollPage`
This component represents the scrollable pages.
```jsx 
interface ScrollPageProps {
  isFilter: boolean;
  setIsFilter: React.Dispatch<React.SetStateAction<boolean>>;
}

const ScrollPage: FunctionComponent<ScrollPageProps> = ({
  isFilter,
  setIsFilter,
}) => {
  // Component logic goes here

  // Scroll to next page and page hide other page
  useEffect(() => {
    const handleScroll = (event: WheelEvent) => {
      const { deltaY } = event;
      const nextPage = deltaY > 0 ? currentPage + 1 : currentPage - 1;

      setTimeout(() => {
        if (nextPage >= 1 && nextPage <= totalPageCount) {
          dispatch(setCurrentPage(nextPage));
          smoothScrollToTop();
          dispatch(setIsOpenDialog(false));
        }
        setIsFilter(false);
        dispatch(setIsOpenDialog(false));
      }, 400);
    };
    window.addEventListener("wheel", handleScroll);
    return () => {
      window.removeEventListener("wheel", handleScroll);
    };
  }, [currentPage, isOpenDialog]);
};
```

## Component Structure
The component structure includes various MUI components, such as Grid and Hidden, to handle the layout and responsiveness of the pages. It also uses Redux for state management.

## Component Logic
The component logic includes handling scrolling between pages, setting the current page, and displaying the appropriate content based on the current page.

## Example Usage
```jsx
import ScrollPage from "./ScrollPage";

function HOME() {
  return (
    <div>
      {/* Other components */}
      <ScrollPage isFilter={true} setIsFilter={setIsFilter} />
      {/* Other components */}
    </div>
  );
}

export default App;
```

That's it! You can now use the ScrollPage component to create scrollable pages in your application.




