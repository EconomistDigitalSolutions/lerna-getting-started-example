# Walkthrough notes

## Dependency graph

`npx nx graph`

## Build all packages

`npx lerna run build`
`npx lerna run test`

## Add caching

`npx lerna add-caching`

> See the newly created nx.json file

## Run commands with scope

`npx lerna run build --scope=remixapp`

`npx lerna run dev --scope=remixapp`

`npx lerna watch -- lerna run build --scope=remixapp --include-dependents`

## Publishing and versioning

- Make sure you have your GitHub auth setup in `~/.npmrc`

```
@economistdigitalsolutions:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:_authToken={GitHubPAT}
```

- Choose from locked or independent versioning
- Add publishConfig in package.json to point to GitHub

```
  "publishConfig": {
    "registry": "https://npm.pkg.github.com"
  }
```

`npx lerna version`

`npx lerna publish --no-private`

> The `Publish` command versions and publishes the packaages
