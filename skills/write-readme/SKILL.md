---
name: write-readme
description: Write, rewrite, simplify, or review a repository README. Use when asked to create or clean up a README, fix stale setup or quickstart instructions, or make a project easier to understand and run from a fresh checkout.
license: CC-BY-SA-4.0
---

# Write a maintainable README

Treat the README as an entry point, not a second configuration file. Explain what the project is for and how the intended reader can get started. Refer readers to the files that own the details.

## Workflow

1. **Identify the reader and their first task.** A public library may need a minimal usage example; a personal configuration repo may only need setup and a check command. Match the repository's language and tone unless the user asks otherwise.
2. **Verify the current repository.** Read the existing README and the relevant tracked files or pending changes: manifests, scripts, configuration, lockfiles, CI, and license. Don't assume local ignored files, old documentation, or generated artifacts exist on a fresh checkout.
3. **Write the shortest working path.** Give the project one clear purpose statement. Then show the prerequisites, working directory, and commands needed for the first useful result. Add usage, checks, troubleshooting, or license information only when they help this reader. Distinguish required steps from optional ones.
4. **Prefer links over inventories.** Link to the manifest for dependencies, the lockfile for pinned versions, the config for integrations, and the script for the actual workflow. Keep one canonical command or a representative example where it helps someone act. A deliberate example is fine; a list presented as the current truth will drift.
5. **Verify before handing it back.** Confirm relative links resolve and commands exist. Where practical, try the documented path in a clean checkout or a temporary directory. Say what you didn't run. Don't execute commands that deploy, delete data, or require credentials just to validate the README.

## Review for loose coupling

Ask: **If someone adds a dependency, switches a default, or replaces an integration without changing the reader's workflow, does this README have to change?** If yes, link to the source of truth or describe the stable operation instead.

| Avoid | Prefer |
| --- | --- |
| “Install `foo` and `bar`” when a lockfile decides the set | “Restore dependencies from the lockfile,” with the restore command |
| An inventory of current themes, integrations, or internal folders | A short purpose statement and links to the relevant configuration |
| A hand-maintained copy of a build or validation procedure | The canonical build or check command from the project |

Keep details that are part of the reader-facing contract: real prerequisites, the supported entry point, and anything needed for the example to work. Don't turn a useful quickstart into a chain of links. Remove stale commands, empty sections, and boilerplate the repository doesn't need.
