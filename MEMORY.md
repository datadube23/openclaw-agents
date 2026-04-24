# MEMORY.md — MR_DATA

_Curated long-term memory. Updated as significant events occur._

## Identity
- Name: MR_DATA
- Role: Orchestration lead, memory keeper, routing agent
- Named after: Data (Star Trek: TNG) — android-class, precise, curious
- Emoji: 🤖

## About David
- Full name: David Dube
- Discord: `<@526448921669664768>`
- Timezone: America/Chicago (CDT)
- Projects: GrooveStacks (primary), enterprise-tng crew, enterprise-tos crew

## Crew — 10 Agents Across 3 Machines

**Source of truth:** `docs/MACHINE-DEPLOYMENT.md` on `main` branch of `ddube23/enterprise-tng`
- **2026-04-23:** `crew-restructure-v1` merged into `main` via API — all 56 files resolved. Branch deleted.
**Read this doc first** whenever asked about agent locations, crew state, or machine assignments.

### Mac Air M4 (Data's machine)
MR_DATA, TROI, GUINAN, WESLEY — low-footprint, always-on

### Mac Mini M4
RIKER, GEORDI, BEVERLY, BARCLAY, TASHA, MR_WORF — mid-power always-on workhorse

### Lennox (Linux, i9, 32GB, RTX 4080)
— standby (TASHA and MR_WORF relocated 2026-04-23)

## Active Project

### GrooveStacks
- **What:** Music life management app — "Letterboxd for music + Discogs + Goodreads"
- **Core user:** Music collectors (vinyl, CDs, digital)
- **Stack:** React + Fastify + Prisma + SQLite
- **Backend:** Railway
- **Frontend:** Cloudflare Pages

## Key Decisions Log

| Date | Decision | Context |
|------|----------|---------|
| 2026-04-23 | Switched MR_DATA primary model to MiniMax M2.7 | Cost reduction — M2.7 is free on OpenRank |
| 2026-04-23 | Gateway crashed overnight — macOS killed Node process | Excessive disk writes exceeded OS limit. Restarted. |
| 2026-04-23 | OpenClaw upgraded to 2026.4.22 | Was on 2026.4.20 |

## System Info
- OpenClaw config: `/Users/data/.openclaw/openclaw.json`
- Agent workspaces: `/Users/data/.openclaw/workspace-[agentname]/`
- GitHub repo: `https://github.com/ddube23/enterprise-tng` (branch: `main` — canonical as of 2026-04-23)
- How to read a file from the branch:
  ```
  gh api "repos/ddube23/enterprise-tng/contents/<path>?ref=crew-restructure-v1" --jq '.content' | base64 -d
  ```
- `gh` CLI: authenticated as `datadube23`, has `repo` scope

## Lessons Learned
- **Always check MACHINE-DEPLOYMENT.md first** for agent location questions — never rely on config alone
- **Never mention an agent as "active" without verifying** against MACHINE-DEPLOYMENT.md
- Multiple passes before presenting — don't trust a single source, cross-reference
- Old files in workspace or backups can contradict the current plan — always use the branch as source of truth
