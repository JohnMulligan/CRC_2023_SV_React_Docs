# EnslavedHomePage

This is a React component named `EnslavedHomePage` that represents the home page for a project related to past people who were enslaved. It provides a basic structure for rendering the page with a header, navigation bar, and a scrolling content section.

## Dependencies
This code has the following dependencies:

- `React` library: This code uses React to define and render the component.


## Usage
To use this component, follow these steps:

1) Make sure you have the required dependencies installed.
2) Import the necessary components:
- `EnslavedPageScrolling` from the `@/components/PastPeople/Enslaved/EnslavedPageScrolling` module.
- `HeaderEnslavedNavBar` from the `@/components/PastPeople/Enslaved/HeaderEnslaved/HeaderEnslavedNavBar` module.
- `HeaderLogoSearch` from the `@/components/header/HeaderSearchLogo` module.
3) Use the `EnslavedHomePage` component in your application by rendering it as part of your page structure.
4) Customize the imported components or add additional components as needed.

## Example
```jsx
import EnslavedPageScrolling from '@/components/PastPeople/Enslaved/EnslavedPageScrolling';
import HeaderEnslavedNavBar from '@/components/PastPeople/Enslaved/HeaderEnslaved/HeaderEnslavedNavBar';
import HeaderLogoSearch from '@/components/header/HeaderSearchLogo';
import React from 'react';
import '@/style/page-past.scss';

const EnslaversHomePage: React.FC = () => {
  return (
   <div id="enslaved-home-page">
      <HeaderLogoSearch />
      <HeaderEnslavedNavBar />
      <EnslavedPageScrolling />
    </div>
  );
};

export default EnslaversHomePage;
```

In the above example, the `EnslavedHomePage` component is used within a parent component named `EnslavedHomePage`. 
The imported components are rendered within the `EnslavedHomePage` component, providing the necessary structure for the enslaved people project home page.

Please note that this code assumes the presence of specific module paths `(@/components/...)` and a specific style file `(@/style/page-past.scss)`. Ensure that these paths are correctly configured in your project before using this code.