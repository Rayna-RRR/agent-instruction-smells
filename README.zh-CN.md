# agent-instruction-smells

语言：简体中文 | [English](README.md)

这是一个面向 `AGENTS.md`、`CLAUDE.md`、`SKILL.md`、Cursor rules 等 AI 编程代理指令文件的 “bad → fixed” 案例库。这里的 instruction smells 指的是那些看起来合理、但会让 AI 编程代理变慢、跑偏、误触发或更难验证的指令写法。每个案例都提供坏例子、修复例子、原因解释和可复制的修复提示。

## 这个仓库是什么

这是一个可复用的 instruction smells 样本库。每个案例都包含：

- 合成但贴近真实场景的坏例子。
- 更安全、更聚焦的修复例子。
- 对坏味道影响的解释：它为什么会伤害 AI 编程代理。
- 可复制的修复提示，适合粘贴到 Codex / Claude Code / Cursor。
- 面向维护者的检查清单和可复用的审查提示词。

## 这个仓库不是什么

这个仓库不是：

- 规则检查器
- 扫描器
- 命令行工具
- `AGENTS.md` 生成器
- 安全扫描器

它不会自动发现所有问题，也不会替你判断一个项目是否安全。它是面向教育和工作流质量的资源，帮助维护者更清楚地编写、审查和修复 AI 编程代理指令文件。

## 为什么 agent 指令文件会失效

AI 编程代理指令文件会失效，通常不是因为写得不够多，而是因为它开始承担错误的工作：保存项目历史、复制工具文档、堆积过期命令、混入互相冲突的规则，或者把不安全的捷径写成默认流程。

AI 编程代理会把这些文件当成当前任务的执行指导。一个过期命令、一段复制来的规则检查器说明、一个过宽的 skill 触发条件，都可能影响它接下来怎么读代码、怎么改文件、怎么验证结果。

好的指令文件应该小、当前、可执行、有边界。

## instruction smells索引

| instruction smells | 文件类型 | 风险 | 适用场景 | 操作 |
| --- | --- | --- | --- | --- |
| [上下文膨胀](smells/context-bloat/) | `AGENTS.md` | 高 | 文件像资料堆积，而不是任务指导。 | [复制修复提示](smells/context-bloat/repair-prompt.md) |
| [冲突指令](smells/conflicting-instructions/) | `AGENTS.md` | 高 | 不同段落要求 AI 编程代理做互相矛盾的事。 | [复制修复提示](smells/conflicting-instructions/repair-prompt.md) |
| [过期命令](smells/stale-commands/) | `AGENTS.md` | 中 | setup、test、deploy 等命令已经失效或引用旧工具。 | [复制修复提示](smells/stale-commands/repair-prompt.md) |
| [lint 规则泄漏](smells/lint-leakage/) | `AGENTS.md` | 中 | 规则检查器或格式化工具细节挤占了真正有用的工作流指导。 | [复制修复提示](smells/lint-leakage/repair-prompt.md) |
| [skill 泄漏](smells/skill-leakage/) | `AGENTS.md` | 中 | 项目级指令里粘贴了完整 skill 正文或工具手册。 | [复制修复提示](smells/skill-leakage/repair-prompt.md) |
| [过宽的 skill 触发条件](smells/overbroad-skill-trigger/) | `SKILL.md` | 高 | 一个 skill 几乎声明自己适用于所有任务。 | [复制修复提示](smells/overbroad-skill-trigger/repair-prompt.md) |
| [橡皮图章式 reviewer](smells/rubber-stamp-reviewer/) | `SKILL.md` | 高 | 审查指令鼓励默认认可，而不是发现缺陷。 | [复制修复提示](smells/rubber-stamp-reviewer/repair-prompt.md) |
| [不安全的 skill 指令](smells/unsafe-skill-instructions/) | `SKILL.md` | 严重 | skill 要求 AI 编程代理绕过审批、测试、敏感信息处理或其他安全边界。 | [复制修复提示](smells/unsafe-skill-instructions/repair-prompt.md) |

## 如何使用一个 instruction smells 案例

1. 打开 `smells/` 下的一个坏味道文件夹。
2. 先读 `bad.*.md`，识别问题长什么样。
3. 再对比 `fixed.*.md`，看修复后应该如何缩小范围、保留意图、降低风险。
4. 阅读 `explanation.md`，理解审查时该看什么。
5. 把 `repair-prompt.md` 复制到 Codex、Claude Code、Cursor 或其他 AI 编程代理，并指向你自己的指令文件。

示例：

```text
smells/conflicting-instructions/
  bad.AGENTS.md
  fixed.AGENTS.md
  explanation.md
  repair-prompt.md
```

## 仓库结构

```text
smells/
  <smell-name>/
    bad.AGENTS.md or bad.SKILL.md
    fixed.AGENTS.md or fixed.SKILL.md
    explanation.md
    repair-prompt.md

checklists/
  review-before-shipping-agent-instructions.md
  review-before-adding-a-skill.md
  review-after-codex-init.md

prompts/
  review-agents-md.md
  review-skill-md.md
  compress-agent-instructions.md

fixtures/
  sample-python-repo/
  sample-skill/
```

## 谁适合使用

适合你，如果你：

- 维护 `AGENTS.md`、`CLAUDE.md`、`SKILL.md` 或 Cursor rules。
- 需要审查涉及 AI 编程代理指令文件的 PR。
- 想给团队一组紧凑、可讨论的教学样本。
- 怀疑 AI 编程代理正在遵循过期命令、过宽触发条件或互相冲突的规则。
- 想把“帮我清理指令文件”变成更明确、可执行的修复任务。

## 安全与示例策略

- 坏例子是反面示例，不是推荐写法。不要复制或照着执行。
- 示例是合成或充分匿名化的，不应包含真实私有仓库指令、内部政策文本、客户内容或密钥。
- 不安全示例只用于帮助识别风险写法，不用于提供操作指南。
- 这个仓库不是安全扫描器，也不替代代码审查、安全审计或维护者判断。

## 贡献

欢迎贡献新的 instruction smells 案例，但请保持小而准：

- 不要在没有许可的情况下复制真实仓库指令。
- 使用合成或充分匿名化的例子。
- 坏例子和修复例子应该修复同一个底层问题，而不是换成另一个主题。
- 不要新增依赖、命令行工具、生成器、包管理文件或生成物。
- 修复提示应该能直接复制到 Codex、Claude Code 或 Cursor。

更多规则见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

MIT. See [LICENSE](LICENSE).
