# faker-error-types

Install dependencies:

```
pnpm i
```

`tsc` gives the error:

```
> tsc

node_modules/.pnpm/@faker-js+faker@6.0.0-alpha.3/node_modules/@faker-js/faker/index.ts:4:1 - error TS1203: Export assignment cannot be used when targeting ECMAScript modules. Consider using 'export default' or another module format instead.

4 export = faker;
  ~~~~~~~~~~~~~~~


Found 1 error.
```

This is fixed by adding the "types" field:

From:

```json
{
  "name": "@faker-js/faker",
  "version": "6.0.0-alpha.3",
  "description": "Generate massive amounts of fake contextual data",
  "repository": {
    "type": "git",
    "url": "https://github.com/faker-js/faker.git"
  },
  "license": "MIT",
  "main": "index.js",
  "scripts": {}
}
```

To:

```json
{
  "name": "@faker-js/faker",
  "version": "6.0.0-alpha.3",
  "description": "Generate massive amounts of fake contextual data",
  "repository": {
    "type": "git",
    "url": "https://github.com/faker-js/faker.git"
  },
  "license": "MIT",
  "main": "index.js",
  "types": "index.d.ts",
  "scripts": {}
}
```
