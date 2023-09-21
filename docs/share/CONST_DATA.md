# Application Constants Documentation

This documentation provides an overview of the application constants used in your JavaScript or TypeScript application. Constants are typically used to store values that do not change during the application's runtime but may be configured based on the deployment environment or provide meaningful names for certain values. Here's an explanation of the constants:

## General Constants
#### VOYAGETILE
- Type: String
- Purpose: Represents the title of the Voyages Database.
#### POPELETILET
- Type: String
- Purpose: Represents the title of the People Database.
#### EnslavedTitle
- Type: String
- Purpose: Represents the title for Enslaved People.
#### EnslaversTitle
- Type: String
- Purpose: Represents the title for Enslavers.
#### VOYAGESTABLEFILE
- Type: String
- Purpose: Represents the name of the Voyages Database table file.
#### YOYAGESCARDFILE
- Type: String
- Purpose: Represents the name of the Transatlantic Voyages card file.
#### ENSLAVEDCARDFILE
- Type: String
- Purpose: Represents the name of the Enslaved card file.
#### ENSLAVERSCARDFILE
- Type: String
- Purpose: Represents the name of the Enslavers card file.
#### NSLAVERS_TABLE_FILE
- Type: String
- Purpose: Represents the name of the Enslavers table cell structure file.
#### pathFlatFile
- Type: String
- Purpose: Represents the path to flat files used in the application.
#### ENSLAVED_TABLE_FILE
- Type: String
- Purpose: Represents the name of the Enslaved table cell structure file.
#### AFRICANORIGINS_TABLE_FILE
- Type: String
- Purpose: Represents the name of the African Origins table cell structure file.
#### TEXAS_TABLE_FILE
- Type: String
- Purpose: Represents the name of the Texas table cell structure file.
#### VOYAGESPAGE
- Type: String
- Purpose: Represents the Voyages Page identifier.
#### ALLVOYAGES
- Type: String
- Purpose: Represents the identifier for "all-voyages."
#### ALLVOYAGESPAGE
- Type: String
- Purpose: Represents the URL path for "all-voyages."
#### INTRAAMERICAN
- Type: String
- Purpose: Represents the identifier for "intra-american."
#### INTRAAMERICANPAGE
- Type: String
- Purpose: Represents the URL path for "intra-american."
#### TRANSATLANTIC
- Type: String
- Purpose: Represents the identifier for "transatlantic."
#### TRANSATLANTICPATH
- Type: String
- Purpose: Represents the path for "trans-atlantic."
#### TRANSATLANTICPAGE
- Type: String
- Purpose: Represents the URL path for "trans-atlantic."
#### VOYAGESTEXAS
- - Type: String
- Purpose: Represents the identifier for "texas."
#### VOYAGESTEXASPAGE
- Type: String
- Purpose: Represents the URL path for "texas."
#### PASTHOMEPAGE
- Type: String
- Purpose: Represents the Past Home Page identifier.
#### Enslaved
- Type: String
- Purpose: Represents the identifier for "Enslaved."
#### ALLENSLAVED
- Type: String
- Purpose: Represents the identifier for "all-enslaved."
#### ALLENSLAVEDPAGE
- Type: String
- Purpose: Represents the URL path for "all-enslaved."
#### ENSALVEDPAGE
- Type: String
- Purpose: Represents the URL path for "enslaved."
#### AFRICANORIGINS
- Type: String
- Purpose: Represents the identifier for "african-origins."
#### AFRICANORIGINSPAGE
- Type: String
- Purpose: Represents the URL path for "african-origins."
#### ENSLAVEDTEXAS
- Type: String
- Purpose: Represents the identifier for "texas."
#### ENSLAVEDTEXASPAGE
- Type: String
- Purpose: Represents the URL path for "texas."
#### DOCUMENTPAGE
- Type: String
- Purpose: Represents the Document Page identifier.
#### BLOGPAGE
- Type: String
- Purpose: Represents the Blog Page identifier.
#### ALLENSLAVERS
- Type: String
- Purpose: Represents the identifier for "all-enslavers."
#### ENSALVERSPAGE
- Type: String
- Purpose: Represents the URL path for "enslaver."
#### mbaccesstoken
- Type: String
- Purpose: Represents an access token for Mapbox services.
#### mappingSpecialists
- Type: String
- Purpose: Represents a URL for Mapbox mapping specialists.
#### mappingSpecialistsRivers
- Type: String
- Purpose: Represents a URL for Mapbox mapping specialists related to rivers.
#### mappingSpecialistsCountries
- Type: String
- Purpose: Represents a URL for Mapbox mapping specialists related to countries.
MAP_CENTER
- Type: Tuple (Array)
- Purpose: Represents the center coordinates for the map.
#### MAXIMUM_NATIVE_ZOOM
- Type: Number
- Purpose: Represents the maximum native zoom level for the map.
#### MINIMUM_ZOOM
- Type: Number
- Purpose: Represents the minimum zoom level for the map.
#### MAXIMUM_ZOOM
- Type: Number
- Purpose: Represents the maximum zoom level for the map.
#### ZOOM_LEVEL_THRESHOLD
- Type: Number
- Purpose: Represents a zoom level threshold.
#### VOYAGESTYPE
- Type: String
- Purpose: Represents the type identifier for "voyages."
#### ENSALVEDTYPE
- Type: String
- Purpose: Represents the type identifier for "enslaved."
#### ENSLAVERSTYPE
- Type: String
- Purpose: Represents the type identifier for "enslavers."
#### BLOGTYPE
- Type: String
- Purpose: Represents the type identifier for "blog."
#### minRadiusInpixels
- Type: Number
- Purpose: Represents the minimum radius in pixels.
#### maxRadiusInPixels
- Type: Number
- Purpose: Represents the maximum radius in pixels.
#### maxRadiusInPixelsNode
- Type: Number
- Purpose: Represents the maximum radius in pixels for nodes.
### Network Graph Node Type Constants
#### ENSLAVEDNODE
- Type: String
- Purpose: Represents the node type identifier for "enslaved."
#### ENSLAVERSNODE
- Type: String
- Purpose: Represents the node type identifier for "enslavers."
#### VOYAGESNODE
- Type: String
- Purpose: Represents the node type identifier for "voyages."
#### ENSLAVEMENTNODE
- Type: String
- Purpose: Represents the node type identifier for "enslavement_relations."
#### classToColor
- Type: Object
- Purpose: Maps node types to color codes.
#### RADIUSNODE
- Type: Number
- Purpose: Represents the radius of nodes.
#### cachenamePivot
- Type: String
- Purpose: Represents the cache name for pivot tables.
## Global Search Constants
#### GlobalSearchVoyagesType
- Type: String
- Purpose: Represents the global search type identifier for "voyages."
#### GlobalSearchEnslavedType
- Type: String
Purpose: Represents the global search type identifier for "enslaved."
#### GlobalSearchEnslaversType
- Type: String
Purpose: Represents the global search type identifier for "enslavers."
#### GlobalSearchBlogType
- Type: String
Purpose: Represents the global search type identifier for "blog."

These constants are likely used throughout your application to maintain consistency and configure different aspects of your app, such as titles, URLs, map settings, and node types.

Please note that the explanations provided here are based on the variable names and comments in your code. If there are additional details or specific usages of these constants in your application, you may need to refer to the codebase or documentation for further context.