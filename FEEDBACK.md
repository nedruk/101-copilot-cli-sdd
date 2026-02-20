# Workshop Feedback

This file documents incongruences, errors, typos, or confusing parts encountered during the workshop.

## Resolved

The following issues have been addressed with inline `⚠️ **FEEDBACK**` notes in the relevant modules:

- ✅ Module 1: Programmatic authentication for CI/CD environments
- ✅ Module 1: Container/CI authentication troubleshooting
- ✅ Module 2: Auth requirement warning
- ✅ Module 2: Exercise prompt clarity (filename, line count, pipe wording)
- ✅ Module 3: Session persistence clarification
- ✅ Module 3: `--share`/`--share-gist` version availability
- ✅ Module 5: `--allow-tool`/`--deny-tool` version availability
- ✅ Module 7: agentskills.io external URL dependency
- ✅ Module 7: `/skill list` command availability
- ✅ Module 12: `COPILOT_TOKEN` vs standard env vars clarification
- ✅ Module 12: `--available-tools`/`--excluded-tools` flag consistency
- ✅ Module 12: Autopilot mode section (v0.0.411 feature) with feedback callout
- ✅ Module 12: Fleet command section (v0.0.411-v0.0.412 features) with feedback callout
- ✅ Module 12: `--bash-env` flag documentation (v0.0.412 feature) with feedback callout
- ✅ Module 12: LSP timeout configuration via `lsp.json` (v0.0.412 feature) with feedback callout
- ✅ Module 12: Shell mode access change documentation (v0.0.410 change)

## Open Items

None - all identified issues have been addressed.

## Recent Changes

- ✅ Version bump: Workshop updated from v0.0.405 to v0.0.409
- ✅ Module 4: Added `/instructions` command section (v0.0.407 feature) with feedback callout
- ✅ Index: Added `/instructions` to slash commands quick reference table
- ✅ README: Expanded SDD acronym, added Dev Container guidance, reframed install options as alternatives
- ✅ Module 1: Added container/CI auth troubleshooting section and table row
- ✅ Module 2 Ex4: Specified filename (`hello.py`) in prompt to reduce randomness across participants
- ✅ Module 2 Ex5: Replaced "first 10 lines" prompt with explicit `cat` command to avoid Copilot confusion
- ✅ Module 2 Ex6: Fixed piped input prompt wording ("Explain what this file contains" vs "Explain this output")
- ✅ Module 2: Added comprehensive "Slash Commands" section covering all 30+ `/command` features, keyboard shortcuts, command categories, and 3 new exercises (`/plan`, `/review`, `/diff`, `/init`, `/rename`, `/tasks`, `/theme`, `/terminal-setup`, `/lsp`, `/user`). Module renamed to "Operating Modes & Commands" with updated duration (30 min).
- ✅ **Module 12 Update (v0.0.410-v0.0.412)**: Added 4 new exercises covering:
  - **Exercise 4**: Autopilot Mode (v0.0.411) - autonomous multi-step task execution
  - **Exercise 5**: Fleet Command (v0.0.411-v0.0.412) - parallel sub-agents with orchestrator validation and parallel dispatch
  - **Exercise 6**: Advanced Shell Configuration (v0.0.410, v0.0.412) - `--bash-env` flag and shell mode access changes
  - **Exercise 7**: LSP Configuration (v0.0.412) - `lsp.json` for language server timeout control
  - Updated configuration reference tables with version information
  - Renumbered remaining exercises (8-11)
  - Updated workshop duration from 20min to 30min
  - Updated index to reflect new features and learning objectives

## Summary

The workshop content provides a thorough deep dive into the GitHub Copilot CLI, covering installation, basic usage, configuration, and advanced customization via MCP, skills, agents, and hooks.

**Positive Aspects:**
1. **Structure:** Logical progression from basics to advanced topics.
2. **Practicality:** Hands-on exercises are well-designed.
3. **Advanced Features:** Coverage of MCP, custom agents, and hooks demonstrates powerful extensibility.
4. **Inline Warnings:** Version-specific features are now clearly marked with feedback callouts.
