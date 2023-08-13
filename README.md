# nodejs-playground

Project for studying Node.js and related technologies.

## Project Setup

```shell
# Install Yarn globally
npm install -g yarn

# Create Node.js project
mkdir nodejs-playground
cd nodejs-playground
npm init

# Add TypeScript support
yarn add -D typescript ts-node
npx tsc --init
```

Uncomment and set the following to the generated default `tsconfig.json`:

```text
"rootDir": "./src",
"outDir": "./build",
```

Add entry file `src/main.ts`

## NPM Task Setup

```json
{
  "main": "build/main.js",
  "scripts": {
    "build": "npx tsc",
    "clean": "npx tsc --build --clean",
    "clean-build": "npx tsc --build --clean && npx tsc",
    "start": "npx ts-node src/main.ts"
  }
}
```