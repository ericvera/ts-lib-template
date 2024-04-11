# Typescript library repo template

An opinionated template repo configured with the following:

- Typescript
- ESM only
- Node >= 20
- Prettier (see `package.json` for config)
- Typescript ESLint (strict & typed mode)
- Github Actions deployment to npm on push to `main` branch
- Auto package version bump on push to `main` branch (based on [Conventional Commits](https://www.conventionalcommits.org/) conventions)
- Github Release generation on deployment (based on [Conventional Commits](https://www.conventionalcommits.org/) conventions)
- Yarn with `nodeLinker: node-modules`
- Block commits on lint/format issues (using `lint-staged`)
- VS Code config with suggested eslint and prettier extensions
- VS Code configured for auto-save

## Configuration before you start:

### Update the `LICENSE` file

- Replace `I Forgot To Add My Name Here` on the copyright line with your name

### Update the `package.json` file

- `name`: Your package name
- `repository`: Your repo info
- `keywords`: Keywords to help people find your package

### Add NPM_TOKEN to the repo secrets

    NOTE: The package must have been published at least once with `npm publish` in order to be able to generate a granular token scoped to the specific package.

1. [Get a token](https://docs.npmjs.com/creating-and-viewing-access-tokens#creating-granular-access-tokens-on-the-website) from npmjs.com
2. [Add a secret with the npm token to be used by Github Actions](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)

## Things to know

- Run `yarn` at the root to install all the dependencies and register the new package name before pushing the initial commit
- Ensure that any commits follow [Conventional Commits](https://www.conventionalcommits.org/) conventions in order for the version bump and release note to work appropriately
-
