# Usage

This template contains a small native ESM library. Native ESM uses JavaScript `import` and `export` statements.

> After you create a repository from this template, replace this document with usage instructions for your library.

## Requirements

Use Node.js 26 or later to run the example and validate this repository.
Use an ESM project to import the sample API.

## Run the sample

Run this command from the repository root:

```sh
node examples/basic.mjs
```

The command prints:

```text
Hello, Eli!
```

The example calls `createGreeting` with the name `Eli`.
Read the [API reference](api.md) for the function details.

## Use a derived library

This template package is not available from npm.
Create a repository from this template before you install a library package.
Replace the package name, source code, type declarations, examples, and documentation.
Set the package publication and access options for the derived library.

After you publish the derived package, install it in an ESM project:

```sh
npm install @your-scope/your-library
```

Replace `@your-scope/your-library` with the package name from the derived library's `package.json`.
Import its documented exports from the package root.

```js
import { createGreeting } from "@your-scope/your-library";

console.log(createGreeting("Eli"));
```

This import works after the derived library exports `createGreeting` from its package root.
Update the example when the derived library uses a different API.

## Validate a derived library

Run `npm test` to check the source, tests, documentation, package, and repository rules.
Run `npm run typecheck` to check the TypeScript declarations.
Run `npm run pack` to check the files that npm will include in the package.

If npm reports `E404`, check the package name, registry, publication status, and access settings.
If Node.js cannot resolve an import, check the package exports and the installed package name.
