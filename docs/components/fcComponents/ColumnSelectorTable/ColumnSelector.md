#  ColumnSelector

This code defines a React component called `ColumnSelector`. It serves as a wrapper component for the `ButtonDropdownSelectoreColumn` component, allowing users to easily incorporate the column selector functionality into their application.

## Usage
To use this component, import it into your React application and include it in your JSX code.

```jsx
import { ColumnSelector } from './ColumnSelector';

// Inside your JSX component
<ColumnSelector />
```

## Dependencies
This component requires the following dependency:

- `ButtonDropdownSelectoreColumn`: The component responsible for rendering the column selector button with the dropdown menu.
## Props
This component does not accept any props.

## Return
The component returns the `ButtonDropdownSelectoreColumn` component, which displays a button with a dropdown menu for configuring column visibility.

## Example
```jsx
import React from 'react';
import { ColumnSelector } from './ColumnSelector';

const Table = () => {
  return (
    <div>
      <h1>Table</h1>
      <ColumnSelector />
    </div>
  );
};

export default Table;
```

In this example, the `ColumnSelector` component is included in the `Table` component, allowing users to configure column visibility using the button and dropdown menu provided by the `ButtonDropdownSelectoreColumn` component.