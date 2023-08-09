# Node CI Action
This action is a basic CI for node projects. The action install node, install project dependencies, run project build and run project tests

> The action uses (actions/setup-node)[https://github.com/actions/setup-node] to install the node version with a limited arguments version

## Arguments

### Node version
- node-version: Version spec of the version to use in SemVer notation, examples: 12.x, 10.15.1, >=10.15.0, lts/Hydrogen, 16-nightly, latest, node
  - default: 20.x
- cache: Used to specify a package manager for caching in the default directory. Supported values: npm, yarn, pnpm
  - default: npm
 
## Usage

```yaml
steps:
- uses: arensis/node-ci-action@v1
  with:
    node-version: 18
    cache: 'yarn'
```

The node-version is optional. If not supplied will be installed the node version 20.x

The cache package is optional. If not supplied will be use npm
