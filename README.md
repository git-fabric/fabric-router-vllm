<p align="center"><img src="docs/banner.svg" alt="fabric-router-vllm: fabric-router: Ollama model specialized for fabric-sdk meta-routing" width="100%"></p>

# fabric-router-vllm

**fabric-router**: an Ollama model specialized for the **fabric-sdk meta-routing**, part of git-fabric's **fabric-llm** layer (`L3+L4 gateway`).

It answers questions about its domain locally, so the fabric only escalates to Claude when it has to. See [fabric-sdk](https://github.com/git-fabric/sdk) for how requests are routed.

| | |
|---|---|
| Base model | `qwen2.5:14b` |
| Context window | 8,192 tokens |
| Temperature | 0.10 |

## Use it

```bash
ollama create fabric-router -f Modelfile
ollama run fabric-router
```

## What's inside

A single [`Modelfile`](Modelfile): the base model, its sampling parameters, and a system prompt that teaches the model the fabric-sdk meta-routing.

<!-- org-footer -->
---

<p align="center"><sub>Part of <a href="https://github.com/git-fabric">git-fabric</a> · composable fabric apps for Git-native infrastructure · built by <a href="https://github.com/ry-ops">ry-ops</a></sub></p>
