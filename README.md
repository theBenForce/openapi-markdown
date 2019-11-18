# openapi-markdown

[![npm][npm-image]][npm-url] [![Build Status][travis-image]][travis-url]

CLI script to turn swagger/OpenAPI yaml into markdown files.
Primarily supports swagger 2.0, with some OpenAPI 3.0 features.

### Installation

    npm install -g openapi-markdown

### Usage

```
openapi-markdown [-h] [-v] -i [-o] [--skip-info]

Options:
  -h, --help      Show this help message and exit.
  -v, --version   Show program's version number and exit.
  -i , --input    Path to the openapi yaml file
  -o , --output   Path to the resulting md file
  --skip-info     Skip the title, description, version etc, whatever is in the info block.

```

### Npx (requires no installation)

```
npx openapi-markdown -i ./basic-auth.yaml
```

#### Example:

```javascript
openapi-markdown -i path/to/openapi/file.yaml
```

By default it will create the new file within the same directory with the same name as openapi file but with .md extension.
So, if openapi file is placed in `project/api-doc/openapi.yaml` the new file will be created as `project/api-doc/openapi.md`

You can also use it as a npm script in your package.json:

    npm i --save-dev openapi-markdown

```jsonc
{
  "scripts": {
    "md-docs": "openapi-markdown -i path/to/openapi.yaml"
    //...
  }
}
```

    npm run md-docs

[npm-url]: https://www.npmjs.com/package/openapi-markdown
[npm-image]: https://img.shields.io/npm/v/openapi-markdown.svg
[travis-url]: https://travis-ci.org/theBenForce/openapi-markdown
[travis-image]: https://travis-ci.org/theBenForce/openapi-markdown.svg?branch=master
