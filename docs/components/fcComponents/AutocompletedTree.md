# AutocompleteBox Component

The AutocompleteBox component is a React component that provides an autocomplete functionality with nested selection capabilities. It utilizes the "multi-nested-select" library to achieve this functionality.

##Features
- Autocomplete with nested selection: Users can search for and select items from a hierarchical structure.
- Customizable appearance: The component provides various options to customize its appearance, such as enabling buttons, displaying chips, setting width and height, and more.
- Event handling: The component supports event callbacks for various actions, including view more, chip deletion, and value change.
## Usage
To use the AutocompleteBox component, follow these steps:

1) Install the "multi-nested-select" package by running the following command:
```js
npm install multi-nested-select
```

2) Import the necessary dependencies and interfaces:

```jsx
import React, { useEffect, useRef, useState } from "react";
import { NestedSelect } from "multi-nested-select";

interface Country {
  name: string;
  code: string;
  disabled?: boolean;
  zones: Zone[];
  continent: string;
  provinceKey: string;
}

interface Zone {
  code: string;
  disabled?: boolean;
  name: string;
}
```

3) Create the AutocompleteBox component:
```jsx
const AutocompleteBox: React.FC = () => {
  const ref = useRef<HTMLDivElement>(null);
  const [response, setResponse] = useState<Country[]>([]);
  const data: Country[] = [
    {
      name: "Afghanistan",
      code: "AF",
      disabled: true,
      zones: [],
      continent: "Asia",
      provinceKey: "REGION",
    },
    // Rest of the data...
  ];

  const callbackFunction = (value: Country[]) => {
    console.log(value);
    setResponse(value);
  };

  useEffect(() => {
    const handleClickOutside = (event: MouseEvent) => {
      if (ref.current && !ref.current.contains(event.target as Node)) {
        // alert("saving fat");
      }
    };

    document.addEventListener("click", handleClickOutside, true);

    return () => {
      document.removeEventListener("click", handleClickOutside, true);
    };
  }, []);

  return (
    <div className="center-component" ref={ref}>
      <NestedSelect
        enableButton={true}
        state={true}
        width={450}
        height={200}
        leading={true}
        chip={true}
        // limit={5}
        placeholderCtx={true}
        trailing={true}
        trailingIcon={true}
        inputClass="myCustom_text"
        continent={false}
        selectAllOption={true}
        dropDownClass="myCustom_dropbox"
        selectedValue={data}
        onViewmore={(v: any) => alert("viewed")}
        onChipDelete={(v: any) => alert("deleted")}
        onChange={(v: any) => console.log("okay", v)}
        callback={(val: any) => callbackFunction(val)}
      />
    </div>
  );
};

export default AutocompleteBox;
```
4) Customize the component by modifying the props passed to the NestedSelect component.

- You can enable or disable buttons, chips, and other options according to your requirements.
- Use the provided event callbacks to handle actions such as view more, chip deletion, and value change.
- Customize the appearance by setting width, height, CSS classes, and other relevant properties.

5) Incorporate the AutocompleteBox component into your application as needed:

```jsx
import AutocompleteBox from "./AutocompleteBox";

function App() {
  return (
    <div>
      <AutocompleteBox />
    </div>
  );
}
```