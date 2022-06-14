<!-- ## Git Commit Guidelines -->
# Git 提交指南

<!-- We have very precise rules over how our git commit messages can be formatted. This leads to **more
readable messages** that are easy to follow when looking through the **project history**. But also,
we use the git commit messages to **generate the AngularJS change log**. -->
我们对如何格式化 git 提交消息有非常精确的规则。这会导致在浏览**项目历史**时易于理解的**更具可读性的消息**。而且，我们使用 git commit 消息来**生成 AngularJS 更改日志**。

<!-- The commit message formatting can be added using a typical git workflow or through the use of a CLI
wizard ([Commitizen](https://github.com/commitizen/cz-cli)). To use the wizard, run `yarn run commit`
in your terminal after staging your changes in git. -->
可以使用典型的 git 工作流程或通过使用 CLI 向导 ([Commitizen](https://github.com/commitizen/cz-cli)) 添加提交消息格式。要使用该向导，请在 git 中暂存更改后在终端中运行 `yarn run commit`。

<!-- ### Commit Message Format -->
## 提交消息格式

<!-- Each commit message consists of a **header**, a **body** and a **footer**. The header has a special
format that includes a **type**, a **scope** and a **subject**: -->
每个提交消息由一个 **header**、一个 **body** 和一个 **footer** 组成。标头具有特殊格式，包括 **type**、**scope** 和 **subject**：

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

<!-- The **header** is mandatory and the **scope** of the header is optional. -->
**header** 是必需的，header 的 **scope** 是可选的。

<!-- Any line of the commit message cannot be longer than 100 characters! This allows the message to be easier
to read on GitHub as well as in various git tools. -->
提交信息的任何一行不能超过 100 个字符！这使得消息在 GitHub 以及各种 git 工具中更易于阅读。

<!-- ### Revert -->
## 回滚

<!-- If the commit reverts a previous commit, it should begin with `revert: `, followed by the header
of the reverted commit.
In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit
being reverted. -->
如果提交恢复了先前的提交，它应该以 `revert: ` 开头，后跟恢复提交的标头。
在正文中它应该说：`This reverts commit <hash>.`，其中哈希是要恢复的提交的 SHA。

<!-- ### Type -->
## Type

<!-- Must be one of the following: -->
必须是以下之一：

<!-- - **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing or correcting existing tests
- **chore**: Changes to the build process or auxiliary tools and libraries such as documentation
  generation -->
- **feat**：新功能
- **fix**：错误修复
- **docs**：仅更改文档
- **style**：不影响代码含义的更改（空格、格式、缺少分号等）
- **refactor**：既不修复错误也不添加功能的代码更改
- **perf**：提高性能的代码更改
- **test**：添加缺失或纠正现有测试
- **chore**：对构建过程或辅助工具和库的更改，例如文档生成

<!-- ### Scope -->
## Scope

<!-- The scope could be anything specifying place of the commit change. For example `$location`,
`$browser`, `$compile`, `$rootScope`, `ngHref`, `ngClick`, `ngView`, etc... -->
范围可以是指定提交更改位置的任何内容。 例如 `$location`、`$browser`、`$compile`、`$rootScope`、`ngHref`、`ngClick`、`ngView` 等...

<!-- You can use `*` when the change affects more than a single scope. -->
当更改影响多个范围时，您可以使用 `*`。

<!-- ### Subject -->
## Subject

<!-- The subject contains succinct description of the change: -->
主题包含对更改的简洁描述：

<!-- - use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize first letter
- no dot (.) at the end -->
- 使用祈使语气，现在时：“change”不是“changed”也不是“changes”
- 第一个字母不要大写
- 末尾没有点 (.) 或句号

<!-- ### Body -->
## Body

<!-- Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior. -->
就像在**主题**中一样，使用祈使式现在时：“change”不是“changed”也不是“changes”。
主体应该包括改变的动机，并将其与以前的行为进行对比。

### Footer

<!-- The footer should contain any information about **Breaking Changes** and is also the place to
[reference GitHub issues that this commit closes][closing-issues]. -->
页脚应包含有关 **Breaking Changes** 的任何信息，并且也是 [reference GitHub issues that this commit closes][close-issues] 的地方。

<!-- **Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.
The rest of the commit message is then used for this. -->
**重大更改**应以单词 `BREAKING CHANGE:` 开头，并带有一个空格或两个换行符。
然后将提交消息的其余部分用于此目的。
