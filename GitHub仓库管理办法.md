# GitHub 仓库管理办法

## 适用范围

- 本办法所述内容均为**建议性**内容，如果有足够好的理由，可以不遵守该本文所述内容，但应当进行说明

- 在上海大学开源社区名下所有**提供对外服务**的 GitHub **代码**所在的仓库，用于

  - 保存记录和文档
  - 实验性目的
  - 对内服务
  - GitHub pages 内容 

  等的仓库不适用此办法

- 对于本文件生效前创建的仓库，如果要进行大的修改，建议逐步迁移到本办法所述的规范，但对于不大型修改的，没有必要迁移

- 对于由于“不知道此办法的存在”等原因，没有遵守此办法的 GitHub 仓库，社员有责任提醒和帮助仓库所有者明白此办法的意义，并协助其迁移。

## 沟通和文档中使用的语言

优先使用中文，如有可能提供英文翻译。

## 贡献代码的规则

根据项目进度和合作情况，允许灵活选择项目的贡献规则，这些规则可以在 GitHub 的 branch 保护规则中设置。

- 项目完全由一个人开发和维护，不准备吸引 contributor，直接允许 commit 即可
- 项目主要由一个人开发和维护，但准备吸引或已经有数个 contributor（无论contributor是否是社区内人员），则应当允许主要开发者 commit，其他 contributor 均需通过 pull request 提交代码，且要求一个 Approve 的 review 才允许 merge。
- 项目由数个人一起开发和维护，则所有 contributor 均需通过 pull request 提交代码，且要求数个 Approve 的 review 才允许 merge， Approve 个数按照项目实际情况确定。

## Readme.md

Readme 文件的目的是告知**用户和潜在开发者**该项目的用途。

Readme 文件应当简要的包含

- 项目的用途
- 若是其他更大项目的一部分，给出其链接
- 给用户的简单说明，如果内容足够少可以全部放在这里，否则给出最简单的使用范例和指向详细文档的链接
- 给希望参与开发的开发者的引导，如果内容足够少可以放在这里，否则放置指向 CONTRIBUTING.md 的链接

## Contributing.md

Contributing 文件的目的是告知**新开发者**如何上手开发项目的用途。

Contributing 文件应当包含

- 欢迎新开发者加入本项目的开发

- 简要介绍项目的技术栈

- 简要介绍项目的大体架构、各个文件（夹）都是用来干什么的

  本项如果过长，可以放到别的文件中，例如每个文件夹下的 readme.md 或者 wiki，在此处放置链接

- 工作流程的指导，包括

  - 如何fork并clone仓库
  - 如何安装依赖
  - 如何build
  - 如何运行可以在开发者端运行的测试
  - 如何提交代码
  - 如何提pull request

- 告知开发者如果遇到任何问题，欢迎提出issue。

## ISSUE_TEMPLATE

建议根据 GitHub 推荐的方式提供 bug_report 和 feature_request 的模板。

## pull_request_template.md

建议提供 pull_request 模板，内容可以根据需要制定，如关联的issue等等。

## LICENCE

至少应该有一个 LICENCE，类型不限。

## Issue 和 Pull Request 管理

### Labels

建议使用 Label 来标记 Issue 和 Pull Request 的类型，以便让开发者能快速找到自己感兴趣的 Issue 或可以 review 的 Pull Request，建议使用以下 label：

- 通用
  - `documentation`
  - `duplicate`
  - `cicd`
  - `test`
  - `refactor`
- issue
  - `bug`
  - `good first issue`
  - `easy`
  - `medium`
  - `hard`
  - `low priority`
  - `medium priority`
  - `high priority`
  - `wont fix`
- pull request
  - `invalid`

### Issue

项目的维护者应当时不时地查看是否有新的用户提出的 issue。

发现用户提出的 issue 应当尽快处理。

同时也可以用 issue 跟踪新功能的进度。

### Pull Request

项目的维护者应当时不时地查看是否有新的 Pull request。

发现 Pull request 应当尽快 review，如果 review 后已经达到 merge 的要求，则应当尽快merge。

## CI/CD

推荐使用 GitHub Actions 构建仓库的CI/CD系统，功能可以包含：

- 运行测试
- 构建并发布 Release/Docker 镜像
- 将构建出的制品发布到社区的**开发**服务器
