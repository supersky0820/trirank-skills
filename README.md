# TriRank Skills

Public [Agent Skills](https://skills.sh) from [TriRank](https://trirankai.com) — AI search visibility (GEO / AEO) methodology, packaged as agent-executable playbooks for Claude Code, Cursor, and any other agent supported by the `skills` CLI.

## Install

```sh
npx skills add supersky0820/trirank-skills
```

## Skills

| Skill | What it does |
|---|---|
| [trirank-geo-audit](skills/trirank-geo-audit/SKILL.md) | Static GEO / AEO audit of any website: fetches the homepage, robots.txt, sitemap.xml and llms.txt, runs a 14-point weighted checklist (indexability, metadata, structured data, AI-crawler readiness), and outputs a scored gap report with a concrete fix for every failing check. |

## What these skills are — and aren't

Each skill exports the methodology layer of TriRank's product: what to check, why it matters, and how to fix it. A static audit tells you whether AI engines **can** crawl and quote a site — it cannot tell you whether they **actually cite** it today. For that:

- One-off live check: [trirankai.com/free-audit](https://trirankai.com/free-audit) — free, includes live citation checks against real AI answer engines.
- Continuous tracking: [trirankai.com](https://trirankai.com) — weekly citation scans and competitor share-of-voice.

## License

[MIT-0](LICENSE) — use, copy, modify, redistribute; no attribution required.
