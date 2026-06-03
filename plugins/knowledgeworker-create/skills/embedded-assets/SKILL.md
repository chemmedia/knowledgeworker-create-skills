---
name: embedded-asset
description: >
  Tutorial for creation of Knowledgeworker Create embedded assets. Use when user says "Create package asset", "build HTML5 content", "create custom question", or invokes /embedded-asset.
license: MIT
metadata:
  author: chemmedia AG
  version: "0.0.1"
---

# Knowledgeworker Create Embedded Asset Skill

Embedded assets are HTML5 content packages embedded into [Knowledgeworker Create](https://www.knowledgeworker.com) courses via iframe. The `knowledgeworker-embedded-asset-api` npm package handles communication between the asset and the course runtime.

Full API reference, types, and examples: **https://github.com/chemmedia/knowledgeworker-embedded-asset-api**

A working example project showing a complete embedded asset implementation: **https://github.com/chemmedia/knowledgeworker-embedded-asset-api-example**

UI integration (CSS variables, pre-styled classes, and JS access to design tokens that stay in sync with the course theme): **https://github.com/chemmedia/knowledgeworker-embedded-asset-api-ui** — bundled with `knowledgeworker-embedded-asset-api` by default, no separate install needed.

## When to use this skill

- Create or modify an embedded asset, HTML5 medium, or custom media asset
- Create or modify a custom question or HTML5 question

## Asset types

| Type | Description |
|------|-------------|
| `medium` | Standalone content; triggers completion |
| `question` | Question with LMS-evaluated answer |
| `question-with-custom-question-text` | Question where the asset renders the question text |
| `advanced-question` | Question with full UI control (check/retry/solution buttons) |

The asset type is received in the `onInitialize` event handler and determines which actions and event handlers are relevant.

## Key concepts

- **Actions** — functions the asset calls to send data to the runtime (e.g. `completed()`, `answered()`, `setSuspendData()`)
- **Event handlers** — callbacks the runtime calls to push state into the asset (e.g. `onInitialize`, `onShowResult`, `onReset`)
- **Suspend data** — arbitrary string persisted between sessions, restored via `onInitialize`
- **Auto completion** — by default the runtime marks the asset complete after load; set `autoCompletion: false` in `configure()` to trigger it manually via `completed()`

When implementing, read the GitHub repo to get the exact API signatures, `Configuration` type, and usage examples.
