---
source: https://docs.deno.com/runtime/manual/getting_started/first_steps
tags:
  - draft
  - backend
  - deno
  - deno-manual
---
Create a deno project

```bash
deno init
```

Run a deno script

```bash
deno run <filename>
```

Runtime secure by default. Explicit permission must be given to allow a script to access potentially sensitive APIs 

> [!note]
> - run `deno help run` to see a list of all permissions
> - grant all permission with `deno run -A <filename>`

Modules are imported with ECMAScript syntax. Deno support load and executing code from URLs.

```typescript
import { assertEquals } from "https://deno.land/std@0.224.0/assert/mod.ts";
```

configure deno in the `deno.json` or `deno.jsonc` file.

Deno allows the use of npm and node modules.

```typescript
import express from "npm:express@4"
```

```typescript
import { readFileSync } from "node:fs"
```

> [!warning]
> Figure out how to get types from `@types/node`


>[!todo] Native web app frameworks
>- Deno Fresh
>- Alpeh
>- Hono

