# TypeScript presentation

It's a small presentation of TypeScript.

## Description

TypeScript - is an open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing to the language.

### Advantage

- Static typing.
- Compiles to nice JavaScript.
- Native code is well read, it is easy to understand.
- The compiler will find and will give a type mismatch error before the compile.

## Install

### Webpack and Vue

Loader install

`npm install --save-dev typescript ts-loader`

Create config `tsconfig.json` in root folder.

```JSON
{
  "compilerOptions": {
    "module": "es6",
    "target": "es5",
    "noImplicitAny": false,
    "sourceMap": false
  },
  "include": [
    "resources/**/*"
  ]
}
```

#### webpack.config.js

```JS
module.exports = {
  module: {
    rules: [
      {
        test: /\.tsx?$/,
        loader: 'ts-loader',
        exclude: /node_modules/,
      },
    ],
  },
  resolve: {
    extensions: ['*', '.js', '.jsx', '.vue', '.ts', '.tsx'],
  },
};
```

[More in Microsoft repository](https://github.com/Microsoft/TypeScript-Vue-Starter#typescript-vue-starter)

## Author

[BrooonS](http://github.com/brooons)