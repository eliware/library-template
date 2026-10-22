# API reference

This template exports one function from the package root: `createGreeting`.

> After you create a repository from this template, replace this reference with accurate API documentation for the derived library.

## `createGreeting`

```ts
createGreeting(name?: string): string
```

Create a greeting for a name.

| Input  | Type     | Required | Description                                  |
| ------ | -------- | -------- | -------------------------------------------- |
| `name` | `string` | No       | The name to include. The default is `world`. |

The function returns `Hello, <name>!`.
If you omit `name` or pass `undefined`, the function uses `world`.
The function keeps the supplied string as written.
It does not remove spaces or change the supplied string.

```js
import { createGreeting } from "@your-scope/your-library";

createGreeting("Eli"); // "Hello, Eli!"
createGreeting(); // "Hello, world!"
createGreeting(""); // "Hello, !"
createGreeting(" Eli "); // "Hello,  Eli !"
```

Replace the example package name with the name in the derived library's `package.json`.
The package root is the documented import path.
The package does not expose internal source paths as public imports.

## TypeScript

The package includes `src/index.d.ts` as its TypeScript declaration.
The declaration describes an optional string input and a string result.

```ts
import { createGreeting } from "@your-scope/your-library";

const greeting: string = createGreeting("Eli");
```

Replace the example package name with the name in the derived library's `package.json`.
