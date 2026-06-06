# boilersync-react

React components and utilities for [BoilerSync](https://github.com/montaguegabe/boilersync) template workflows.

This package is the reusable React companion for BoilerSync. It provides UI and data helpers for displaying BoilerSync template metadata, rendering template input fields, collecting field values, and preparing those values for BoilerSync commands.

## Installation

```sh
npm install boilersync-react
```

The package expects React and React DOM to be provided by the host app:

```json
{
  "peerDependencies": {
    "react": ">=18 <20",
    "react-dom": ">=18 <20"
  }
}
```

## Usage

```tsx
import {
  TemplateFieldList,
  buildInitialFieldValues,
  serializeTemplateFieldValues,
  type TemplateInputField,
} from "boilersync-react";

const fields: TemplateInputField[] = [
  {
    name: "project_name",
    label: "Project name",
    required: true,
  },
];

const initialValues = buildInitialFieldValues(fields);
```

`TemplateFieldList` can render fields in read-only summary mode or interactive input mode. Pass `values` and `onFieldChange` to collect user input.

## Exports

- `TemplateFieldList`
- `TemplateInput`
- BoilerSync template metadata types
- Template field value helpers
- Shared diff viewer exports used by Openbase Coder frontends

## License

MIT
