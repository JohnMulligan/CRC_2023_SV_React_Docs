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