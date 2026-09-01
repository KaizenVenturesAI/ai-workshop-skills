---
name: slack-add-single-channel-guest
description: Use Computer Use to navigate from the Slack desktop app to Workspace Admin and invite a person as a guest limited to exactly one channel. Use for a human-in-the-loop Slack guest invitation; do not use for full members or multi-channel guests.
---

# Add a Slack Single-Channel Guest

Use the Computer Use skill for every UI action. This is a guided human-in-the-loop workflow: automate navigation and routine clicks, but stop for authentication, personal information, channel selection, and final approval.

## Preconditions

- Computer Use must be installed and enabled with Screen Recording and Accessibility access.
- The user must be a Slack Workspace Owner or Admin, or otherwise have permission to invite guests.
- Ask which Slack workspace to use if more than one is visible or the intended workspace is unclear.
- Do not reuse names, email addresses, workspaces, or channels from earlier demonstrations.

If Computer Use is unavailable, stop and explain how to enable it. Do not replace this exercise with manual instructions or a Slack API workflow because the workshop objective is to execute the demonstrated UI path.

## Phase 1: Navigate from the desktop

1. Initialize Computer Use and inspect **Slack** directly. Do not ask the user to launch it first.
2. If Slack is signed out, on a workspace picker, or presents SSO, a password field, CAPTCHA, or two-factor authentication, stop and hand control to the user. Ask them to authenticate privately and tell you when the intended workspace is open. Never request, view, or enter credentials or one-time codes.
3. After the user returns, inspect Slack again and verify the intended workspace.
4. Open the user's profile menu and choose **Account Settings**. Slack may open this page in Google Chrome.
5. Inspect **Google Chrome** and navigate through **People → Members** to **Manage members**. Use the named accessibility controls visible in the current state; reacquire state after every navigation and never reuse recorded element indexes or screen coordinates.
6. Select **Invite People**.

If the labels have changed, use the closest semantically equivalent Slack controls. Stop if the current screen cannot be identified confidently.

## Phase 2: Human enters the guest details

When the invitation dialog is ready, stop and hand control to the user. Ask them to:

1. State the intended guest's full name in chat so the final confirmation can identify the person. Slack may not provide a name field at invitation time.
2. Enter the guest's email address into **Email addresses** themselves.
3. Choose **Invite as guests or external partners** and select **Guest**.
4. Select exactly one channel under **Add to channels**.
5. Leave **Allow them to be added to more channels** unchecked.
6. Choose an expiration only if they want one; otherwise keep **No limit**.
7. Return control and say the form is ready without clicking **Send**.

Do not type the email address or choose the channel on the user's behalf. These are deliberate workshop handoff points.

## Phase 3: Validate and send

1. Inspect the current Slack invitation form after the user returns.
2. Verify all of the following before proceeding:
   - Invite type is **Guest**.
   - Exactly one channel is selected.
   - **Allow them to be added to more channels** is unchecked.
   - The **Send** control has not already been activated.
3. If an email address is visible, use it only to check whether the invitation is internally consistent. Mask it in any summary or confirmation.
4. If any condition is wrong or uncertain, explain the problem and hand control back to the user to correct it.
5. Immediately before clicking **Send**, ask for action-time confirmation. State the guest's name, masked email if visible, workspace, selected channel, expiration, and that sending will email an invitation and grant access to that Slack channel.
6. Only after the user confirms, click **Send**. Then select **Done** if Slack shows a completion dialog.

## Phase 4: Verify

Return to **Manage members** and search for the invited email if the user provides it again or it remains safely available in the UI. Verify a pending status such as **Invited Guest** or an equivalent inactive guest row.

A pending invitation may not display **Single-Channel Guest** until accepted. The one selected channel and the unchecked multi-channel option are the important access controls at invitation time. Do not claim the guest accepted or joined unless Slack visibly confirms it.

Report the workspace, guest name, masked email, selected channel, expiration, and pending/sent status. If Slack reports a plan limit, permission problem, duplicate member, or guest allowance issue, stop and report it; never silently convert the person to a regular member.
