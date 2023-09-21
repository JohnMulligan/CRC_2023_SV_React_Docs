# Voyages_CRC_2023_Docs

This repository contains the documentation for the Voyages_CRC_2023 project, which is a comprehensive platform for exploring historical data related to voyages, enslaved people, and more. This README provides essential information for setting up and navigating the documentation.

![voyagesHome](./docs/assets/voyagesHome.png)


## Installation
To view and work with this documentation locally, you need to have `mkdocs` installed. You can install it using `pip`, the Python package manager:
```jsx
pip install mkdocs
```

## Usage
To test the documentation locally, you can use the following command:
```jsx
mkdocs serve
```
This will launch a local development server, allowing you to view the documentation in your web browser.

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Additional Resources
For more information on using mkdocs or customizing the documentation, refer to the official mkdocs documentation:

- MkDocs Getting Started [https://www.mkdocs.org/getting-started/]


## Project Structure
The documentation is organized into sections and follows a structured hierarchy, making it easy to navigate and find specific information. Below is an overview of the key folders and sections:
```
----main.md
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
  │   │── fetchAPI
  │   │     ├── blogApi
  │   │     │     ├── fetchAuthorData
  │   │     │     ├── fetchBlogAutoCompleted
  │   │     │     ├── fetchBlogData
  │   │     │     ├── fetchInstitutionDataAPI
  │   │     ├── geoApi
  │   │     │     ├── fetchEnslavedGeoTreeSelect
  │   │     │     ├── fetchEnslaversGeoTreeSelect
  │   │     │     ├── fetchVoyagesGeoTreeSelect
  │   │     ├── homeApi
  │   │     │     ├── fetchSearchGlobal
  │   │     ├── pastEnslavedApi
  │   │     │     ├── fetchEnslavedMap
  │   │     │     ├── fetchPastEnslavedApiService
  │   │     │     ├── fetchPastEnslavedAutoCompleted
  │   │     │     ├── fetchPastEnslavedOptionsApi
  │   │     │     ├── fetchPastEnslavedOptionsList
  │   │     │     ├── fetchPastEnslavedRangeSliderData
  │   │     │     ├── fetchPastEnslavedSortedTableData
  │   │     │     ├── fetchPastNetworksGraph
  │   │     ├── pastEnslaversApi
  │   │     │     ├── fetchPastEnslaversApiService
  │   │     │     ├── fetchPastEnslaversAutoCompleted
  │   │     │     ├── fetchPastEnslaversOptionsApi
  │   │     │     ├── fetchPastEnslaversOptionsList
  │   │     │     ├── fetchPastEnslaversRangeSliderData
  │   │     │     ├── fetchPastEnslaversSortedTableData
  │   │     ├── voyagesApi
  │   │     │     ├── fetchApiPivotCrosstabsTables
  │   │     │     ├── fetchApiService
  │   │     │     ├── fetchAutoVoyageComplete
  │   │     │     ├── fetchOptionsData
  │   │     │     ├── fetchOptionsFlat
  │   │     │     ├── fetchRangeSliderData
  │   │     │     ├── fetchVoyageGroupby
  │   │     │     ├── fetchVoyageOptionsAPI
  │   │     │     ├── fetchVoyagesMap
  │   │     │     ├── fetchVoyagesOptionsApi
  │   │     │     ├── fetchVoyageSortedData
  │   │── pages
  │   │     ├── AuthorPage
  │   │     ├── BlogPage
  │   │     ├── DocumentPage
  │   │     ├── Enslaved
  │   │     ├── Enslavers
  │   │     ├── Home
  │   │     ├── InstitutionAuthorsPage
  │   │     ├── PastHomePage
  │   │     ├── VoyagesPage
  │   │── redux
  │   │     ├── getAutoCompleteSlice
  │   │     ├── getBlogDataSlice
  │   │     ├── getCardFlatObjectSlice
  │   │     ├── getColumnsSlice
  │   │     ├── getCommonGlobalSearchResultSlice
  │   │     ├── getDataPathNameSlice
  │   │     ├── getDataSetCollectionSlice
  │   │     ├── getFilterPeopleObjectSlice
  │   │     ├── getFilterSlice
  │   │     ├── getGeoTreeDataSlice
  │   │     ├── getLanguagesSlice
  │   │     ├── getNodeEdgesAggroutesMapDataSlice
  │   │     ├── getOptionsDataPastPeopleEnslavedSlice
  │   │     ├── getOptionsDataSlice
  │   │     ├── getOptionsFlatObjSlice
  │   │     ├── pastNetworksSlice
  │   │     ├── getPeopleEnslavedDataSetCollectionSlice
  │   │     ├── getPeopleEnslaversDataSetCollectionSlice
  │   │     ├── getPivotTablesDataSlice
  │   │     ├── getScrollEnslavedPageSlice
  │   │     ├── getScrollEnslaversPageSlice
  │   │     ├── getScrollPageSlice
  │   │     ├── getTableSlice
  │   │     ├── rangeSliderSlice
  │   │     ├── resetAll
  │   │     ├── store
  │   │── share
  │   │     ├── AUTH_BASEURL
  │   │     ├── CONST_DATA
  │   │     ├── InterfaceTypePastNetworks
  │   │     ├── InterfaceTypePivotTable
  │   │     ├── InterfaceTypes
  │   │     ├── InterfaceTypesBlog
  │   │     ├── InterfaceTypesGlobalSearch
  │   │     ├── InterfaceTypesMap
  │   │     ├── InterfaceTypesTable
  │   │     ├── InterfactTypesDatasetCollection
  │   │     ├── PeopleCollectionType
  │   │── style
  │   │     ├── blogs.scss
  │   │     ├── cards.scss
  │   │     ├── homepage.scss
  │   │     ├── index.css
  │   │     ├── map.scss
  │   │     ├── Nav.scss
  │   │     ├── networks.scss
  │   │     ├── page-past.scss
  │   │     ├── page.scss
  │   │     ├── Slider.scss
  │   │     ├── table.scss
  │   │── styleMUI
  │   │     ├── customStyle.ts
  │   │     ├── index.ts
  │   │     ├── thems.ts
  │   │── tests
  │   │     ├── flat-files
  │   │     │     ├── african_origins_filter_menu.test.ts
  │   │     │     ├── BARGRAPH_OPTIONS.test.ts
  │   │     │     ├── enslaved_filter_menu.test.ts
  │   │     │     ├── enslavers_filter_menu.test.ts
  │   │     │     ├── PIECHART_OPTIONS.test.ts
  │   │     │     ├── SCATTER_OPTIONS.test.ts
  │   │     │     ├── Table_Cell_Structure.test.ts
  │   │     │     ├── texas_filter_menu.test.ts
  │   │     │     ├── transatlantic_voyages_filter_menu.test.ts
  │   │     ├── redux-test
  │   │     │     ├── getColumns.test.ts
  │   │     │     ├── getDataSetCollection.test.ts
  │   │     ├── untils-test
  │   │     │     ├── valueGetter.test.ts
  │   │── utils
  │   ├── flatfiles --> all json files
  │   │     ├── african_origins_filter_menu.json
  │   │     ├── african_origins_table_cell_structure.json
  │   │     ├── enslaved_card.json
  │   │     ├── enslaved_filter_menu.json
  │   │     ├── enslaved_options.json 
  │   │     ├── enslavers_card.json 
  │   │     ├── ENSLAVERS_COLLECTIONS.json
  │   │     ├── enslavers_filter_menu.json
  │   │     ├── enslaved_table_cell_structure.json 
  │   │     ├── PEOPLE_COLLECTIONS.json
  │   │     ├── enslaver_options.json
  │   │     ├── people_page_data.json
  │   │     ├── texas_filter_menu.json
  │   │     ├── texas_table_cell_structure.json
  │   │     ├── transatlantic_voyages_filter_menu_SIMPLE.json
  │   │     ├── transatlantic_voyages_filter_menu.json
  │   │     ├── varnamechecker.py
  │   │     ├── VOYAGE_BARGRAPH_OPTIONS.json
  │   │     ├── VOYAGE_COLLECTIONS.json
  │   │     ├── VOYAGE_PIECHART_OPTIONS.json
  │   │     ├── VOYAGE_PIVOT_OPTIONS.json
  │   │     ├── VOYAGE_SCATTER_OPTIONS.json
  │   │     ├── voyage_table_cell_structure__updated21June.json
  │   ├── functions
  │   │     ├── convertDataToGeoTreeSelectFormat.ts
  │   │     ├── convertToSlug.ts
  │   │     ├── createdLableNode.ts
  │   │     ├── createNodeDict.ts 
  │   │     ├── extractVarNamesTest.ts
  │   │     ├── formatCount.ts
  │   │     ├── formatText.ts
  │   │     ├── formatType.ts
  │   │     ├── generateCardsData.ts
  │   │     ├── generateColumnDef.ts
  │   │     ├── generateRowsData.ts
  │   │     ├── getColorStyle.ts
  │   │     ├── getGeoValuesCheck.ts
  │   │     ├── getMapBackgroundColor.ts
  │   │     ├── getMinMaxEdges.ts
  │   │     ├── getMinMaxValueNode.ts
  │   │     ├── getNodeColorStyle.ts
  │   │     ├── getNodeSize.ts
  │   │     ├── getOptionLabelSearchGlobal.tsx
  │   │     ├── getRowsPerPage.ts
  │   │     ├── hasValueGetter.ts
  │   │     ├── languages.ts
  │   │     ├── maxWidthSize.ts
  │   │     ├── pageVariantsFromTop.ts
  │   │     ├── processCardData.ts
  │   │     ├── TableAndCardCollectionsOptions.ts
  │   │     ├── traverseData.ts
  │   │     ├── updateColumnDefsAndRowData.tsx
  ├── App
  ├── main
  ├── env
  ├── eslintrc
  ├── gitignore
  ├── index.html
  
```

## Components
The `components` folder contains documentation related to the various React components used in the Voyages_CRC_2023 project. Components are grouped by feature, making it easier to understand and work with them.

## FetchAPI
The `fetchAPI` folder provides documentation for the API-related functionality of the project. It includes details about fetching data from various sources and endpoints.

## Pages
The `pages` folder contains documentation for different pages or sections of the project. Each page's documentation helps users understand its purpose and functionality.

## Redux
The `redux` folder explains how Redux is used within the project, including details about the slices and reducers responsible for managing application state.

## Share
The `share` folder contains shared resources, constants, and interface types that are used across different parts of the project.

## Style and StyleMUI
The `style` and `styleMUI` folders contain stylesheet files used for styling the project. They provide documentation for the project's styling approach.

## Tests
The `tests` folder contains documentation related to testing within the project, including unit tests, Redux tests, and utility tests.

## Utils
The `utils` folder explains the utility functions used throughout the project. It provides insights into how data is processed and transformed.

## Other Files
- `App.js:` The main application file.
- `main.md:` The main documentation file.
- `env:` Environment configuration.
- `eslintrc:` ESLint configuration.
- `.gitignore:` Git ignore file.
- `index.html:` HTML entry point for the project.

## Contribution
Contributions to this documentation are welcome. If you find any issues, errors, or would like to contribute improvements, please follow the contribution guidelines outlined in the project repository.

Thank you for using the Voyages_CRC_2023 documentation! We hope it helps you navigate and understand this valuable historical data resource.