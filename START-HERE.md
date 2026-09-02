# Start here: prepare Codex for Computer Use

Complete this setup before installing any workshop skill. Codex must already be installed and able to control the Mac before it can install other applications or execute the workflows in this repository.

Allow about 10 minutes. Stay at the Mac because macOS permission changes, authentication, and restarts require a person.

## 1. Install Codex manually

1. Download and install the official ChatGPT desktop app for macOS from the [OpenAI quickstart](https://learn.chatgpt.com/docs/quickstart).
2. Open the app and sign in with the attendee's own ChatGPT account.
3. Select **Codex** from the ChatGPT/Codex switcher.
4. Open or create a local folder for the workshop when prompted.

Codex cannot perform this first installation for itself.

## 2. Select the workshop runtime

In the Codex task controls, select:

- Model: **5.6 Sol** (`gpt-5.6-sol`)
- Reasoning: **Medium**
- Processing: **Fast mode**

If Fast mode is unavailable for the attendee's account or app version, continue on the available processing tier. Do not confuse Medium reasoning with processing speed.

GPT-5.6 Sol supports Computer Use. See the [official model page](https://developers.openai.com/api/docs/models/gpt-5.6-sol).

## 3. Install and enable Computer Use

1. Open **Plugins** in the desktop app.
2. Open **Computer Use**.
3. Select **Install plugin** if shown.
4. Select **Enable** if shown.
5. Turn on both the **Computer Use server** and **Computer Use skill** toggles.
6. Select **Try now**.

See the [official Computer Use setup](https://learn.chatgpt.com/docs/computer-use).

## 4. Grant the required macOS permissions

When macOS prompts, the attendee must personally grant:

- **Screen Recording** so Computer Use can see app windows.
- **Accessibility** so Computer Use can click, type, and navigate.

If Codex still cannot see or control an app, open **System Settings → Privacy & Security** and verify that **Codex Computer Use** is enabled under both **Screen Recording** and **Accessibility**. Quit and reopen the desktop app if macOS requests it.

These system permissions are separate from Codex's app approvals. Full Disk Access is not a standard Computer Use requirement and should not be enabled unless a specific approved task explains why it needs it. Other permissions are task-specific—for example, Wispr Flow requires Microphone access for dictation.

## 5. Configure app access

1. In the desktop app, open **Settings → Computer use**.
2. Confirm that Computer Use control is enabled.
3. During a task, approve each application Codex needs to operate.
4. Choose **Always allow** only for trusted workshop applications that the attendee expects Codex to use repeatedly, such as System Settings, Finder, Slack, Wispr Flow, or the attendee's chosen browser.

App approvals can be reviewed or removed later from **Settings → Computer use → Always-allowed apps**.

## 6. Run the readiness test

Start a new Codex task and send:

> Use Computer Use to open System Settings, identify the visible settings category, and return to Codex without changing any setting. Tell me whether Screen Recording, Accessibility, the Computer Use server, and the Computer Use skill are ready. Stop if any permission is missing.

The Mac is ready when Codex can:

- Start Computer Use without an installation error.
- See the System Settings window.
- Open it and navigate using named controls.
- Return without changing a setting.

If the test fails, recheck **Plugins → Computer Use**, **Settings → Computer use**, and the two macOS permissions before proceeding.

## 7. Install and run a workshop skill

1. Return to the [skill catalog](README.md#skill-catalog).
2. Open the desired `SKILL.md` and download it, or download this repository as a ZIP.
3. Attach that `SKILL.md` to a new Codex task.
4. Send:

   > Install the attached Markdown file as a Codex skill, validate it, and execute it from start to finish using Computer Use. Pause when you need me for authentication, permissions, personal information, physical actions, or final submission.

5. Complete human handoffs for passwords, Touch ID, passkeys, one-time codes, CAPTCHAs, macOS permissions, and physical hardware actions. Do not paste credentials into the task.

