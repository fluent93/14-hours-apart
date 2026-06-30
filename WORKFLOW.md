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

## Episode Pipeline

1. Write one episode in Google Docs.
2. Title it clearly, for example: `Episode 001 - The First Message`.
3. Share or export the episode text.
4. Save the cleaned version as `01_raw_episodes/001_the_first_message.md`.
5. Create a scene card as `02_scene_cards/001_the_first_message.md`.
6. Update possible placement in `03_outline/chapter_outline.md`.
7. Add privacy notes before any scene becomes draft prose.

## File Naming

Use numbered lowercase filenames:

- `01_raw_episodes/001_short_title.md`
- `02_scene_cards/001_short_title.md`
- `04_draft/ch01.md`
- `04_draft/ch02.md`

Keep numbers stable even if the outline changes.

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
4. Codex suggests outline placement.
5. Author approves or corrects the placement.
6. Codex commits the repository update.

After 5 to 7 episodes:

- revise the chapter outline
- identify missing emotional beats
- decide the opening chapter strategy

Only then begin drafting full chapters.

## Privacy Rule

Do not put highly identifying real-life material into GitHub unless it has been fictionalized or the author explicitly decides it belongs there.
