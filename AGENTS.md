# AGENTS.md

## Project

Repository: `eliware/library-template`. Purpose: maintain `@eliware/library-template`, a Node.js 26 starter for libraries using native ESM.

## Scope and boundaries

Repository-wide scope: these instructions apply throughout `eliware/library-template`; nearer `AGENTS.md` files govern their subdirectories. Important boundaries: this repository owns the template structure, sample API, tests, metadata, and documentation. It excludes ownership of shared requirements, documentation policy, and release procedures. Shared repository requirements are maintained by `eliware/test`, documentation indexes maintained by `eliware/docs`, and release procedures by `eliware/operations`.

## Layout

The required repository structure includes `src/` implementation modules mirrored by `tests/`, public API files `src/index.mjs` and `src/index.d.ts`, `docs/`, `specs/`, and runnable `examples/`. TypeScript declarations are type metadata validated by `npm run typecheck`, not executable source modules. The exact package contents allowlist is `src/`, `docs/`, `README.md`, `AGENTS.md`, `LICENSE`, `RELEASE_NOTES.md`, and `examples/`.

## Development

Before changing files, read the root README.md, applicable AGENTS.md instructions, applicable documentation, and applicable specifications.

Read this file, `README.md`, and applicable documentation and specifications before changing files. Repository-wide development instructions apply to all source and test subdirectories; nearer `AGENTS.md` files apply only in their subdirectories. Every source and test module must have a single responsibility: one cohesive purpose and one reason to change. Business-logic modules and coordinators are both valid, including coordinators of coordinators, when each module does only its own responsibility. When a change introduces a distinct responsibility, create a focused submodule with a mirrored test and wire it through its owner; do not add the new responsibility to an existing module. During ordinary review, do not ignore mixed responsibilities you notice; refactor them as part of the change. The enforced maxima of 100 source lines and 200 test lines are separate blocking limits: passing them does not prove cohesion or permit mixed responsibilities below those limits. Keep `src/` and `tests/` exactly mirrored. This guidance is actionable, current, and concise; project-specific guidance supplements shared requirements without weakening them.

## Validation

Use Node.js 26, native ESM `.mjs` modules, and npm. The library has no runtime environment settings or configuration files; runtime behavior is controlled by API options. Run `npm ci` after dependency changes and `npm test` for aggregate validation and coverage. Use `npm run lint`, `npm run audit`, `npm run format:check`, `npm run typecheck`, and `npm run pack` for focused validation. `npm run format` writes files; use `npm run format:check` for read-only formatting validation.

## Security

Protect credentials, tokens, and private data. Never commit secret values or machine-specific runtime state. Keep real credentials out of source, tests, examples, and documentation; use only safe placeholders in `.env.example`.

## Changes

Preserve the documented public contract and update its specifications, tests, declarations, documentation, examples, and release notes when applicable. Record only approved deviations. Publication requires explicit authorization through the applicable Operations release handoff; this file does not authorize publishing.

## Library

The public runtime entrypoint is `@eliware/library-template`, implemented by `src/index.mjs`; `src/index.d.ts` provides declarations for the public exports. Keep exports and declarations synchronized and test the public API. Document compatibility in the README and release notes. Packaging limits package contents to the documented allowlist. Validate behavior and coverage with `npm test`, types with `npm run typecheck`, and package contents with `eliware-test --pack` or `npm run pack`. Run the documented consumer-validation procedure before release consideration.

## npm publication

Package identity: @eliware/library-template. Version source: package.json.version. The exact package.json.files allowlist is src/, docs/, README.md, AGENTS.md, LICENSE, RELEASE_NOTES.md, examples/. Pack validation command: eliware-test --pack (also npm run pack). Pack validation result: require pass before release. npm provenance mechanism: npm Trusted Publishing with provenance. Exact-version public npm registry verification: verify the exact package.json version for @eliware/library-template at registry.npmjs.org. Release approval and execution ownership: Eli and the project developer run TagIt preflight; Eli decides readiness and instructs DevOps; DevOps executes the authorized release. Release authorization and handoff: publication requires explicit authorization through the Operations release handoff; this section grants no permission.
