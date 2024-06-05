---
source: https://docs.deno.com/runtime/manual/basics/import_maps
tags:
  - deno
  - backend
  - draft
  - deno-manual
---
in `deno.jsonc`

```json
{
  "imports": {
    "lodash": "https://esm.sh/lodash@4.17.21",
    "@std/assert": "jsr:@std/assert@^0.226.0",
  }
}
```

in project

```typescript
import _ from "lodash";
```

- version used by project is controlled in one place
- much short than specifying re-specifying the URL in each module that uses it

works for npm specifiers as well

```json
"lodash": "npm:lodash@^4.17
```

> [!tip]
> use `deno add` to automatically add to your import map

```bash
deno add @std/assert
```

use `"scopes"` to override imports within specific modules. this allows for different versions of dependencies to be used in different modules

```json
{
  "scopes": {
    "url-to-module": {
      "@std/assert": "jsr:@std/assert@^0.200.0",
    }
  }
}
```