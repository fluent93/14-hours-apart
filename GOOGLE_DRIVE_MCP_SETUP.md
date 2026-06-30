# Google Drive MCP Setup

This project can use Google Drive as the source-writing space and GitHub as the structured project memory.

## Intended Flow

1. Draft original episodes in Google Docs.
2. Codex reads selected Google Docs through the `gdrive` MCP server.
3. Codex converts each episode into:
   - `01_raw_episodes/001_*.md`
   - `02_scene_cards/001_*.md`
   - outline placement notes in `03_outline/chapter_outline.md`
4. Codex commits the structured files to GitHub.

## Current Codex MCP Registration

A global Codex MCP server named `gdrive` is registered on this machine.

It uses:

```bash
npx -y @modelcontextprotocol/server-gdrive
```

Credential paths:

```bash
/home/ubuntu/.config/codex-gdrive/gcp-oauth.keys.json
/home/ubuntu/.config/codex-gdrive/credentials.json
```

Do not commit either credential file to GitHub.

## Google Cloud Setup

In Google Cloud Console:

1. Create or select a Google Cloud project.
2. Enable the Google Drive API.
3. Configure the OAuth consent screen.
4. Add OAuth scope:

```text
https://www.googleapis.com/auth/drive.readonly
```

5. Create an OAuth Client ID.
6. Application type: Desktop App.
7. Download the OAuth client JSON.
8. Put it here:

```bash
/home/ubuntu/.config/codex-gdrive/gcp-oauth.keys.json
```

## Authenticate The Drive MCP Server

After the OAuth JSON exists, run:

```bash
GDRIVE_OAUTH_PATH=/home/ubuntu/.config/codex-gdrive/gcp-oauth.keys.json GDRIVE_CREDENTIALS_PATH=/home/ubuntu/.config/codex-gdrive/credentials.json npx -y @modelcontextprotocol/server-gdrive auth
```

The command prints or opens a Google authorization flow. Sign in with the Google account that owns the project Docs and approve read-only Drive access.

After authentication, the server writes:

```bash
/home/ubuntu/.config/codex-gdrive/credentials.json
```

## Verify In Codex

Check registration:

```bash
codex mcp get gdrive
```

Restart Codex after adding or authenticating the MCP server so the tool list refreshes.

Then ask Codex to search Drive for a known episode document title.

## Safety Rules

- Keep OAuth files outside the Git repository.
- Prefer a dedicated Google Drive folder named `14-hours-apart`.
- Keep raw private memories in Google Docs until fictionalized.
- Commit only cleaned Markdown, scene cards, outlines, drafts, and market package files.
- Use read-only Drive scope unless there is a deliberate reason to let Codex write to Drive.
