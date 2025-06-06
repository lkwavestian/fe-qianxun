# @fe-qianxun/tailwind-config

tailwindcss config used by maomao

## 安装

```sh
pnpm add -D @fe-qianxun/tailwind-config
# OR
npm i -D @fe-qianxun/tailwind-config
```

## 使用

> 为了兼容 `esm` 的项目，直接使用 `cjs`

创建 `tailwind.config.cjs` 文件（内容如下）

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  presets: [require("@fe-qianxun/tailwind-config")],
};
```

## 功能

- [x] `tailwindcss` 基础配置
- [x] 新的工具类
  - `flex-row-center` 水平垂直居中（水平排列）
  - `flex-col-center` 水平垂直居中（垂直排列）
