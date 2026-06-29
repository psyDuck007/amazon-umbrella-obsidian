# AGENTS

This knowledge base is for JZAC / QZYD Amazon US cantilever patio umbrella operations.

Before editing or generating operational content, read:

1. `00-知识库入口/01-AI使用总规则.md`
2. `02-产品事实库/00-产品矩阵总表.md`
3. `02-产品事实库/05-参数与表述禁区/不得新增的参数与功能.md`
4. `13-LLM-Wiki工作台/index.md`
5. `13-LLM-Wiki工作台/workflows.md`
6. The module-specific rule file for the requested task.

Do not invent unverified ASINs, SKUs, product dimensions, certifications, wind ratings, base weights, warranty promises, power bank claims, or compliance-sensitive statements.

When information is missing, mark it as `待确认` and place it in `12-收集箱与附件/03-待确认产品信息.md` or `12-收集箱与附件/04-待验证观点.md`.

## LLM Wiki operating rules

This vault follows a Karpathy-style LLM Wiki pattern adapted for Amazon operations:

- Treat raw user inputs, reports, observations, and screenshots as source material.
- Keep product facts in `02-产品事实库`; never overwrite them from memory or assumptions.
- Use `13-LLM-Wiki工作台/raw/` for unprocessed source material when the user provides bulk notes or raw documents.
- Use `13-LLM-Wiki工作台/wiki/` for cross-module synthesis, strategy maps, concept pages, and question queues.
- Use `09-规则案例与实验/06-已验证结论/` for user-confirmed, validated operating conclusions.
- Use `09-规则案例与实验/01-待验证假设/` or `12-收集箱与附件/04-待验证观点.md` for unvalidated ideas.
- After any meaningful knowledge-base update, update `13-LLM-Wiki工作台/index.md` or `13-LLM-Wiki工作台/log.md` when relevant.

When the user sends short notes like `广告优化 已验证 ...`, `定价策略 待验证 ...`, or `标题优化 个人判断 ...`, classify them by topic, status, evidence, scope, and risk before writing them into the vault.
