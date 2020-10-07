# tsconfig

A strict tsconfig for TypeScript projects.

> **Note**: this repo is still experimental. It may not work correctly and breaking changes should be expected before version 1.

## Getting started

Install from NPM, including peer dependencies, with `--save-dev`

```bash
npm i @nick-mazuk/tsconfig typescript --save-dev
```

Then, create a `tsconfig.json` file in the root of your project with

```json
{
    "extends": "@nick-mazuk/tsconfig/tsconfig.json",
    "include": ["**/*.ts", "*.ts"], // add other files to include here
    "exclude": ["node_modules"]
}
```

### Versions

This package has configs for different scenarios (more coming).

| Version | extends | includes |
| ---- | ---- | ---- |
| **NextJS** | `@nick-mazuk/tsconfig/next` | `["next-env.d.ts", "**/*.ts", "**/*.tsx", "pages/_app.tsx", "error.tsx.config"]` |

When using a more specific config, the base config is not needed. For instance, with NextJS, this is all that's required:

```json
{
    "extends": "@nick-mazuk/tsconfig/next.json",
    "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", "pages/_app.tsx", "error.tsx.config"],
    "exclude": ["node_modules"]
}
```
