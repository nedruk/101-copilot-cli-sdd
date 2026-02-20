# Workshop FEEDBACK Triage

> Auto-generated from all `⚠️ **FEEDBACK**` callouts across workshop modules.
> Workshop version: **v0.0.412**

### How to use this file
- Set **Status** to one of: `pending` · `fix` · `skip` · `done`
- Add **Notes** with instructions for what to change — Copilot will read them and action anything marked `fix`

---

## Module 01 — Installation

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 1 | [L146](docs/workshop/01-installation.md#L146) | Browser OAuth won't work in headless/CI/Docker environments — use `GITHUB_TOKEN` env var instead. | 🔑 Auth | done | remove it - in line 265 there is an example |
| 2 | [L265](docs/workshop/01-installation.md#L265) | Browser OAuth fails in Docker/CI/remote servers — use a PAT from https://github.com/settings/personal-access-tokens/new | 🔑 Auth | done | remove it - in line 146 there is an example |

---

## Module 02 — Operating Modes & Commands

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 3 | [L109](docs/workshop/02-modes.md#L109) | New keyboard shortcuts (v0.0.410–v0.0.412) require specific terminal capabilities: Shift+Enter needs kitty keyboard protocol; Ctrl+Z is Unix only; Page Up/Down and double/triple-click require alt-screen mode; Ctrl+Y/Ctrl+X Ctrl+E require `$EDITOR`/`$VISUAL` set. | 📅 Version-specific | done | WARNING |
| 4 | [L115](docs/workshop/02-modes.md#L115) | Shell mode removed from Shift+Tab cycle in v0.0.410 — now **only accessible via `!`** (e.g., `! ls -la`). Breaking change. | 📅 Version-specific | done | remove any shift+tab cycle for shell mode - it is no longer a feature |
| 5 | [L136](docs/workshop/02-modes.md#L136) | `/update` and `/changelog` introduced in v0.0.412. Use `/changelog` for release notes and `/update` for install instructions. | 📅 Version-specific | done | remove it - the workshop targets that version |
| 6 | [L140](docs/workshop/02-modes.md#L140) | Exercises require authentication. If "not authenticated" errors appear, set `GITHUB_TOKEN`, `GH_TOKEN`, or `COPILOT_GITHUB_TOKEN`. | 🔑 Auth | done | add a Note to authenticate before running the exercies |
| 7 | [L292](docs/workshop/02-modes.md#L292) | Always specify exact filenames in prompts for consistent results — omitting them may cause Copilot to generate varying filenames. | 💡 Prompt tip | done | make it a Tip |
| 8 | [L339](docs/workshop/02-modes.md#L339) | Avoid referencing specific line counts for short files — Copilot may reason about file length rather than run the expected command. | 💡 Prompt tip | done | make it a Tip |
| 9 | [L387](docs/workshop/02-modes.md#L387) | When piping content, use "this content"/"this file" in prompts — using "this output" may cause Copilot to say it sees no output. | 💡 Prompt tip | done | make it a Tip |

---

## Module 03 — Sessions

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 10 | [L41](docs/workshop/03-sessions.md#L41) | Session persistence behavior unclear. Each `copilot` invocation starts a **fresh session** — auto-resume behavior unverified. `--resume` flag is always required to restore a previous session. | 🐛 Bug/Unclear | done | make it clear - here are the help details: Session /resume /rename /context /usage /session /compact /share |
| 11 | [L313](docs/workshop/03-sessions.md#L313) | `--share` and `--share-gist` flags not visible in `copilot --help` for v0.0.400 — may be version-gated or preview only. | 📅 Version-specific | done | delete, we shouldn't use any version specific details |

---

## Module 04 — Instructions

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 12 | [L60](docs/workshop/04-instructions.md#L60) | Module exercises can be simulated without a live auth session (file creation only). Full testing requires auth. | 🔑 Auth | done| delete |

---

## Module 05 — Tools

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 13 | [L145](docs/workshop/05-tools.md#L145) | `--allow-tool` and `--deny-tool` flags not visible in `copilot --help` for v0.0.400 — may be version-gated. Verify with `copilot --help`. | 📅 Version-specific | done | should not write version specific |

---

## Module 06 — MCP Servers

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 14 | [L50](docs/workshop/06-mcps.md#L50) | MCP error visibility in timeline added in v0.0.410 — errors were silently ignored in earlier versions. | 📅 Version-specific | done| make it a warning |
| 15 | [L103](docs/workshop/06-mcps.md#L103) | Always validate JSON syntax in `~/.copilot/mcp-config.json` before restarting Copilot to avoid silent failures. | 💡 Tip | done| make it a tip |
| 16 | [L319](docs/workshop/06-mcps.md#L319) | `/mcp reload` added in v0.0.412 — prior versions required full session restart to pick up config changes. | 📅 Version-specific | done| delete |
| 17 | [L436](docs/workshop/06-mcps.md#L436) | Tilde `~` expansion in `cwd` field added in v0.0.410 — use `~/projects/my-server` instead of absolute paths for portability. | 📅 Version-specific | done| delete |
| 18 | [L461](docs/workshop/06-mcps.md#L461) | Duplicate callout for `/mcp reload` (v0.0.412) in Exercise 5 — consider consolidating with [L319](docs/workshop/06-mcps.md#L319). | 🧹 Cleanup | done| remove duplicate |

---

## Module 07 — Skills

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 19 | [L408](docs/workshop/07-skills.md#L408) | Exercise relies on external URL `https://agentskills.io` — verify site is live before running exercise; may need a fallback. | 🌐 External dependency | done| delete |
| 20 | [L566](docs/workshop/07-skills.md#L566) | `/skill list` command may not exist in all versions — verify with `/help` before using. | 📅 Version-specific | done| delete |

---

## Module 08 — Plugins

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 21 | [L222](docs/workshop/08-plugins.md#L222) | Code snippet uses CommonJS `require` without `module.exports` or type in `package.json` — works as-is but may confuse learners expecting explicit exports. | 🧹 Cleanup | done| make it a tip |

---

## Module 09 — Custom Agents

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 22 | [L66](docs/workshop/09-custom-agents.md#L66) | Testing agent behavior requires an authenticated session — config file creation can be done without auth, but live testing cannot. | 🔑 Auth | done| delete |

---

## Module 10 — Hooks

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 23 | [L47](docs/workshop/10-hooks.md#L47) | Hook scripts require `jq` for JSON parsing — must be installed before exercises (`apt install jq` / `brew install jq`). | 🔧 Prerequisite | done| delete |

---

## Module 11 — Context Management

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 24 | [L48](docs/workshop/11-context.md#L48) | Claude Sonnet 4.6 added in v0.0.411; GPT-5 mini deprecated in v0.0.412. Model availability varies by Copilot subscription tier. | 📅 Version-specific | done| use the flag /model select the model and then /context to see what's the context. DON'T USE VERSION SPECIFIC DETAILS update and use opus-46,  Gemini 3 Pro ,GPT-5.3-Codex  and GPT-5 mini |
| 25 | [L56](docs/workshop/11-context.md#L56) | Token usage and compaction behavior cannot be fully verified without a live authenticated session. | 🔑 Auth | done| delete |

---

## Module 12 — Advanced Topics

| # | Line | Issue | Category | Status | Notes |
|---|------|-------|----------|--------|-------|
| 26 | [L45](docs/workshop/12-advanced.md#L45) | `COPILOT_TOKEN` env var usage is unclear — may be script-local only. Prefer `GITHUB_TOKEN`, `GH_TOKEN`, or `COPILOT_GITHUB_TOKEN`. | 🐛 Bug/Unclear | done| put a Important ->  `COPILOT_GITHUB_TOKEN`, `GH_TOKEN`, `GITHUB_TOKEN` (in order of precedence): an authentication token that takes precedence over previously stored credentials.|
| 27 | [L202](docs/workshop/12-advanced.md#L202) | `--available-tools` and `--excluded-tools` may be synonyms/replacements for `--allow-tool`/`--deny-tool` — documentation inconsistency. Verify with `copilot --help`. | 🐛 Bug/Unclear | done| delete -> they aren't synonyms they are different |
| 28 | [L240](docs/workshop/12-advanced.md#L240) | Autopilot mode introduced in v0.0.411 — verify availability with `copilot --help`. | 📅 Version-specific | done| delete |
| 29 | [L324](docs/workshop/12-advanced.md#L324) | `/fleet` introduced in v0.0.411; orchestrator validation and parallel dispatch added in v0.0.412 — verify with `/help`. | 📅 Version-specific | done| delete |
| 30 | [L434](docs/workshop/12-advanced.md#L434) | `--bash-env` flag introduced in v0.0.412; shell mode `!`-only access change from v0.0.410. Verify with `copilot --help`. | 📅 Version-specific | done| delete |
| 31 | [L531](docs/workshop/12-advanced.md#L531) | LSP timeout configuration via `lsp.json` added in v0.0.412 — advanced users only. | 📅 Version-specific | done| delete |
| 32 | [L709](docs/workshop/12-advanced.md#L709) | General troubleshooting note: flag availability varies by version — always cross-check with `copilot --version` and `--help`. | 💡 Tip | done| delete |

---

## Summary by Category

| Category | Count |
|----------|-------|
| 📅 Version-specific | 15 |
| 🔑 Auth | 6 |
| 💡 Prompt tip / Tip | 5 |
| 🐛 Bug/Unclear | 3 |
| 🧹 Cleanup | 2 |
| 🌐 External dependency | 1 |
| 🔧 Prerequisite | 1 |
| **Total** | **32** |

---

## High Priority Items

1. **#10 (Module 03 L41)** — Session auto-resume behavior is unclear and may mislead learners. Needs clarification or a test.
2. **#26 (Module 12 L45)** — `COPILOT_TOKEN` env var undocumented — could cause auth failures for learners.
3. **#27 (Module 12 L202)** — Tool flag naming inconsistency (`--available-tools` vs `--allow-tool`) — could break exercises.
4. **#18 (Module 06 L461)** — Duplicate `/mcp reload` callout — consolidate to reduce noise.
5. **#19 (Module 07 L408)** — External dependency `agentskills.io` — single point of failure for an exercise; needs a fallback.





USE THIS TO APPLY THE NOTES

> [!NOTE]
> This is a note block.


> [!WARNING]
> This is a warning block.


> [!TIP]
> This is a tip block.


> [!IMPORTANT]
> Something critical goes here.
