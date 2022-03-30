# cw-husky

> 基于[husky@7.0.4](https://github.com/typicode/husky)开发

嘉为蓝鲸Devops前端项目适用
安装后将会自动校验提交信息，提交信息以以下类别开头：

- docs: 仅文档变更
- feat: 新特性
- fix: 修复缺陷
- perf: 性能优化
- refactor: 代码重构，同时不能是缺陷修复或新特性
- style: 代码样式调整，不涉及业务变更
- test: 添加测试用例或修改测试用例

提交信息需包含工作项ID，若无以P0_0代替，例如：
`fix: p1_12345 流水线功能修复`

# 安装

```
yarn add cw-husky -D
```

# 使用

## 添加脚本

在根目录`package.json`文件的`scripts`中加入`prepare`脚本，内容为`cw-husky install`
设置后要执行一次此脚本

```sh
yarn prepare
```

## 新增Hook示例

```sh
npx cw-husky add .husky/pre-commit "npm test"
git add .husky/pre-commit
```

创建commit

```sh
git commit -m "Keep calm and commit"
# `npm test`将会自动执行
```

# Husky官方文档

https://typicode.github.io/husky
