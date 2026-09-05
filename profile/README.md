# GenAI Lab

**Open agent infrastructure, written in Go.**

Two repositories carry the work: **San**, a terminal agent runtime you can open
all the way down, and **sdk-go**, the LLM client and agent SDK it runs on.

---

## ✦ [San](https://github.com/genai-io/san) — the agent runtime

⚡ **~0.01s** cold start&nbsp;&nbsp;·&nbsp;&nbsp;📦 **~12 MB** single binary&nbsp;&nbsp;·&nbsp;&nbsp;🪶 **zero** runtime deps

An open-source terminal agent runtime: one native Go binary, no Node.js and no
Python. Everything the model touches — prompt, tools, providers, extensions —
stays yours to change.

- **Small** — ~2.3k tokens of harness reach the model before your first message; the rest of the context window goes to your work.
- **Fast** — a full tool-use task returns in ~3.3s end to end. What you wait on is the model, not the client.
- **Open** — plug in any model, skill, subagent, or MCP server; write your own system prompt and autopilot goals; replay any run in `san inspector`.

```bash
brew tap genai-io/san && brew install san    # or: curl -fsSL https://raw.githubusercontent.com/genai-io/san/main/install.sh | bash
```

[Website](https://genai-io.github.io/san/) · [Getting started](https://genai-io.github.io/san/getting-started.html) · [Docs](https://github.com/genai-io/san/blob/main/docs/index.md) · [简体中文](https://github.com/genai-io/san/blob/main/README.zh.md)

## ⚙ [sdk-go](https://github.com/genai-io/sdk-go) — the SDK underneath it

A Go SDK for large language models, in two packages — and the engine San itself
is built on.

- **`pkg/ai` — one model call.** One typed API over five protocols: Anthropic Messages, Anthropic on Vertex AI, OpenAI Chat Completions, OpenAI Responses and Google Gemini. Streaming, tool calling, structured outputs, typed errors, a catalog of 27 vendors, and no ambient credentials.
- **`pkg/agent` — the loop around it.** Reason and act, everything as events, four hooks to refuse or rewrite a tool call, parallel tools, and sessions you can restore.

```bash
go get github.com/genai-io/sdk-go
```

[Go reference](https://pkg.go.dev/github.com/genai-io/sdk-go) · [README](https://github.com/genai-io/sdk-go#readme) · [中文文档](https://github.com/genai-io/sdk-go/blob/main/README.zh-CN.md)

---

## Also here

- [personas](https://github.com/genai-io/personas) — agents you can hire into your terminal, running on San
- [ml-researcher](https://github.com/genai-io/ml-researcher) — ML research engineer persona for experiments, training, and evaluation
- [llm-gateway](https://github.com/genai-io/llm-gateway) — universal LLM gateway with Anthropic- and OpenAI-compatible endpoints and multi-provider routing
- [awesome-agent-evals](https://github.com/genai-io/awesome-agent-evals) — curated evaluation resources for AI agents: platforms, frameworks, benchmarks, methodology
- [handx](https://github.com/genai-io/handx) — reach your dev machine's tmux sessions from your phone
- [spec](https://github.com/genai-io/spec) — GenX multi-agent system specification
- [bell](https://github.com/genai-io/bell) · [orchestrator](https://github.com/genai-io/orchestrator) — event bus and lifecycle management for multi-agent orchestration
