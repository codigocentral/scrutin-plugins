# Scrutin AI assistant plugin

Read existing Scrutin analysis results in your authorized organization. The tools
list repositories and analyses, retrieve findings and dependency vulnerabilities,
and evaluate quality gates. They do not run scans, modify code, apply patches,
or post PR comments. Fixes proposed by the assistant are suggestions to review.

## Requirements

- A Scrutin account with an organization and completed cloud analyses.
- Free includes aggregate summaries. Individual analysis details require Pro or
  higher; PR/repository quality gates require Enterprise.
- Access to `https://mcp.scrutin.dev/mcp` over Streamable HTTP.

## Connect and authorize

In Antigravity, add the remote endpoint in `mcp_config.json`:

```json
{ "mcpServers": { "scrutin": { "serverUrl": "https://mcp.scrutin.dev/mcp" } } }
```

Validate a local plugin copy with `agy plugin validate --strict ./plugins/antigravity`.
The package contains its logo, license, and three workflow skills. Marketplace
intake and production OAuth verification are separate from local validation.
Follow the assistant's browser OAuth flow, sign in to Scrutin, choose your
organization, and authorize read-only access. Never paste passwords, API keys,
or access tokens into chat. If the public marketplace repository is unavailable,
use the direct MCP connection or a locally exported plugin until publication.

## Try it

- "List my repositories in Scrutin."
- "Show critical findings from the latest analysis of my repository."
- "Explain the quality gate evaluation for that analysis."
- "Summarize the latest analysis counts and aggregate metrics."

The three skills are `review-pr`, `explain-finding`, and `repository-risk`.
They interpret existing results. They report missing data and plan restrictions
without inventing findings or claiming that work was performed.

## Privacy Policy

Tools expose analysis results from the organization you authorize. Findings may
include file names, line references, code excerpts, and vulnerability information.
Retrieved data is shared with your connected assistant and handled under its
provider's policies and the [Scrutin Privacy Policy](https://scrutin.dev/privacy).
Tokens authorize read-only access; no public package contains credentials.
Revoke the connection in Scrutin Settings → Integrations → Connected apps.
See the [Terms of Service](https://scrutin.dev/terms).

## Support

[Connection and troubleshooting guide](https://docs.scrutin.dev/integrations/ai-assistants#support)
or [support@scrutin.dev](mailto:support@scrutin.dev).

## License

Plugin manifests, skills, and bundled assets are distributed under the
[MIT License](LICENSE).
