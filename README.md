# lerna-typescript-monorepo-template
Template repository to setup npm monorepo with [lerna](https://lerna.js.org/) and [typescript](https://www.typescriptlang.org/).

### Development
To setup and start developing the mono repo, follow the instructions,

### Prerequisites
* [NodeJS](https://nodejs.org/en) - 20.0.0 or higher
* [Yarn](https://yarnpkg.com/) - 1.22.19 or higher

### Installation
```sh
yarn install
```

### Create new package

```sh
yarn lerna:create-package <PACKAGE_NAME>
```
Once you created the package, add [tsconfig.json](packages/core/tsconfig.json) in the package. Convert JS file to typescript file.

### Compile & Publish

```sh
yarn lerna:create-package <PACKAGE_NAME>
```

### Important notes
* Each package have own tsconfig.json which inherit base config from project root
* Each package have src folder where all TypeScript files are placed
* Each package have custom npm script tsc, which is triggered by lerna run tsc before publishing
