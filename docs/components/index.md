# Components Structure

The Components folder within your React application is a crucial part of organizing and managing the user interface. It contains reusable and modular components that make up various parts of your application. This documentation outlines the recommended folder structure for organizing components effectively.

## Folder Hierarchy
A well-organized Components folder structure can improve code maintainability, readability, and collaboration among team members. Here's a suggested hierarchy for your Components folder:

```jsx
  │   ├── components
  │   │     ├── Blog
  │   │     │     ├── AuthorPage
  │   │     │     │      ├── AuthorInfo
  │   │     │     │      ├── AuthorPostList
  │   │     │     ├── InstitutionsAuthors
  │   │     │     │      ├── InstitutionAuthors
  │   │     │     │      ├── InstitutionAuthorsList
  │   │     │     ├── AutoCompletedSearhBlog
  │   │     │     ├── BlogCardContent
  │   │     │     ├── BlogCardHeaderBody
  │   │     │     ├── BlogDetailsPost
  │   │     │     ├── BlogResultsList
  │   │     │     ├── NavBarBlog
  │   │     │     ├── PageButton
  │   │     │     ├── SelectBlogDropdown
  │   │     ├── canscanding
  │   │     │     ├── CanscandingMenu
  │   │     │     ├── CanscandingMenuEnslavedMobile
  │   │     │     ├── CanscandingMenuEnslaversMobile
  │   │     │     ├── CanscandingMenuVoyagesMobile
  │   │     │     ├── Dropdown
  │   │     │     ├── MenuListDropdown
  │   │     │     ├── MenuListDropdownPeople.tsx
  │   │     │     ├── NestedMenuItem
  │   │     │     ├── PaperDraggable
  │   │     ├── FunctionComponents
  │   │     │     ├──  Cards
  │   │     │     │      ├── CardModal
  │   │     │     │      ├── Cards
  │   │     │     ├──  ColumnSelectorTable
  │   │     │     │      ├── ButtonDropdownSelectoreColumn
  │   │     │     │      ├── ColumnSelector
  │   │     │     │      ├── DropdownColumn
  │   │     │     │      ├── NestedMenuColumnItem
  │   │     │     ├──  GeoTreeSelect
  │   │     │     │      ├── GeoTreeSelected
  │   │     │     │      ├── ModalGeoTreeSelected
  │   │     │     ├──  Map
  │   │     │     │      ├── CurvedPolyLine
  │   │     │     │      ├── LeafletMap
  │   │     │     │      ├── MAPS
  │   │     │     │      ├── MyLineComponent
  │   │     │     │      ├── NodeCurvedLinesMap
  │   │     │     │      ├── NodeMarkerMap
  │   │     │     │      ├── PolylineMap
  │   │     │     │      ├── renderAnimatedLines
  │   │     │     │      ├── renderPolylineMap
  │   │     │     │      ├── renderPolylineNodeMap
  │   │     │     ├──  Map
  │   │     │     │      ├── drawNetwork
  │   │     │     │      ├── findHoveredEdge
  │   │     │     │      ├── findNode
  │   │     │     │      ├── ModalNetworksGraph
  │   │     │     │      ├── NetworkDiagram
  │   │     │     │      ├── NetworkDiagramSlaveVoyages
  │   │     │     │      ├── ShowsAcoloredNodeKey
  │   │     │     ├──  PivotTables
  │   │     │     │      ├── PivotTables
  │   │     │     │      ├── SelectDropdownPivotable
  │   │     │     ├── AutocompletedBox
  │   │     │     ├── CustomHeader
  │   │     │     ├── DatasetButton
  │   │     │     ├── FilterButton
  │   │     │     ├── GenerateCellTableRenderer
  │   │     │     ├── GlobalSearchButton
  │   │     │     ├── HeaderTitle
  │   │     │     ├── LanguagesDropdown
  │   │     │     ├── RangeSlider
  │   │     │── header
  │   │     │     ├── drawerMenuBar
  │   │     │     ├── HeaderNavar
  │   │     │     ├── HeaderSearchLogo
  │   │     │── Home
  │   │     │     ├── stylesMenu
  │   │     │     │      ├── StyledBurger
  │   │     │     │      ├── SytledMenu
  │   │     │     ├── AutoGlobalSearchBar
  │   │     │     ├── BurgerMenu
  │   │     │     ├── HomeSearch
  │   │     │     ├── Menu
  │   │     │     ├── MenuDropdownProps
  │   │     │     ├── SlaveVoyageLogo
  │   │     │     ├── VideoBackground
  │   │     │── PastPeople
  │   │     │     ├── Enslaved
  │   │     │     │      ├── ColumnSelectorEnslavedTable
  |   │     │     │      │      ├── ButtonDropdownSelectorEnslaved
  │   │     │     │      ├── HeaderEnslaved
  |   │     │     │      │      ├── HeaderEnslavedNavBar
  │   │     │     |      ├── EnslavedPage
  │   │     │     |      ├── EnslavedPageScrolling
  │   │     │     |      ├── EnslavedTable
  │   │     │     ├── Enslaved
  │   │     │     │      ├── ColumnSelectorEnslaversTable
  |   │     │     │      │      ├── ButtonDropdownSelectorEnslavers
  │   │     │     │      ├── HeaderEnslavers
  |   │     │     │      │      ├── HeaderEnslaversNavBar
  │   │     │     |      ├── EnslaversPage
  │   │     │     |      ├── EnslaversPageScrolling
  │   │     │     |      ├── EnslaversTable
  │   │     │     ├── Header
  │   │     │     │      ├── DrawerMenuPeopleBar
  |   │     │     │      ├── NavBarPeople
  │   │     │     ├── PastPeoplePage
  │   │     │── voyagePage
  │   │     │     ├── Results
  │   │     │     │      ├── AggregationSumAverage
  │   │     │     │      ├── BarGraph
  │   │     │     │      ├── PieGraph
  │   │     │     │      ├── Scatter
  │   │     │     │      ├── SelectDropdown
  │   │     │     │      ├── VoyagesHompPage
  │   │     │     │      ├── VoyagesTable
  │   │     │     ├── ScrollPage
```

## Common Folder
The `Common` folder is used for components that are shared across multiple sections of your application. These components are often generic and can be reused throughout the app.

## Feature-Specific Folders
Each major feature or section of your application should have its own folder within the `components` directory. In this example, there is a `Home` folder representing the homepage, but you can create folders for other features as needed.

## Component Files
Each component folder contains the following files:

- `ComponentName.js:` The JavaScript file where the component is defined.
- `ComponentName.css` (or `.scss`): The stylesheet for the component, if applicable.
- `ComponentName.test.js` (optional): Unit tests for the component using a testing framework like Jest.


## Benefits of This Structure

1) `Modularity:` Components are organized by feature, making it easy to locate and work with specific parts of your application.

2) `Reusability:` Components in the Common folder are easily accessible and can be reused across various sections of your app.

3) `Scalability:` As your application grows, this structure scales well, making it easier to manage an increasing number of components.

4) `Testing:` By placing unit tests in the same folder as the component, you can easily locate and run tests for specific components.

5) `Clear Separation of Concerns:` Keeping component files, stylesheets, and tests together maintains a clear separation of concerns.

## Usage
To use a component in your application, simply import it where needed:

```jsx
import Button from '../components/Common/Button/Button';
import Menu from '../components/Home/Menu/Menu';
import VideoBackground from '../components/Home/VideoBackground/VideoBackground';
// ...
```
## Contributing
This structure provides a clear and organized way to manage and integrate components into your React application, improving development efficiency and maintainability.