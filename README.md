# Scrutin Plugins

Public plugin manifests, skills, and branding assets for [Scrutin](https://scrutin.dev).
All customer plugins query existing analysis results through OAuth at
`https://mcp.scrutin.dev/mcp`. They do not start scans or change source code.

- Claude / Cowork / Claude Code: `plugins/claude-code`.
- ChatGPT / Codex / Cursor: `plugins/agent-plugin` (Agent Plugins 1.0).
- Antigravity: `plugins/antigravity` (partner directory review is separate).
- GitHub Copilot: `plugins/github-copilot` (portable skills plus a client-specific agent).

## Install in Claude Code

```text
/plugin marketplace add codigocentral/scrutin-plugins
/plugin install scrutin@scrutin
```

For direct MCP connection, installation from disk, requirements and examples,
read each plugin README and the [connection guide](https://docs.scrutin.dev/integrations/ai-assistants).
A repository publication does not mean approval in any vendor directory.

## Privacy and support

[Privacy](https://scrutin.dev/privacy) · [Terms](https://scrutin.dev/terms) ·
[Support](https://docs.scrutin.dev/integrations/ai-assistants#support).
Never put credentials or repository data in this repository or public issues.

## License

[MIT](LICENSE).
