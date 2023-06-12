# Voyages Application Interfaces
This folder contains a collection of interfaces used in the Voyages application. These interfaces define the structure and types of various objects and data used throughout the application.

## `Table of Contents`

```js
export interface Flatlabel {
    key: string;
    label: string;
    id: number;
    type: string;
}

export interface Options {
    [key: string]: VoyageOptionsValue;
}

export interface VoyageOptionsValue {
    type: string
    label: string
    flatlabel: string
}

export interface IsShowProp {
    [id: string]: boolean;
}

export interface OptionsDataState {
    value: Record<string, never>;
}

export interface RangeSliderState {
    rangeValue: RangeSliderMinMaxInitialState
    loading: boolean;
    error: boolean;
    varName: string;
    isChange?: boolean
    rangeSliderMinMax: RangeSliderMinMaxInitialState
}

export interface RangeSliderMinMaxInitialState {
    [key: string]: number[]
}

export interface AutoCompleteInitialState {
    results: [],
    total_results_count: number,
    autoCompleteValue: Record<string, AutoCompleteOption[] | string[]>;
    autoLabelName: string[]
    isChangeAuto: boolean
}

export interface AutoCompleteValueInitialState {
    [key: string]: string[]
}

export const TYPES: {
    IntegerField: string;
    DecimalField: string;
    CharField: string;
} = {
    IntegerField: 'IntegerField',
    DecimalField: 'DecimalField',
    CharField: 'CharField'
};


export interface AutoCompleteSliceLists {
    results: string[]
    total_results_count: number
}

export interface AutoCompleteLists {
    results: AutoCompleteOption[]
    total_results_count: number
}

export interface AutoCompleteOption {
    id: number
    label: string
}


export type VoyagaesFilterMenu = FilterMenu[]

export interface FilterMenu {
    label: string
    var_name?: string
    type?: string
    flatlabel?: string
    children?: ChildrenFilter[]
}

export interface ChildrenFilter {
    label?: string
    children?: ChildrenFilterArr[]
    var_name?: string
    type?: string
    flatlabel?: string
}

export interface ChildrenFilterArr {
    var_name: string
    type: string
    label: string
    flatlabel: string
}

export interface ChildrenNewObjectProp {
    varName?: string
    subMenu: string | null
    id: number | null
    flatlabel?: string | null
    type?: string | null
}

export interface VoyageGroupby {
    [key: string]: VoyageGroupbyValue;
}

export interface VoyageGroupbyValue {
    [key: string]: number[]
}

export interface plotXYProps {
    x_vars: PlotXYVar[]
    y_vars: PlotXYVar[]
}

export interface PlotXYVar {
    var_name: string
    type: string
    label: string
}

export interface BargraphXYVar {
    var_name: string
    type: string
    label: string
}

export interface ScatterOptionsXYResponse {
    [key: string]: [];
}

export interface VoyagesOptionProps {
    x_vars: string;
    y_vars: string;
}

export interface AutocompleteBoxProps {
    value?: AutoCompleteOption[];
}

export interface currentPageInitialState {
    currentPage: number;
    isOpenDialog: boolean
}

export interface HeaderNavBarMenuProps {
    setIsFilter: React.Dispatch<React.SetStateAction<boolean>>;
    isFilter: boolean;
    window?: () => Window;
}

export interface NavProps {
    setIsFilter: React.Dispatch<React.SetStateAction<boolean>>;
    isFilter: boolean;
    window?: () => Window;
}

export interface CanscandingMenuProps {
    setIsFilter?: React.Dispatch<React.SetStateAction<boolean>>;
    isFilter?: boolean;
    window?: () => Window;
}
```

Feel free to use these interfaces as references when working with the Voyages application. They provide the necessary structure and types for various data objects and components used in the application.