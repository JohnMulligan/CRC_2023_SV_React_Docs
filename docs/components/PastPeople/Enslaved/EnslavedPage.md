# EnslavedPage Component
The `EnslavedPage` component is a React functional component that represents a page displaying information about the Enslaved dataset. It includes various dependencies, Redux state management, and event handlers.

## Dependencies
The component imports the following dependencies:

- `@mui/material`: Provides components such as `Box` and `Grid` for layout purposes.
- `@/style/page-past.scss`: Custom styles specific to the page.
- `react-redux`: Provides the `useDispatch` and `useSelector` hooks for Redux state management.
- `@/redux/store`: Imports the Redux store and provides the `AppDispatch` and `RootState` types.
- `@/share/InterfactTypesDatasetCollection`: Imports the BaseFilter and DataSetCollectionProps types.
- `@/redux/getPeopleDataSetCollectionSlice`: Imports Redux actions for setting the base filter, dataset header, blocks, style name, and text introduction.

## Usage
To use the `EnslavedPage` component, follow these steps:

- Import the necessary dependencies and components:
```jsx
import { Box, Grid } from '@mui/material';
import '@/style/page-past.scss';
import { useDispatch, useSelector } from 'react-redux';
import { AppDispatch, RootState } from '@/redux/store';
import {
  BaseFilter,
  DataSetCollectionProps,
} from '@/share/InterfactTypesDatasetCollection';
import {
  setBaseFilterPeopleDataKey,
  setBaseFilterPeopleDataSetValue,
  setBaseFilterPeopleDataValue,
  setDataSetPeopleHeader,
  setPeopleBlocksMenuList,
  setPeopleStyleName,
  setPeopleTextIntro,
} from '@/redux/getPeopleDataSetCollectionSlice';
```

- Implement the `EnslavedPage` component:

```jsx
const EnslavedPage = () => {
  // Redux state and dispatch
  const currentDate = new Date();
  const currentYear = currentDate.getFullYear();
  const { value, textIntroduce } = useSelector(
    (state: RootState) => state.getPeopleDataSetCollection
  );
  const dispatch: AppDispatch = useDispatch();
  
  // Event handler
  const handleSelectEnslavedDataset = (
    base_filter: BaseFilter[],
    textHeder: string,
    textIntro: string,
    styleName: string,
    blocks: string[]
  ) => {
    // ... implementation ...
  };
  
  // Render the component
  return (
    <>
      <div className="page" id="main-enslaved-home">
        <Box>
          <Grid container spacing={2}>
            <Grid item xs={12} className="grid-enslaved-introduction">
              <div>{textIntroduce}</div>
              <div className="btn-enslave-box">
                {value.map((item: DataSetCollectionProps, index: number) => {
                  const { base_filter, headers, style_name, blocks } = item;
                  return (
                    <div
                      onClick={() =>
                        handleSelectEnslavedDataset(
                          base_filter,
                          headers.label,
                          headers.text_introduce,
                          style_name,
                          blocks
                        )
                      }
                      key={`${item}-${index}`}
                      className="enslave-nav-btn"
                    >
                      {headers.label}
                    </div>
                  );
                })}
              </div>
            </Grid>
          </Grid>
        </Box>

        <div className="credit-bottom-right">{`Credit: Artist Name ${currentYear}`}</div>
      </div>
    </>
  );
};

export default EnslavedPage;
```

The `EnslavedPage` component is a functional component that represents a page displaying information about the Enslaved dataset. It includes various components, Redux state management, and event handlers.

The component renders a container `(Box)` and a grid `(Grid)` from Material-UI for layout purposes. It displays the dataset introduction text and a set of buttons for selecting different datasets. The component uses Redux to manage the state of the selected dataset and dispatches actions to update the Redux store based on user interactions.

By customizing the content and styles of the `EnslavedPage` component, you can create a page tailored to display information about the Enslaved dataset in your application or website.
