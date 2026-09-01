---
name: setup-wispr-flow-mx-vertical
description: Install and configure Wispr Flow on any supported Mac, then bind a Logitech MX Vertical button to Push to talk, Hands-free mode, or a Transform and verify it end to end. Use for workshop onboarding, first-time setup, reassignment, or troubleshooting. Prefer Wispr Flow's native mouse capture over Logi Options+.
---

# Set Up Wispr Flow with a Logitech MX Vertical

Complete this workflow with Computer Use. Do not stop after describing the steps. Guide the user through unavoidable physical actions and permission prompts, then resume and verify the result.

This skill is portable across supported Mac mini, Mac Studio, MacBook Air, MacBook Pro, iMac, and other macOS hardware. Navigate by current UI labels rather than device model or fixed screen coordinates.

## Workshop bootstrap

When this Markdown file is attached or pasted into Codex and the skill is not installed:

1. Save this entire file as `setup-wispr-flow-mx-vertical/SKILL.md` inside the user's Codex skills directory. Prefer `$CODEX_HOME/skills` when configured; otherwise use `~/.codex/skills`.
2. Keep normal automatic skill discovery enabled.
3. Validate the installed skill with the available Skill Creator validator when present.
4. Continue directly into the execution workflow below. Do not finish after installation or return only a runbook.

If filesystem access is unavailable, use this file as the live operating procedure and tell the user the skill could not be persisted.

## Required Codex runtime profile

Before changing the Mac, verify that the current task is running with:

- Model: `gpt-5.6-sol` (shown in the Codex picker as **5.6 Sol**)
- Reasoning effort: **Medium**
- Processing: **Fast mode** (the fast/priority service tier)

Do not claim to have changed the model or processing tier when the active task cannot change its own runtime. If any setting is unavailable or mismatched, pause and ask the user to select **5.6 Sol**, **Medium**, and **Fast**, then tell them to reply **Continue**. Resume from the current step after they do.

Medium is the reasoning setting, not a speed setting. Fast is the processing mode. Availability can depend on the attendee's account and Codex version; if Fast mode is unavailable, explain that plainly and ask whether to continue on the available tier.

Official references:

- [GPT-5.6 Sol model](https://developers.openai.com/api/docs/models/gpt-5.6-sol)
- [Fast mode service tier](https://developers.openai.com/api/reference/cli/resources/responses/methods/create)

## Desired outcome

Finish only when all applicable checks pass:

- Wispr Flow is installed, running, and signed in.
- The MX Vertical is connected and its normal pointer movement works.
- Required macOS permissions are enabled.
- Wispr Flow recognizes the chosen physical button, for example as `Mouse 4`.
- The requested dictation mode or Transform is assigned.
- A harmless live test succeeds.
- The user knows which physical button was bound and how to operate it.

## Inputs

Determine these from the request or ask concise questions only when needed:

- Physical MX Vertical button to bind. The demonstrated choice was the forward thumb button, detected as `Mouse 4`.
- Action: `Push to talk`, `Hands-free mode`, or a named Transform such as `Polish`.

If the user has not chosen an action, recommend **Push to talk** for a first workshop setup. Explain that it records only while the button is held; **Hands-free mode** toggles dictation on and off. Do not overwrite an existing shortcut without showing the conflict and receiving the user's choice.

## Execution workflow

### 1. Preflight

1. Use Computer Use to inspect the current Mac and Wispr Flow state.
2. Confirm the MX Vertical is connected by Bluetooth or its USB receiver and that pointer movement works. Ask the user to connect or test the physical device when necessary.
3. Check whether Wispr Flow is installed.
4. If it is missing, offer to download it from the official Wispr Flow source. Obtain action-time confirmation before installing or running newly downloaded software.
5. Open Wispr Flow. Hand off sign-in, password, passkey, and one-time-code steps to the user, then resume.

### 2. Permissions

Wispr Flow may require Microphone, Accessibility, and sometimes Input Monitoring permissions.

1. Navigate to the relevant prompt or macOS System Settings pane.
2. Pause immediately before changing a macOS privacy or security setting and ask the user to approve it themselves.
3. Relaunch Wispr Flow if macOS or the app requests it.
4. Re-inspect the app and confirm no required permission remains blocked.

### 3. Native MX Vertical onboarding

Use Wispr Flow's native mouse-button capture first; Logi Options+ is not required for the demonstrated workflow.

1. In Wispr Flow, open **Settings**.
2. Under **General**, find **Shortcuts** and choose **Change**.
3. If the **Introducing: Mouse Shortcuts** banner is present, choose **Set it up**.
4. Follow the visible onboarding until Wispr Flow requests a key or mouse button.
5. Ask the user to press the chosen physical MX Vertical button once. Do not simulate or guess this hardware input.
6. Choose **Done** when appropriate.
7. Verify **Mouse Flow setup complete!** if that confirmation is present.

### 4A. Assign Push to talk or Hands-free mode

1. Open **Settings** → **General** → **Shortcuts** → **Change**.
2. Under the requested mode, choose **Add another** or the current shortcut control.
3. Wait until the UI says **Press key or mouse button**.
4. Ask the user to press the desired MX Vertical button once.
5. Confirm Wispr Flow displays the detected name, such as **Mouse 4**.
6. Choose **Done** and verify the assignment remains visible.

### 4B. Assign a Transform

The recorded example assigned **Mouse 4** to **Polish**.

1. Select **Transforms** in the Wispr Flow sidebar.
2. Open the requested Transform.
3. Under **Choose a keyboard shortcut**, select the existing shortcut control.
4. Wait until the UI says **Press key or mouse button**.
5. Ask the user to press the desired physical button once.
6. Verify **Shortcut saved** and confirm the Transform card shows the detected button name.

### 5. Verify end to end

1. Open a harmless blank text field, such as a new note or Wispr Flow's scratchpad.
2. Ask the user to perform the physical action:
   - **Push to talk:** hold the button, speak a short sentence, then release.
   - **Hands-free mode:** press once, speak, then press again.
   - **Transform:** dictate or select a short sample, then press the assigned button.
3. Confirm the expected text appears or the requested Transform runs.
4. If the first test fails, inspect the current app state and troubleshoot before retrying. Stop after two unchanged failures and report the exact blocker instead of looping.
5. Finish with a concise handoff naming the physical button, Wispr Flow's detected button name, assigned action, and successful test.

## Troubleshooting

- **Button is not detected:** Reopen shortcut capture and press the physical button only after **Press key or mouse button** appears.
- **Button triggers another action:** Inspect Wispr Flow and Logi Options+ for a conflicting mapping. Change only the conflicting per-app mapping after showing it to the user.
- **Nothing happens:** Recheck Microphone and Accessibility permissions, then relaunch Wispr Flow.
- **Button name is not Mouse 4:** Accept the name Wispr Flow reports; numbering varies by button and system mapping.
- **UI differs from this guide:** Find the semantic equivalents of **Settings**, **Shortcuts**, **Push to talk**, **Hands-free mode**, and **Transforms**. Refresh Computer Use state after every action and never reuse stale element indexes.
- **Mac hardware differs:** Treat the Mac model as irrelevant unless the macOS version or available ports affect connection. Bluetooth and receiver-based setups follow the same Wispr Flow assignment flow after the mouse is connected.

## Boundaries

- Do not expose, record, or copy passwords, authentication codes, or personal Wispr Flow content.
- Do not modify snippets, style rules, microphone choice, language settings, or unrelated Transforms.
- Do not replace existing shortcuts without explicit user direction.
- Use stable accessibility labels before coordinates and re-inspect the UI after each action.
