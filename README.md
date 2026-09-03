# 开发工具项目规范文档

本文档定义了开发工具项目的标准结构和要求，作为后续开发其他工具的统一规范。

## 使用方式

本仓库只承载规范文档，不提供可安装的代码。直接克隆或在线查看即可：

```bash
git clone https://github.com/farfarfun/fundev-doc.git
cat fundev-doc/README.md
```

新建或改造「开发工具类」项目时，对照下文的目录结构与 README 模板逐条检查是否合规；
组织级更通用的仓库规范见 [todo-list 仓库的 SPEC.md](https://github.com/farfarfun/todo-list/blob/master/SPEC.md)。

## 项目结构要求

### 1. 文档结构

`CHANGELOG.md` 放在**仓库根目录**（与 [SPEC.md](https://github.com/farfarfun/todo-list/blob/master/SPEC.md) §14.3 保持一致），其余项目文档放 `doc/` 文件夹：

```
project-name/
├── CHANGELOG.md           # 版本变更日志（新版本在最上面），根目录
└── doc/
    └── API.md             # API文档（包含所有类说明、字段说明、使用实例）
```

#### 1.1 版本变更日志
- **CHANGELOG.md**: 遵循 [Keep a Changelog](https://keepachangelog.com/) 格式，所有版本变更记录在一个文件中，新版本变更日志放在文件最上面，必须位于仓库根目录

#### 1.2 API文档
- **API.md**: 包含所有类的说明、字段说明和使用实例的完整API文档

### 2. 项目根目录结构

```
project-name/
├── README.md              # 项目说明文档
├── LICENSE               # 开源许可证
├── CHANGELOG.md         # 版本变更日志
├── .gitignore           # Git忽略文件
├── requirements.txt     # Python依赖 (Python项目)
├── package.json         # Node.js依赖 (Node.js项目)
├── doc/                 # 文档目录 (详见上述结构)
├── src/                 # 源代码目录
├── tests/               # 测试代码目录
├── scripts/             # 脚本文件目录
└── examples/            # 使用示例目录
```

## 开发规范

### 3. 代码规范
- 使用中文注释
- 遵循相应语言的编码规范 (PEP8 for Python, ESLint for JavaScript等)
- 函数和类必须有文档字符串
- 重要的业务逻辑必须有注释说明

### 4. 版本管理
- 使用语义化版本号 (Semantic Versioning)
- 每次发布前更新CHANGELOG.md
- 使用Git标签标记版本

### 5. 测试要求
- 单元测试覆盖率不低于80%
- 集成测试覆盖主要业务流程
- 提供测试数据和测试环境配置

### 6. 部署要求
- 包含环境变量配置说明
- 提供部署脚本和说明文档

## README.md 模板

每个项目的README.md应包含以下部分：

```markdown
# 项目名称

项目简短描述

## 功能特性
- 功能点1
- 功能点2

## 快速开始
### 安装
### 配置
### 运行

## 使用说明
### 基本用法
### 高级功能

## API文档
链接到 doc/API.md

## 开发指南
### 环境搭建
### 代码规范
### 测试

## 变更日志
链接到 CHANGELOG.md（根目录）

## 许可证
## 贡献指南
## 联系方式
```

## 文档维护

- 文档应与代码同步更新
- 重要变更必须更新相关文档
- 定期审查和更新文档内容
- 使用Markdown格式编写所有文档

---

**注意**: 本规范为强制性要求，所有新项目必须严格遵循此结构和规范。

---

## 关于 farfarfun

[farfarfun](https://github.com/farfarfun) 是一个专注于实用工具库的开源组织，
涵盖云存储、数据处理、AI、多媒体与开发工具链等方向。

- 🏠 组织主页：<https://github.com/farfarfun>
- 📧 联系：farfarfun@qq.com

本项目基于 [MIT](LICENSE) 协议开源。