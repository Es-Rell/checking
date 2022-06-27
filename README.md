Language : [English](./README.md) | [中文](./README.zh.md)

# checking

A simple validation git commit, using the Angular specification, relies on [husky](https://github.com/typicode/husky)

## 📦 Use

Install

```
npm i @esrell/checking husky --save-dev
or
yarn add @esrell/checking husky -D

yarn husky install
or
npm run husky install

npx husky add .husky/commit-msg ""
```

In `.husky/commit-msg` Add code at the end of the file:

```
export GIT_PARAMS=$*
npx --no-install checking
```

## 🔨 Test

```
git add .
git commit -m"Test"
```

The terminal returns the following to indicate success:

```
  ERROR  invalid commit message format.

  Proper commit message format is required for automated changelog generation. Examples:


      feat(compiler): add 'comments' option
      fix(compiler): fix some bug
      docs(compiler): add some docs
      style(compiler): Formatting code structure (changes that do not affect how the code runs)
      UI(compiler): better styles
      chore(compiler): Made some changes to the scaffolding
      refactor(compiler): Code refactoring without affecting operation and functionality

      Other commit types: locale, perf, workflow, build, CI, typos, tests, types, wip, release, dep

```

## 🔗 Link

- [Change Log](CHANGELOG.md)
