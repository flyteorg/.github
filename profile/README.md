![Flyte Image](https://raw.githubusercontent.com/flyteorg/static-resources/main/common/flyte_cover.jpg)

<h3 align="center">
  <a href="https://flyte.org">Website</a>
  <span> · </span>
  <a href="https://docs.flyte.org/">Documentation</a>
  <span> · </span>
  <a href="https://blog.flyte.org/">Blog</a>
  <span> · </span>
  <a href="https://slack.flyte.org/">Slack</a>
  <span> · </span>
  <a href="https://www.youtube.com/channel/UCNduEoLOToNo3nFVly-vUTQ/playlists">YouTube</a>
</h3>

<h3 align="center">
  Flyte 2 is the open-source AI runtime to scale durable workflows to production — on your own infra.
</h3>

Write plain, async-native Python that orchestrates agents, data and ML pipelines, and inference — with the durability, reproducibility, and observability that production demands.

#### Why Flyte 2

- **🤖 Dynamic, agent-native execution** — Write or generate orchestration logic that adapts on the fly at runtime. Loops, conditionals, fan-outs, and LLM-driven control flow are just Python.
- **🛡️ Durable, self-healing workflows** — Flyte 2 is infrastructure-aware, automatically recovering from both logic and infrastructure failures like OOM crashes. Every execution is logged, reproducible, and observable from a single UI.
- **⚡ Realtime and batch inference** — Flyte 2 handles inference natively, no separate serving stack required.

#### Architecture — where the code lives

| Repository | What it is |
| --- | --- |
| [flyteorg/flyte](https://github.com/flyteorg/flyte/tree/main) | The Flyte 2 control plane and backend live on `main` — scheduling, state, recovery, and the console. |
| [flyteorg/flyte-sdk](https://github.com/flyteorg/flyte-sdk) | The Python SDK — pure Python with async/await. `pip install flyte` |
| [flyteorg/flyte-sdk-go](https://github.com/flyteorg/flyte-sdk-go) | The Go SDK — interface with Flyte from other languages. |

#### Get started

```python
# pip install flyte
import flyte

env = flyte.TaskEnvironment(name="hello")

@env.task
async def hello(name: str) -> str:
    return f"Hello, {name}!"

if __name__ == "__main__":
    flyte.init_from_config()
    run = flyte.run(hello, name="world")
    print(run.url)
```

Show us some ❤️ by starring [flyteorg/flyte](https://github.com/flyteorg/flyte)!
