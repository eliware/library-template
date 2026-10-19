# [![eliware.org](https://eliware.org/logos/brand.png)](https://discord.gg/M6aTR9eTwN)

## @eliware/library-template [![npm](https://img.shields.io/npm/v/@eliware/library-template)](https://www.npmjs.com/package/@eliware/library-template) [![License](https://img.shields.io/github/license/eliware/library-template)](https://github.com/eliware/library-template/blob/main/LICENSE) [![CI](https://github.com/eliware/library-template/actions/workflows/ci.yaml/badge.svg)](https://github.com/eliware/library-template/actions/workflows/ci.yaml)

A starting point for Eliware Node.js libraries that use native ESM.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [Development](#development)
- [Testing](#testing)
- [Troubleshooting](#troubleshooting)
- [Security](#security)
- [API](#api)
- [Packaging](#packaging)
- [Examples](#examples)
- [Support](#support)
- [Links](#links)
- [License](#license)

## Features

Start a Node.js library with a sample ESM API, TypeScript declarations, tests, and examples.

## Requirements

Use Node.js 26 or later.

## Setup

Create a repository from this template. Replace the template identity, sample API, and package metadata.
Run `npm ci` from the repository root.

## Usage

The template is not published to npm. Read the [user guide](docs/README.md) and [release notes](RELEASE_NOTES.md).

## Development

Read [the specifications index](specs/README.md) before you change files.

## Testing

Run `npm test` before handoff.

## Troubleshooting

If `npm ci` fails, confirm that Node.js 26 or later is installed and that the configured registry responds.
If an import fails, check the package name and the `exports` field after you create your repository. See [usage guidance](docs/usage.md).

## Security

Keep credentials, secret values, private data, and runtime state out of Git.
Use an approved secret store to manage secret values.

## API

See the [API reference](docs/api.md) for the sample `createGreeting` function.

## Packaging

The `files` field in `package.json` lists `src/`, `docs/`, `README.md`, `AGENTS.md`, `LICENSE`, `RELEASE_NOTES.md`, `examples/`, `specs/`, and `package.json` for npm packaging.
Use numeric `MAJOR.MINOR.PATCH` versions. Use a `v<version>` tag for each release.
The npm workflow starts when you push the tag.
Run `npm run pack` to check package contents. Publish only after approved release steps.

## Examples

Run `node examples/basic.mjs` to see the sample API. See [example guidance](examples/README.md).

## Support

For help, questions, or to chat with the author and community, visit:

[![Discord](https://eliware.org/logos/discord_96.png)](https://discord.gg/M6aTR9eTwN)[![eliware.org](https://eliware.org/logos/eliware_96.png)](https://discord.gg/M6aTR9eTwN)

**[eliware.org on Discord](https://discord.gg/M6aTR9eTwN)**

## Links

- [Home Page](https://eliware.org)
- [GitHub Org](https://github.com/eliware)
- [GitHub Repo](https://github.com/eliware/library-template)
- [Bug Reports](https://github.com/eliware/library-template/issues)
- [npm](https://www.npmjs.com/package/@eliware/library-template)
- [Discord](https://discord.gg/M6aTR9eTwN)

## License

[MIT © Eliware](LICENSE)
