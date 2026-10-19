# API reference

This template exports one function from the package root: `createGreeting`.

> After you create a repository from this template, replace this reference with the API documentation for your library.

## `createGreeting`

```ts
createGreeting(name?: string): string
```

Create a greeting for a name.

| Input  | Type     | Required | Description                                        |
| ------ | -------- | -------- | -------------------------------------------------- |
| `name` | `string` | No       | The name to include. The default value is `world`. |

The function returns `Hello, <name>!`.
If you omit `name`, the function returns `Hello, world!`.
The function keeps the supplied name as written.

```js
import { createGreeting } from "@your-scope/your-library";

createGreeting("Eli"); // "Hello, Eli!"
createGreeting(); // "Hello, world!"
createGreeting(""); // "Hello, !"
```

Use the package root for imports. The package does not document or export internal source paths.

## TypeScript

The package includes `src/index.d.ts` as its type declaration.
TypeScript projects can infer that the function accepts an optional string and returns a string.

```ts
import { createGreeting } from "@your-scope/your-library";

const greeting: string = createGreeting("Eli");
```

Replace the example package name with the name in the derived library's `package.json`.
