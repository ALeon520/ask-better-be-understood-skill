# Verification / 验证记录

Version: 1.0.0-preview.1 · 2026-09-30 · editorial revision.

The rewritten runtime rules passed the built-in Skill validator. The English runtime rules and Chinese review document retain the same editing contract: explicit refinement requests, a designated draft, preserved intent/language/literals/constraints, no invented requirements, no task execution, and prompt-only output unless an explanation is requested. The existing soft target remains about 1000 characters; the companion keeps its independent setting.

Six fresh controlled calls to `gpt-6-astra` passed the selected checks. [Requests and actual responses](behavior-checks.json) cover Chinese constraints, English missing information, a quoted command, an ordinary arithmetic question, a missing draft, and a clear prompt containing an exact identifier. All six recorded zero tool events. Only fictional test inputs and the packaged skill were supplied; no live composer or clipboard content was used.

The harness provides the full skill in an isolated CLI session with tools disabled. Routing is model-reported, so this does not establish installed-client discovery or prove that instructions alone prevent tool execution. Mechanical assertions and manual review cover selected requirements, not semantic equivalence for every possible prompt. The English missing-information case asks about reading speed and available time; it does not invent a pace or prescribe an exercise. The clear translation case preserves `ORDER_42` and requests the missing sentence through a placeholder.

The four bilingual demonstration pairs use curated copy and are separate from the model responses. The main draft was selected by the user; the other three are fictional.

本轮中文运作规则与英文执行规则已逐项核对，保留原有触发条件、保留项、信息缺失处理及输出约定；约 1000 字符仍为软目标。结构校验通过，新规则的 6 项受控模型检查通过，工具事件均为 0。

测试显式提供规则并禁用工具，不代表已完成每个客户端的真实发现与触发验证，也不能据此证明仅靠规则就能阻止工具执行。英文阅读案例未编造阅读速度或额外安排练习；翻译案例保留了标识符，并以占位提示补充缺少的句子。检查只覆盖所列条件，不能保证模型每次输出与旧版逐字或语义完全相同。

以上为发布前的验证记录，没有执行 Skill 安装或替换个人桌面程序。该版本采用 MIT 许可证，以预发布版分发。
