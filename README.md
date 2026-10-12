# [![eliware.org](https://eliware.org/logos/brand.png)](https://discord.gg/M6aTR9eTwN)

## @eliware/library-template [![npm](https://img.shields.io/npm/v/@eliware/library-template)](https://www.npmjs.com/package/@eliware/library-template) [![License](https://img.shields.io/github/license/eliware/library-template)](https://github.com/eliware/library-template/blob/main/LICENSE) [![CI](https://github.com/eliware/library-template/actions/workflows/ci.yaml/badge.svg)](https://github.com/eliware/library-template/actions/workflows/ci.yaml)

A reusable starting point for Eliware Node.js libraries using native ESM.

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

This template provides a reusable starting point. Each derived repository owns its product behavior and operating decisions.

## Requirements

Use Node.js 26 or later and npm 12 or later for repository validation.

## Setup

Create a repository from this template. Replace the template name, description, URLs, keywords, and sample content.
Run `npm ci` from the repository root.

## Usage

Follow this README and the [user guide](docs/README.md). Read [release notes](RELEASE_NOTES.md) for release history.

## Development

Read [AGENTS.md](AGENTS.md) and [the specifications index](specs/README.md) before you change files.
Keep documents and records in the repository that owns them.
Read [release notes](RELEASE_NOTES.md) for release history.

## Testing

Run `npm test` before handoff. It runs the repository checks through `eliware-test`.

## Troubleshooting

Install the required Node.js and npm versions. Run `npm ci` after dependency changes.
Review the file and rule in any validation error.

## Security

Keep credentials, secrets, private data, and runtime state out of Git.
Use only approved secret stores for secret values.

## API

The public function is `createGreeting(name?: string): string`.
Call `createGreeting("Eli")` to return `Hello, Eli!`. Call it with no name to return `Hello, world!`.

## Packaging

The package allowlist is `src/`, `docs/`, `README.md`, `AGENTS.md`, `LICENSE`, `RELEASE_NOTES.md`, `examples/`, and `specs/`.
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
