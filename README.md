# grunt-react-docgen

> Grunt plugin based on [react-docgen](https://github.com/reactjs/react-docgen) and [doctrine](https://github.com/eslint/doctrine) for react component doc json generate.

## 快速上手

### 安装

```shell
npm install grunt-react-docgen --save-dev
```

### Gruntfile.js

```js
grunt.loadNpmTasks('grunt-react-docgen');
```

## 任务配置

### 概览

```js
grunt.initConfig({
  react_docgen: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
})
```

### Options

#### options.entryFiles

- Type: `Array`
- Default value: `['index.jsx']`

需要生成自动化文档的入口文件列表。

#### options.pkgInfo

- Type: `Object`
- Default value: `require(path.join(process.cwd(), 'package.json'))`

组件基本信息，默认取 `package.json`。

#### options.demoEntryJSX

- Type: `String`
- Default value: `'demo/index.jsx'`

组件 Demo 入口的 JSX 代码文件。

#### options.demoUrl

- Type: `String`
- Default value: `'../demo/index.html'`

组件 Demo 入口 url。

#### options.outputFilePath

- Type: `String`
- Default value: `'build/doc.html'`

输出文档 HTML 文件路径。

## 版本历史

- [0.1.0]
  - 初始记录
- [0.1.1]
  - 加上版本号 & tnpm version
- [0.1.2]
  - hack for import React from 'base' instead of from 'react' directly.
- [0.1.3][0.1.4]
  - fix & compatible for `author` field.
- [0.1.5]
  - add `flexible.js` to doc.html
- [0.2.0]
  - 从抓取 demo 内容改为指定 demo 路径通过 iframe 访问
- [0.2.1]
  - 参考 material-ui 的 API 文档输出
- [0.2.6]
  - Catch error for `reactDocgen.parse`
- [0.2.7]
  - fix doc html style

## License
Copyright (c) 2015 dickeylth. Licensed under the MIT license.

## Credits

- Inspired by [stardust](https://github.com/TechnologyAdvice/stardust)'s [gulp-react-docgen.js](https://github.com/TechnologyAdvice/stardust/blob/master/gulp/plugins/gulp-react-docgen.js)
