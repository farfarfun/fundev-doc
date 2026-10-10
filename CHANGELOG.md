# Changelog

本项目遵循 [Keep a Changelog](https://keepachangelog.com/) 与[语义化版本](https://semver.org/lang/zh-CN/)，版本记录按倒序排列。

## [Unreleased]

### 新增

- 补充「使用方式」与「关于 farfarfun」区块，明确本仓库只承载规范文档。

### 修复

- 将规范文本中 `doc/CHANGELOG.md` 的示例路径改为根目录 `CHANGELOG.md`，与组织统一规范（[SPEC.md](https://github.com/farfarfun/todo-list/blob/master/SPEC.md) §14.3）保持一致。
- 将 Python 项目模板的依赖入口改为 `pyproject.toml`，并补充 uv 依赖管理要求。
- 按 [SPEC.md](https://github.com/farfarfun/todo-list/blob/master/SPEC.md) §5 改为明确「不提交 `uv.lock`」：根目录结构清单移除 `uv.lock`，并在 `.gitignore` 中启用 `uv.lock` 忽略规则。
- 「部署要求」收窄为仅适用于仓库自己持有长期运行服务的项目，并补充 `scripts/setup.sh` 统一入口、`start` 后台 / `run` 前台、`.run/` 运行时文件等条件（[SPEC.md](https://github.com/farfarfun/todo-list/blob/master/SPEC.md) §6）。
- `.gitignore` 按 SPEC.md §10.1 补充 `.claude/*`、`.codex/*`、`.cursor/*` 等 AI 编码助手目录的忽略规则，并用 `!` 保留团队共享定义；相关注释统一改为中文。

### 变更

- 无

### 废弃

- 无

## [0.1.0] - 2025

### 新增

- 初始版本：定义开发工具项目的标准目录结构与 README 模板。

### 修复

- 无

### 变更

- 无

### 废弃

- 无
