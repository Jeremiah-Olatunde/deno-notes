---
source: https://docs.deno.com/runtime/manual/getting_started/command_line_interface
tags:
  - backend
  - deno
  - draft
  - deno-manual
---
Help commands

```bash
deno help
deno -h
deno --help
```

```bash
deno help run
deno run -h
deno run --help
```

Specifying the source for `run`. A filename, a url or `-` to read a file from stdin

```bash
deno run <filename>
deno run <url>
cat main.ts | deno run -
```

> [!note] 
> Anything specified after the script name is passed into the script as a command line argument.

```bash
deno run main.ts the quick --brown --fox jumps-over-the "lazy dog"
```

```typescript
console.log(Deno.args); 
// [ "the", "quick", "--brown", "--fox", "jumps-over-the", "lazy dog" ] 
```

> [!warning]
> pass flags like `--help` `--watch` before the script name

Enable the built in file watcher with `--watch`.  

> [!note] Can be used with `deno (run|test|compile|fmt)`

```bash
deno run --watch main.ts
```

Code typechecking

```bash
deno check main.ts
deno run --check main.ts # typecheck code then execute
```

