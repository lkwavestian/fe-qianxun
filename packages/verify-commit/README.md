# @fe-qianxun/verify-commit

一个简单的 commit message 校验工具

## 安装与使用

有两种使用方式，可使用`simple-git-hooks`运行 和 也可使用`husky`运行

### 使用 `simple-git-hooks` 运行

```sh
pnpm add -D @fe-qianxun/verify-commit simple-git-hooks
# OR
npm i -D @fe-qianxun/verify-commit simple-git-hooks
```

#### 添加配置项到 `package.json`

```sh
# 使用 npx + bin 运行
npm pkg set simple-git-hooks.commit-msg='npx fe-qianxun-verify-commit $1'

# OR 使用 pnpm + bin 运行
npm pkg set simple-git-hooks.commit-msg='pnpm fe-qianxun-verify-commit $1'

# OR 使用 node 运行
npm pkg set simple-git-hooks.commit-msg='node ./node_modules/@fe-qianxun/verify-commit/index.js $1'
```

#### 注册 `git-hooks`

> 当 `simple-git-hooks` 有更新时，需要重新注册

```sh
npx simple-git-hooks
```

> 添加 `prepare` 脚本，可以在 `install` 时自动注册已经配置的 `git-hooks`，第一次使用时需要手动运行一次 `npm run prepare`

```sh
npm pkg set scripts.prepare="npx simple-git-hooks"
```

### 使用 `husky` 运行

```sh
pnpm dlx husky-init && pnpm add -D @fe-qianxun/verify-commit
# OR
npx husky-init && npm i -D @fe-qianxun/verify-commit
```

#### 注册 `git-hooks`

```sh
npx husky add .husky/commit-msg 'npx fe-qianxun-verify-commit $1'
```

## 相关链接

- [vue — verify-commit-msg.js | GitHub](https://github.com/vuejs/vue/blob/main/scripts/verify-commit-msg.js)
- [Git 提交规范 | 千浔物语](https://docs.fe-qianxun.com/workflow/git/#commit-%E5%B8%B8%E7%94%A8-type)
- [simple-git-hooks | GitHub](https://github.com/toplenboren/simple-git-hooks)
- [husky | GitHub](https://github.com/typicode/husky)
