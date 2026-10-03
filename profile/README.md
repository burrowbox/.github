<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.svg">
    <img src="logo-light.svg" alt="Burrowbox" width="280">
  </picture>
</p>

<p align="center"><b>Computers for agents. One for you, or one for every customer.</b></p>

<p align="center"><b><a href="https://burrowbox.dev">→ Start using Burrowbox</a></b> · <a href="https://burrowbox.dev/docs">API docs</a></p>

---

Each Burrowbox machine is a persistent little Linux computer for an AI agent: a desktop, a browser that stays signed in, an encrypted credential vault, app installs, desktop control and its own MCP endpoint. Turn it off, and it comes back exactly as it was.

- **For your own agent:** create a machine, connect your agent with one command, and watch it work.
- **For your platform's customers:** provision one isolated machine per customer by API, with metering and live view built in.

```bash
bun add burrowbox
```

```ts
import { Burrowbox } from "burrowbox";

const bb = new Burrowbox(); // reads BURROWBOX_KEY
const machine = await bb.machines.create({ name: "research-bot", size: "tiny" });
console.log(machine.mcpUrl);
```
