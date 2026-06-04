# Knowledgeworker Create Skills

Creating learning content with AI is a powerful way to reduce the time it takes to apply new knowledge throughout your extended enterprise. This repository contains a growing collection of skills that can be used to create and work with learning content with [Knowledgeworker Create](https://www.knowledgeworker.com) using your preferred AI agent.

## Skills

Available skills:

| Skill                                                                     | Description                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Knowledgeworker Create Embedded Assets](skills/embedded-assets/SKILL.md) | Create or modify an embedded asset (HTML5 medium/custom media asset); or create or modify a custom question (HTML5 question). |


## Recommended installation

Install skills with the [skills.sh](https://www.skills.sh/) CLI. It installs skills from this GitHub repository and guides you through skill, agent, and scope selection for supported agents such as Codex, Claude Code, Gemini CLI, Cursor, and others.

```shell
npx skills add chemmedia/knowledgeworker-create-skills
```

To install globally for a specific agent without prompts, pass the agent explicitly:

```shell
npx skills add chemmedia/knowledgeworker-create-skills --agent codex --global --yes
```

To inspect the available skills before installing:

```shell
npx skills add chemmedia/knowledgeworker-create-skills --list
```

## Agent-specific installation

Use the following commands only if you need an agent-specific plugin flow or the `skills` CLI does not support your local setup.

### Claude Code

Install marketplace in Claude Code CLI:

```shell
/plugin marketplace add chemmedia/knowledgeworker-create-skills
/plugin install knowledgeworker-create@knowledgeworker-create
```

### Codex CLI

In your terminal, run:

```shell
codex plugin marketplace add chemmedia/knowledgeworker-create-skills
codex plugin add knowledgeworker-create@knowledgeworker-create
```

## Learn more
- [Knowledgeworker Create](https://www.knowledgeworker.com/)
