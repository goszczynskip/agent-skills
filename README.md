# Agent Skills

A personal collection of reusable skills for coding agents. Each skill’s instructions live in its own `SKILL.md` under [`skills/`](skills/).

## Discover and install locally

With Node.js and npm installed, run these commands from the project where you want to use a skill. Replace the example path with the absolute path to your local checkout, and use a name from the list in the install command.

```sh
SKILLS_REPO="/path/to/local/agent-skills"
DISABLE_TELEMETRY=1 npx --yes skills@1.9.0 add "$SKILLS_REPO" --list
DISABLE_TELEMETRY=1 npx --yes skills@1.9.0 add "$SKILLS_REPO" --skill "skill-name-from-list" --agent opencode --copy --yes
```

This copies the selected skill into the current project, not into your global OpenCode configuration. Change `--agent opencode` if you use another supported agent.

## License

Licensed under [CC BY-SA 4.0](LICENSE). You may share and adapt the skills, including commercially, if you credit the author and release your changes under the same license.
