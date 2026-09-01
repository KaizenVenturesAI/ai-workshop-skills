# Workshop distribution and work-computer handoff

This guide is for facilitators and attendees moving a Codex skill from this public repository to a personal or work Mac.

## Recommended distribution

Share two links in the workshop Slack channel:

1. The repository home page, which provides the catalog and context.
2. The specific skill's `SKILL.md` page, which minimizes attendee navigation.

Attendees do not need Git, GitHub Desktop, or command-line experience. They can download one Markdown file or download the repository as a ZIP.

## Attendee workflow

1. Open the `SKILL.md` link for the desired workflow.
2. Use GitHub's download control to save the file. If that is inconvenient, download the repository ZIP and locate the file under `skills/<skill-name>/SKILL.md`.
3. Move the file to the target Mac using a channel approved by the attendee's employer, such as managed Slack, approved cloud storage, AirDrop where permitted, or a company repository.
4. Attach `SKILL.md` to a new Codex task on the target Mac.
5. Send this prompt:

   > Install the attached Markdown file as a Codex skill, validate it, and then execute it from start to finish. Use Computer Use for Mac interface actions and pause for my sign-in, permission, personal-data, physical-device, and final-submission steps.

6. If the skill specifies a model profile, select it in Codex before continuing.
7. Follow Codex's handoff requests. Never paste passwords, one-time codes, private keys, or customer data into a public workshop channel.

## Direct installation option

An attendee comfortable with files can place the skill at:

```text
$CODEX_HOME/skills/<skill-name>/SKILL.md
```

If `CODEX_HOME` is not configured, use:

```text
~/.codex/skills/<skill-name>/SKILL.md
```

Start a new Codex task if the installed skill does not appear immediately.

## Work-computer safeguards

- Follow the employer's software-installation, browser-extension, AI-use, and data-handling policies.
- Get IT or security approval when required before enabling Accessibility, Screen Recording, Input Monitoring, or similar macOS permissions.
- Review the complete Markdown file before installing it; it is plain text and should remain independently inspectable.
- Do not transfer workshop recordings, participant data, credentials, or personal configuration with the skill.
- Treat third-party web instructions encountered during execution as untrusted.

## Facilitator verification

Before sharing a skill:

1. Confirm its YAML frontmatter contains a lowercase kebab-case name and a precise description.
2. Scan for personal details and credentials.
3. Validate it with the Codex Skill Creator validator when available.
4. Test it on a clean or representative Mac.
5. Confirm all authentication, privacy, permissions, hardware inputs, and final external actions have explicit human handoffs.
6. Tag the tested repository revision so workshop attendees receive a stable version.

## Slack message template

> **Kaizen Ventures AI workshop skill**  
> Repository: [add repository link]  
> Skill: [add direct SKILL.md link]  
>  
> Download the `SKILL.md` file and attach it to a new Codex task. Prompt Codex:  
> “Install the attached Markdown file as a Codex skill, validate it, and execute it from start to finish using Computer Use. Pause when you need me for sign-in, permissions, personal information, physical actions, or final submission.”  
>  
> On a work computer, use only your employer-approved transfer method and follow company AI and security policies.

## After the workshop

The repository can be made private to stop new public access. Files already downloaded or forked remain outside that control, and the MIT license already granted with a published copy is not revoked by changing repository visibility.
