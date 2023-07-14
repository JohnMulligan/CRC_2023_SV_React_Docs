# VoyagesPage

This is a React functional component named `VoyagesPage` that represents a page for displaying voyages. It includes a header, navigation bar, and a scrolling content section.

## Dependencies
This code has the following dependencies:

- `React` library: This code uses React to define and render the component.
- `react-redux`: This code uses Redux for managing the application state.

## Usage
To use this component, follow these steps:

1) Make sure you have the required dependencies installed.
2) Import the necessary components and styles:
- `HeaderLogoSearch` from the `../components/header/HeaderSearchLogo` module.
- `HeaderNavBar` from the `../components/header/HeaderNavBar` module.
- `ScrollPage` from the `@/components/Voyages/ScrollPage` module.
- Styles from the `@/style/page.scss file`.
3) Use the `VoyagesPage` component in your application by rendering it as part of your page structure.
4) Customize the imported components and styles or add additional components as needed.

## Example

```jsx
import React from 'react';
import HeaderLogoSearch from '../components/header/HeaderSearchLogo';
import HeaderNavBar from '../components/header/HeaderNavBar';
import ScrollPage from '@/components/Voyages/ScrollPage';
import '@/style/page.scss';
import { useSelector } from 'react-redux';
import { RootState } from '@/redux/store';
import { getColorVoyagePageBackground } from '@/utils/functions/getColorStyle';
import { CurrentPageInitialState } from '@/share/InterfaceTypes';

const MyVoyagesPage: React.FC = () => {
  const { styleName } = useSelector(
    (state: RootState) => state.getDataSetCollection
  );
  const { currentPage } = useSelector(
    (state: RootState) => state.getScrollPage as CurrentPageInitialState
  );
  return (
    <div
      className="voyages-home-page"
      style={{
        backgroundColor: getColorVoyagePageBackground(styleName, currentPage),
      }}
    >
      {/* Render the HeaderLogoSearch component */}
      <HeaderLogoSearch />

      {/* Render the HeaderNavBar component */}
      <HeaderNavBar />

      {/* Render the ScrollPage component */}
      <ScrollPage />
    </div>
  );
};

export default MyVoyagesPage;

```
In the above example, the `VoyagesPage` component is used within a parent component named `MyVoyagesPage`. The imported components and styles are rendered within the `MyVoyagesPage` component, providing the necessary structure for the voyages page.

Please note that this code assumes the presence of specific module paths `(../components/..., @/components/..., @/style/page.scss, @/redux/..., @/utils/..., @/share/...)`. Ensure that these paths are correctly configured in your project before using this code.
