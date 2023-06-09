# CRC_2023_SV_React_Docs

installation : 
```pip install mkdocs```

To test loacally:
```mkdocs serve```
 
Mkdocs documents: 
 - https://www.mkdocs.org/getting-started/

## Prerequisites
Make sure you have Node.js and npm (Node Package Manager) installed on your machine. You can download and install them from the official Node.js website: https://nodejs.org.

### Code Structure 
```
----main.md
            |-Component_Home.md-|-Canscanding.md 
            |                   |               |-CanscandingMenu.md 
            |                   |               |-Dropdown.md 
            |                   |               |-MenuListDropdown.md 
            |                   |               |-NestedMenuItem.md 
            |                   |               |-PaperDraggable.md 
            |                   |-fcComponets.md 
            |                   |               |-AGTable.md 
            |                   |               |-AutocompletedTree.md 
            |                   |               |-AutocompleteTreeView.md 
            |                   |               |-TableCharacter.md 
            |                   |               |-TableRangeSlider.md 
            |                   |-header.md 
            |                   |               |-HeaderNavBar.md 
            |                   |               |-HeaderSearchLogo.md
            |                   |-voyagePage.md |-Results
            |                   |               |     |-AggregationSumAverage.md 
            |                   |               |     |-AutocompletedBox.md 
            |                   |               |     |-BarGraph.md 
            |                   |               |     |-RangeSlider.md 
            |                   |               |     |-Scatter.md 
            |                   |               |     |-SelectDropdown.md 
            |                   |               |-ScrollPage.md
            |                   |               |-VoyagePage.md
            |-fetchAPI.md       |-fetchAggregationsSlider.md 
            |                   |-fetchApiService.md 
            |                   |-fetchAutoCompleted.md 
            |                   |-fetchOptionsData.md 
            |                   |-fetchOptionsFlat.md 
            |                   |-fetchVoyageGroupby.md
            |-redux.md          |-store.md 
            |                   |-getAutoCompleteSlice.md 
            |                   |-getOptionsDataSlice.md
            |                   |-getOptionsFlatObjSlice.md 
            |                   |-getScatterSlice.md 
            |                   |-getScrollPageSlice.md 
            |                   |-getVoyageGroupbySlice.md
            |                   |-rangeSliderSlice.md    
            |-share.md          |-AUTH_BASEURL.md 
            |                   |-InterfaceTypeNav.md 
            |                   |-InterfaceTypes.md
            |-style.md          |-All css && scss files style are in here to share to the whole app
            |-utils.md          |-getEnumColumnParams.ts
            |                   |-transatlantic_voyages_filter_menu.json
            |                   |-transatlantic_voyages_filter_menuTEST.json
            |                   |-VOYAGE_BARGRAPH_OPTIONS.json
            |                   |-VOYAGE_SCATTER_OPTIONS.json
----Endpoint_request.md 
                
```