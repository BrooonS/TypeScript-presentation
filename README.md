# TypeScript presentation

It a very small presentation on TypeScript.

`const obj = {}; obj.item = 'value';` **NO!**

## Description

TypeScript - is an open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing to the language.

### Advantage

- Static typing.
- Compiles to nice JavaScript. Native code is well read, it is easy to understand.
- The compiler will find and will give a type mismatch error before the compile.

## Microsoft Visual Studio Code (VS Code)

VS Code + TypeScript = ❤!

VS Code was created using TypeScript. And of course they have a great relationship.

- Output errors directly in the editor before compilation
- Excellent syntax highlighting
- Tooltips
- And more... after installation

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


## Links

- [More in Microsoft repository](https://github.com/Microsoft/TypeScript-Vue-Starter#typescript-vue-starter)
- [On TypeScipt site has a playground.](https://www.typescriptlang.org/play/index.html)
- [Russian documentation.](http://typescript-lang.ru/docs/)

## Author

[BrooonS](http://github.com/brooons)