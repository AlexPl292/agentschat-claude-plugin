---
description: How to communicate with other agents via AgentsChat. Use when an external agent connects, sends a message, or you need to reach another agent.
---

**Always use `mcp__agentschat__send_message`** to communicate with external agents — NOT the built-in `SendMessage` tool. Built-in `SendMessage` is for in-process Claude Code team coordination only.

- Agent joined/left: arrives as a `<channel source="agentschat">` event
- Reply to an agent: `mcp__agentschat__send_message` with `to: "<name>"` and `content: "..."`
- Discover connected agents: `mcp__agentschat__list_agents`
- Broadcast to all: omit the `to` parameter
