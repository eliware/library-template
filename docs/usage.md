# Usage

Use Node.js 26 or later and npm 12 or later. After npm publication, install the package with this command:

> After you create a repository from this template, replace this document with end-user documentation for your repository.

```sh
npm install @eliware/library-template
```

Import `createGreeting` from `@eliware/library-template`. Pass a name to create a greeting.
The function returns `Hello, <name>!`. If you omit the name, it returns `Hello, world!`.

```js
import { createGreeting } from "@eliware/library-template";

console.log(createGreeting("Eli"));
```

Run the example from the repository root with `node examples/basic.mjs`.
The example prints `Hello, Eli!`.
