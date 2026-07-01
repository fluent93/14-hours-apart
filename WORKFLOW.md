# Working Workflow

## Recommended Method

Use Google Docs for first-pass episode writing and human revision, then move the cleaned/canonical version into this repository as Markdown.

This keeps the writing process comfortable while making the project folder the long-term memory.

## Why Google Docs First

Google Docs is best for:

- writing from anywhere
- quick emotional drafting
- comments and questions
- sharing one episode at a time
- keeping a natural writing surface separate from structural files

## Why Markdown In The Repository

The repository is best for:

- project bible continuity
- scene cards
- outline placement
- privacy notes
- version history
- KDP package files
- preventing important decisions from being trapped in chat history

## Drafting Levels

Use three separate levels so the author can see real prose without locking the whole novel too early.

1. Raw episode: cleaned factual/emotional memory, not reader-facing prose.
2. Scene card: fictional plan, conflict, subtext, privacy risks, and possible placement.
3. Scene fragment: actual English novel prose for testing voice and sentence-level revision.

A fragment is allowed early. A full chapter waits until several related episodes and the outline support it.

## Episode Pipeline

1. Write one episode in Google Docs.
2. Title it clearly, for example: `Episode 001 - The First Message`.
3. Codex reads the selected Google Doc through Drive MCP.
4. Save the cleaned source version as `01_raw_episodes/001_the_first_message.md`.
5. Create a scene card as `02_scene_cards/001_the_first_message.md`.
6. Record only provisional placement in `03_outline/chapter_outline.md`.
7. Add privacy notes before any scene becomes reader-facing prose.
8. When useful, create a short prose fragment in `04_draft/scene_fragments/` so the author can review actual English fiction sentences before full chapters are drafted.

## File Naming

Use numbered lowercase filenames:

- `01_raw_episodes/001_short_title.md`
- `02_scene_cards/001_short_title.md`
- `04_draft/scene_fragments/001_short_title.md`
- `04_draft/ch01.md`
- `04_draft/ch02.md`

Keep episode numbers stable even if the outline changes. Episode number is collection order, not final chapter order.

## What To Commit To GitHub

Commit:

- Markdown project files
- cleaned raw episodes
- scene cards
- outline changes
- draft chapters
- revision notes
- KDP metadata and descriptions

Avoid committing by default:

- temporary Word files
- duplicate exports
- very large cover source files
- private unfictionalized source material that should not live in GitHub

## Suggested Rhythm

For each episode:

1. Author drafts in Google Docs.
2. Codex cleans it into the raw episode template.
3. Codex creates a scene card.
4. Codex records a provisional placement only.
5. Codex may create a short scene fragment in real English novel prose for sentence-level review.
6. Author comments on voice, emotional accuracy, omissions, and privacy risk.
7. Codex updates the scene card, fragment, and project bible as needed.

After 5 to 7 episodes:

- revise the chapter outline
- identify missing emotional beats
- decide which fragments belong together
- decide the opening chapter strategy

Only then begin assembling full chapter drafts. Full chapters should be built from approved fragments, not invented from one isolated episode.

## Privacy Rule

Do not put highly identifying real-life material into GitHub unless it has been fictionalized or the author explicitly decides it belongs there.

## Google Drive MCP Option

This project is prepared for direct Google Drive reading through a Codex MCP server named `gdrive`. See `GOOGLE_DRIVE_MCP_SETUP.md`.

Recommended use:

1. Draft the original episode in a dedicated Google Drive folder.
2. Ask Codex to read the selected Google Doc through `gdrive`.
3. Codex creates the cleaned Markdown episode, scene card, provisional outline placement, and, when useful, a short scene fragment.
4. Codex commits the structured project files to GitHub.

Keep OAuth credentials and unfictionalized sensitive source material out of GitHub.

