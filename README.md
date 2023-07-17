# CRC_2023_SV_React_Docs

installation : 
```pip install mkdocs```

To test loacally:
```mkdocs serve```
 
Mkdocs documents: 
 - https://www.mkdocs.org/getting-started/

## Prerequisites
Make sure you have Node.js and npm (Node Package Manager) installed on your machine. You can download and install them from the official Node.js website: https://nodejs.org.


## Code Structure 
```
----main.md
  │   ├── components
  │   │     ├── canscanding
  │   │     │     ├── CanscandingMenu
  │   │     │     ├── CanscandingMenuMobile
  │   │     │     ├── Dropdown
  │   │     │     ├── MenuListDropdown
  │   │     │     ├── MenuListDropdownPeople.tsx
  │   │     │     ├── NestedMenuItem
  │   │     │     ├── PaperDraggable
  │   │     ├── FunctionComponents
  │   │     │     ├──  ColumnSelectorTable
  │   │     │     │      ├── ButtonDropdownSelectoreColumn
  │   │     │     │      ├── ColumnSelector
  │   │     │     │      ├── DropdownColumn
  │   │     │     │      ├── NestedMenuColumnItem
  │   │     │     ├── AutocompletedTree
  │   │     │     ├── CustomHeader
  │   │     │     ├── TableCharacter
  │   │     │     ├── TableRangeSlider
  │   │     │── header
  │   │     │     ├── drawerMenuBar
  │   │     │     ├── HeaderNavar
  │   │     │     ├── HeaderSearchLogo
  │   │     │── Home
  │   │     │     ├── stylesMenu
  │   │     │     │      ├── StyledBurger
  │   │     │     │      ├── SytledMenu
  │   │     │     ├── BurgerMenu
  │   │     │     ├── Menu
  │   │     │     ├── MenuDropdownProps
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
  │   │     │     │      ├── AutocompletedBox
  │   │     │     │      ├── BarGraph
  │   │     │     │      ├── PieGraph
  │   │     │     │      ├── RangeSlider
  │   │     │     │      ├── Scatter
  │   │     │     │      ├── SelectDropdown
  │   │     │     │      ├── VoyagesHompPage
  │   │     │     │      ├── VoyagesTable
  │   │     │     ├── ScrollPage
  │   │── fetchAPI
  │   │     ├── pastEnslavedApi
  │   │     │     ├── fetchEnslavedOptionsList
  │   │     │     ├── fetchPastEnslavedApiService
  │   │     │     ├── fetchPastEnslavedAutoCompleted
  │   │     │     ├── fetchPastEnslavedRangeSliderData
  │   │     │     ├── fetchVoyageSortedEnslavedTableData
  │   │     ├── voyagesApi
  │   │     │     ├── fetchApiService
  │   │     │     ├── fetchAutoCompleted
  │   │     │     ├── fetchOptionsData
  │   │     │     ├── fetchOptionsFlat
  │   │     │     ├── fetchRangeSliderData
  │   │     │     ├── fetchVoyageGroupby
  │   │     │     ├── fetchVoyageOptionsPagination
  │   │     │     ├── fetchVoyagesOptionsApi
  │   │     │     ├── fetchVoyageSortedData
  │   │── pages
  │   │     ├── Enslaved
  │   │     ├── Enslavers
  │   │     ├── Home
  │   │     ├── PastPage
  │   │     ├── VoyagesPage
  │   │── redux
  │   │     ├── getAutoCompleteSlice
  │   │     ├── getColumnSlice
  │   │     ├── getDataSetCollectionSlice
  │   │     ├── getFilterPeopleObjectSlice
  │   │     ├── getFilterSlice
  │   │     ├── getOptionsDataPastPeopleEnslavedSlice
  │   │     ├── getOptionsDataSlice
  │   │     ├── getOptionsFlatObjSlice
  │   │     ├── getPeopleDataSetCollectionSlice
  │   │     ├── getScrollEnlavedPageSlice
  │   │     ├── getScrollPageSlice
  │   │     ├── getTableSlice
  │   │     ├── rangeSliderSlice
  │   │     ├── store
  │   │── share
  │   │     ├── AUTH_BASEURL
  │   │     ├── CONST_DATA
  │   │     ├── InterfaceTypes
  │   │     ├── InterfaceTypesTable
  │   │     ├── InterfactTypesDatasetCollection
  │   │     ├── PeopleCollectionType
  │   │── style
  │   │     ├── homepage.scss
  │   │     ├── index.css
  │   │     ├── Nav.scss
  │   │     ├── page-past.scss
  │   │     ├── page.scss
  │   │     ├── Slider.scss
  │   │     ├── table.scss
  │   │── styleMUI
  │   │     ├── index.ts
  │   │     ├── thems.ts
  │   │── tests
  │   │     ├── components
  │   │     ├── flat-files
  │   │     │     ├── BARGRAPH_OPTIONS.test.ts
  │   │     │     ├── PIECHART_OPTIONS.test.ts
  │   │     │     ├── SCATTER_OPTIONS.test.ts
  │   │     │     ├── Table_Cell_Structure.test.ts
  │   │     │     ├── transatlantic_voyages_filter_menu.test.ts
  │   │     ├── redux-test
  │   │     │     ├── getDataSetCollection.test.ts
  │   │     ├── untils-test
  │   │     │     ├── valueGetter.test.ts
  │   │── utils
  │   │     ├── flatfiles
  │   │     │     ├── african_origins_filter_menu.json
  │   │     │     ├── african_origins_table_cell_structure.json
  │   │     │     ├── enslaved_filter_menu.json
  │   │     │     ├── enslaved_options.json
  │   │     │     ├── enslaved_table_cell_structure.json
  │   │     │     ├── enslaver_options.json
  │   │     │     ├── people_page_data.json
  │   │     │     ├── texas_filter_menu.json
  │   │     │     ├── texas_table_cell_structure.json
  │   │     │     ├── transatlantic_voyages_filter_menu_SIMPLE.json
  │   │     │     ├── transatlantic_voyages_filter_menu.json
  │   │     │     ├── varnamechecker.py
  │   │     │     ├── VOYAGE_BARGRAPH_OPTIONS.json
  │   │     │     ├── VOYAGE_COLLECTIONS.json
  │   │     │     ├── VOYAGE_PIECHART_OPTIONS.json
  │   │     │     ├── VOYAGE_SCATTER_OPTIONS.json
  │   │     │     ├── voyage_table_cell_structure__updated21June.json
  │   │     ├── functions
  │   │     │     ├── generateRowsData.ts
  │   │     │     ├── getRowsPerPage.ts
  │   │     │     ├── getColorStyle.ts
  │   │     │     ├── getEnumColumnParams.ts
  │   │     │     ├── hasValueGetter.ts
  │   │     │     ├── TableCollectionsOptions.ts
  │   │     │     ├── traverseData.ts
            
```