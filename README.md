# ts-lib-starter

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![Greenkeeper badge](https://badges.greenkeeper.io/alexjoverm/typescript-library-starter.svg)](https://greenkeeper.io/)
[![Travis](https://img.shields.io/travis/alexjoverm/typescript-library-starter.svg)](https://travis-ci.org/alexjoverm/typescript-library-starter)
[![Coveralls](https://img.shields.io/coveralls/alexjoverm/typescript-library-starter.svg)](https://coveralls.io/github/alexjoverm/typescript-library-starter)
[![Dev Dependencies](https://david-dm.org/alexjoverm/typescript-library-starter/dev-status.svg)](https://david-dm.org/alexjoverm/typescript-library-starter?type=dev)

**一个typescript类库项目的开发脚手架。**

本项目是 [typescript-library-starter](https://github.com/alexjoverm/typescript-library-starter) 脚手架的迭代升级版本。本项目在 typescript-library-starter 的基础上加以修改，更新了项目依赖，使用ESLint替换TS-Lint代码检查方案。

> typescript-library-starter 已经很久没更新了，项目依赖已经老旧，其使用的TS-Lint代码检查方案已经被TS官方放弃。

### Usage | 使用方法

```bash
git clone https://github.com/qiyu99/ts-lib-starter.git YOURFOLDERNAME
cd YOURFOLDERNAME

# Run yarn and write your library name when asked. That's all!
yarn
```

**Start coding!** `package.json`和入口文件已经为您设置好了，你只需保留这些文件的名称相同即可。

### scripts | 脚本

- `yarn lint`: Lints code
- `yarn build`: Generate bundles and typings, create docs
- `yarn start`: Run `yarn run build` in watch mode
- `yarn test:watch`: Run test suite in [interactive watch mode](http://facebook.github.io/jest/docs/cli.html#watch)
- `yarn test:prod`: Run linting and generate coverage
- `yarn commit`: Commit using conventional commit style ([husky](https://github.com/typicode/husky) will tell you to use it if you haven't :wink:)

### Importing library | 导入工具库

您可以导入生成的包以使用此程序生成的整个库：

```javascript
import myLib from 'mylib'
```

另外，如果您有模块化库，则可以从`dist / lib`导入已编译好的模块：

```javascript
import something from 'mylib/dist/lib/something'
```
### FAQ | 问答

#### 当运行 `yarn` 或 `npm install` 命令时，运行了哪个文件?

先运行`tools / init`脚本，该脚本为您设置了所有内容。 简而言之:
 - 修改 RollupJS 配置文件 `rollup.config.js`
 - 修改 `package.json` (name, main, module, typings, author配置项)
 - 修改测试用例文件