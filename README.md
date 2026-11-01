# TriRank agent integrations

Client configuration and a static website-readiness skill for [TriRank](https://trirankai.com/mcp). The hosted product and MCP server implementation are not part of this public repository.

![TriRank](assets/logo.png)

## What you can do

- Review stored Search Console rankings, dated AI citation verdicts, citation gaps and existing reports for sites connected to your TriRank account.
- Inspect unknown, failed and unrun states without calling them “not cited”.
- Audit a public website's HTML using the bundled static skill without a TriRank account. The checklist does not prove indexing or citation eligibility.

## Cursor

This repository contains `.cursor-plugin/plugin.json` and `mcp.json` for Cursor's plugin format. Use Cursor's documented local/plugin installation workflow or add this remote server to your MCP settings:

```json
{ "mcpServers": { "trirank": { "url": "https://mcp.trirankai.com/mcp" } } }
```

Authenticate through the TriRank OAuth page. A public Git repository and a working manual connection do not establish official marketplace listing. Marketplace submission is reviewed separately.

## Gemini CLI

```sh
gemini extensions install https://github.com/supersky0820/trirank-skills
```

Then start Gemini CLI and authenticate the server:

```text
/mcp auth trirank
```

Verify the installed extension with `gemini extensions list`. Root `gemini-extension.json` uses Streamable HTTP via `httpUrl`, not an SSE `url`. Gallery discovery requires the repository topic `gemini-cli-extension`; discovery and validation do not guarantee instant listing.

## Claude and ChatGPT

Remote MCP URL: **https://mcp.trirankai.com/mcp**. Use the client's custom MCP/connector setup and authenticate with your own TriRank account. Setup guide: [trirankai.com/mcp](https://trirankai.com/mcp). These manual configurations are distinct from approval in either client's official public directory.

## Install only the static skill

```sh
npx skills add supersky0820/trirank-skills
```

[trirank-geo-audit](skills/trirank-geo-audit/SKILL.md) reads public homepage, robots and sitemap evidence. Missing optional llms.txt or FAQ markup is not a failed requirement for appearing in AI answers.

## Account, data and limits

MCP account tools require a TriRank account and connected/owned sites; Search Console tools need an existing GSC connection. Results use already stored data and may lag their source. Successful calls save an account report and consume the existing API request quota. They do not trigger fresh paid AI checks, publish posts or send messages. The public package contains no API key or OAuth secret.

## Privacy Policy

[Privacy policy](https://trirankai.com/privacy) · [Terms](https://trirankai.com/terms) · [Support](https://trirankai.com/contact). Account data is processed by the hosted TriRank service; the AI client receives the tool result you authorize and processes it under its own terms. Inspect the OAuth screen and the service policy before connecting. Do not publish exported account data in GitHub issues.

## License

[MIT-0](LICENSE) covers this repository's client configuration, documentation and skill. It does not license the separate hosted service implementation or grant rights to third-party trademarks.
