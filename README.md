# research-idea-forge

科研创新点构建 skill：机制迁移、数学问题构建、多入口构思、候选选择与贡献证据对齐。

当前版本：**1.1.0**。入口：[SKILL.md](research-idea-forge/SKILL.md)。

本技能默认独立完成创新发现、开发、构思过程中的候选比较及最终 idea 卡维护。支持用户已明确指定的项目主责，与 CCFA、idea-spark、Supervisor-Skills 和 PaperSpine 按需协作。

## 能做什么

- 从科学问题、机制迁移、数学重构、结构先验、机制组合或经验异常产生候选。
- 将迁移落到源—目标结构映射、必要适配、最近工作差异和负迁移条件。
- 将数学落到信息集、目标、约束、推导、可执行算子、符号到实现及退化情况。
- 审视候选的关键问题和五维收益，收敛主贡献及所需、现有、缺失证据。
- 维护一份 idea 卡，区分已核验事实、推断、提案和未完成工作。

## 安装到 Codex

将仓库中的 `research-idea-forge` 文件夹复制到 Codex 的 skills 目录。Windows PowerShell 示例：

```powershell
git clone https://github.com/ppsdk/research-idea-forge.git
$skillDestination = Join-Path $env:USERPROFILE '.codex\skills\research-idea-forge'
if (Test-Path -LiteralPath $skillDestination) {
    throw '目标技能已存在；请先备份并确认更新方式。'
}
Copy-Item -LiteralPath '.\research-idea-forge\research-idea-forge' -Destination $skillDestination -Recurse
```

如果设置了 `CODEX_HOME`，使用其 `skills` 子目录。重开会话或刷新技能列表后调用。

## 调用示例

```text
使用 $research-idea-forge，参考这些论文，从机制迁移和数学构建中寻找创新点，
核验最近工作，收敛一条主贡献，并维护一份最终 idea 卡。
```

```text
使用 $research-idea-forge，只比较这些候选的概念价值与逻辑，
不评分、不评实验或资源；若不检索文献，请标明新颖性未核验。
```

技能主体含 9 份按需阅读的参考文件、中文 idea 卡模板及 Codex UI 元数据。其他科研 skill 不是运行前提；文献核验仍需要宿主提供检索工具。

## 验证与边界

v1.1.0 已通过格式、本地引用、交付文件一致性及一个独立候选比较用例检查。原有投影、正则校正和预算分配的数值示例此前已做代数核对。有限用例通过不代表科研创新、实验效果或投稿准备已验证。

## 来源与许可

基于用户的科研构思规则整理，并参考 Supervisor-Skills 的选题审视与 PaperSpine 的贡献/证据方法。已针对多入口构思、概念与实证分离及独立产物主责作适配。

详见 [来源说明](THIRD_PARTY_NOTICES.md) 与 [许可](LICENSE)。
