# Kaizen Ventures AI Workshop Skills

Open-source, reusable Codex skills for Kaizen Ventures AI workshops and practical Mac onboarding.

Each skill is self-contained: download its `SKILL.md`, attach it to a Codex task, and ask Codex to install and execute it. The skills are written to guide attendees through unavoidable sign-in, permission, and hardware steps while automating the rest with Computer Use.

## New Mac? Start here

Codex and Computer Use must be installed and configured before these skills can control the Mac. First-time attendees should complete [Start here: prepare Codex for Computer Use](START-HERE.md), including the Screen Recording and Accessibility permissions and the readiness test, before choosing a skill.

## Skill catalog

| Skill | What it does | File |
|---|---|---|
| Wispr Flow + Logitech MX Vertical | Installs and configures Wispr Flow, binds an MX Vertical button, and verifies dictation or a Transform. | [SKILL.md](skills/setup-wispr-flow-mx-vertical/SKILL.md) |
| Slack single-channel guest | Guides a Slack admin through inviting one guest to exactly one channel with deliberate privacy and send-confirmation handoffs. | [SKILL.md](skills/slack-add-single-channel-guest/SKILL.md) |
| Onboard your Mac | Audits and personalizes a new Mac, installs approved AI/work tools, configures approved settings, and verifies the result. | [SKILL.md](skills/onboard-your-mac/SKILL.md) |
| General AI onboarding | Planned: a product-independent orientation and workspace handoff workflow. | Coming soon |

Suggested Codex prompt:

> Install the attached Markdown file as a Codex skill. Verify that this task is using GPT-5.6 Sol with Medium reasoning and Fast mode, then execute the skill from start to finish using Computer Use.

## Fastest workshop workflow

1. On a new Mac, complete the [Codex and Computer Use setup](START-HERE.md).
2. Open the relevant skill link in the catalog.
3. Download `SKILL.md`, or download this repository as a ZIP.
4. Attach `SKILL.md` to a new Codex task.
5. Paste the suggested prompt.
6. Follow Codex's handoff requests for sign-in, macOS permissions, and physical mouse-button presses.

The attendee does not need to clone the repository or use Git from the command line.

For moving a skill to a managed work computer, facilitator instructions, verification, and copy-ready Slack messages, see [Workshop distribution and work-computer handoff](docs/workshop-distribution.md).

## Repository structure

```text
skills/
  onboard-your-mac/
    SKILL.md
  slack-add-single-channel-guest/
    SKILL.md
  setup-wispr-flow-mx-vertical/
    SKILL.md
```

Add future workshop skills as separate kebab-case folders beneath `skills/`. Keep each skill independently downloadable and avoid including passwords, account data, recordings, or participant information.

## Contributing

Issues and pull requests are welcome. Before submitting a skill:

- Remove personal or customer-specific information.
- Keep frontmatter names lowercase and kebab-case.
- Test the workflow on a clean or representative Mac.
- Verify permission prompts and physical handoffs are explicit.
- Validate the skill with the Codex Skill Creator validator when available.

## License

Released under the [MIT License](LICENSE).

Changing this repository to private later prevents new public access but does not revoke copies or MIT permissions already received.
