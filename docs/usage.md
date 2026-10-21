# Usage

This template demonstrates a small native ESM library. Native ESM uses JavaScript `import` and `export` statements.

> After you create a repository from this template, replace this document with usage instructions for the derived library.

## Requirements

Use Node.js 26 or later to run the sample and validate this repository.
Use an ESM project to import the sample API.

## Create a derived library

1. Create a repository from this template.
2. Set the package name, description, keywords, repository URL, homepage, issue URL, author, and license in `package.json`.
3. Set the package version to the first version for the derived library.
4. Set `private` to `true` when the package must not publish to npm.
5. Set `private` to `false` and set the correct `publishConfig.access` value when you publish to npm.
6. Replace the sample source, type declarations, examples, tests, and documentation.
7. Update `main`, `types`, `exports`, and `files` to match the derived library.
8. Remove or adapt `.github/workflows/npm.yaml` when the derived library does not publish to npm.
9. Run the validation commands before you share or publish the derived library.

The package name `@eliware/library-template` is not available from npm. Do not use it as an installable package name.

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
Read the [API reference](api.md) for details about this function.

## Import a published derived library

Publish the derived package before you install it from npm.

```sh
npm install @your-scope/your-library
```

Replace `@your-scope/your-library` with the package name in the derived library's `package.json`.
Import documented exports from the package root:

```js
import { createGreeting } from "@your-scope/your-library";

console.log(createGreeting("Eli"));
```

This example works after the derived package exports `createGreeting` from its package root.
Change the example when the derived library uses a different API.

## Validate the library

Run these commands from the repository root:

```sh
npm ci
npm test
npm run typecheck
npm run pack
```

`npm ci` installs the locked dependencies.
`npm test` runs aggregate repository checks.
`npm run typecheck` checks the TypeScript declaration.
`npm run pack` checks the files that npm includes in a package.

## Publish to npm

The npm workflow starts when you push a tag that matches `vMAJOR.MINOR.PATCH`.
The workflow runs `npm test` and checks that the tag matches the version in `package.json`.
After those checks pass, the workflow runs `npm publish --provenance`.

Configure npm trusted publishing for the derived GitHub repository and workflow before you push a release tag.
Complete the approved release steps before you publish a tag.
Remove or adapt the npm workflow when the derived library does not publish to npm.

## Troubleshoot installation

If npm reports `E404`, check the package name, registry, publication status, and access settings.
The template package is not published, so install a derived package only after its owner publishes it.

If Node.js cannot resolve an import, check the installed package name and the `exports` field.
Read the [API reference](api.md) to confirm the package root export.
