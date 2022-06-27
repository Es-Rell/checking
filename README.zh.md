语言 : [English](./README.md) | [中文](./README.zh.md)

# checking

一个简单验证 git commit 提交,使用 Angular 规范，依赖于[husky](https://github.com/typicode/husky)

## 📦 使用

安装

```
npm i @esrell/checking husky --save-dev
or
yarn add @esrell/checking husky -D

yarn husky install
or
npm run husky install

npx husky add .husky/commit-msg ""
```

在 `.husky/commit-msg` 文件末尾增加代码:

```
export GIT_PARAMS=$*
npx --no-install checking
```

## 🔨 测试

```
git add .
git commit -m"测试"
```

终端返回如下代表成功:

```
  ERROR  提交日志不符合规范

  合法的提交日志格式如下(模块可选填):


      feat(模块): 添加了个很棒的功能
      fix(模块): 修复了一些 bug
      docs(模块): 更新了一下文档
      style(模块): 格式化代码结构（不影响代码运行的变动)
      UI(模块): 修改了一下样式
      chore(模块): 对脚手架做了些更改
      refactor(模块): 代码重构但不影响运行与功能

      其他提交类型: locale, perf, workflow, build, CI, typos, tests, types, wip, release, dep

```

## 📝 说明

| 类型     | 说明                                              |
| -------- | ------------------------------------------------- |
| feat     | 新功能（feature）                                 |
| fix      | 修补 bug                                          |
| docs     | 文档（documentation）                             |
| style    | 格式（不影响代码运行的变动）                      |
| refactor | 重构（即不是新增功能，也不是修改 bug 的代码变动） |
| tests    | 增加测试                                          |
| chore    | 构建过程或辅助工具的变动                          |
| perf     | 性能优化                                          |
| ...      | 更多暂不做解释 😂                                 |

## 🔗 链接

- [更新日志](CHANGELOG.md)
