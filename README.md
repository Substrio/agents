<p align="center"><img src="plugins/substrio/assets/logo.png" alt="Substrio" width="160"></p>

# Substrio for AI agents

This repository is the plugin marketplace for Substrio. It connects your AI agent to Substrio, so the agent can build, test, and ship apps for you. Substrio is an app platform. Your account holds your apps, and each app comes with a host, data, functions, files, users, and a site.

There is no key in this plugin. The first time your agent calls a Substrio tool, you sign in once in your browser and approve the connection.

## Install

### Claude Code

```
claude plugin marketplace add Substrio/agents
claude plugin install substrio@substrio
```

Inside a session, `/plugin marketplace add Substrio/agents` adds the same marketplace, and `/plugin` installs from it.

### Codex

```
codex plugin marketplace add Substrio/agents
```

Then open `/plugins`, choose the Substrio marketplace, and install Substrio.

### Any other AI

Add Substrio as a remote MCP server at this address:

```
https://mcp.substrio.com/mcp
```

ChatGPT, Claude, Cursor, and most other AI apps take that address in their connector or MCP settings and sign you in the same way.

## What the agent reads

The plugin carries a short skill. The full guide for agents is at [substrio.com/agents.md](https://substrio.com/agents.md), and the complete tool reference is at [mcp.substrio.com/llms.txt](https://mcp.substrio.com/llms.txt).

## License

MIT
