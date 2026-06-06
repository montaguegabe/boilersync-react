# boilersync-react

Shared React components and utilities for BoilerSync template workflows.

This package provides reusable UI and data helpers for reading BoilerSync template metadata, rendering template input fields, collecting field values, and re-exporting shared diff viewer utilities from `multi-react` for Openbase Coder frontends.

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
- Shared `multi-react` diff viewer exports

## License

MIT
