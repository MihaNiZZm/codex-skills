# Missing skill protocol

Check the catalog and verified installed skill roots first. Read an installed SKILL.md even if discovery has not refreshed. Report exact missing names; do not silently substitute similar skills or pretend invocation succeeded.

Give the user a concrete path:

1. If `skill-installer` is available, use it to discover whether the named skill is in the actual curated list. Install the verified entry when authorized.
2. For a verified GitHub source, use the installer's supported command, resolving its installed directory first:
   `python3 <skill-installer-directory>/scripts/install-skill-from-github.py --repo <verified-owner/repo> --path <verified-skill-directory> --ref <verified-ref>`
   Replace placeholders only with verified values. Do not invent a repository URL or claim a skill is curated without checking.
3. If the source is unknown, say so and ask for the trusted repository/path or local skill bundle. Explain that installation goes to `$CODEX_HOME/skills` (normally `~/.codex/skills`) and discovery may require a new turn/session. If no installer exists, a trusted bundle can be placed there as `<name>/SKILL.md` with its referenced files, then validated with the installed skill-creator validator if available.

State which action depends on the missing skill and which preparation can continue. Installation is not permission to execute the downstream product operation. Optional skills are required only when the selected role/task uses them.
