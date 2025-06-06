# @fe-qianxun/prettier

prettier config used by qianxun

## 安装

```sh
pnpm add -D @fe-qianxun/prettier
# OR
npm i -D @fe-qianxun/prettier
```

## 使用

[Sharing configurations · Prettier](https://prettier.io/docs/en/configuration.html#sharing-configurations)

### 添加配置项到 `package.json`

> 直接使用时推荐该方案

```sh
npm pkg set prettier='@fe-qianxun/prettier'
```

### 使用单独的配置文件

> 为了兼容 `esm` 的项目，直接使用 `cjs`

先创建 `.prettierrc.cjs` 文件（内容如下）

```js
module.exports = require('@fe-qianxun/prettier')
```

命令行一键创建

```sh
echo "module.exports = require('@fe-qianxun/prettier')" > .prettierrc.cjs
```
