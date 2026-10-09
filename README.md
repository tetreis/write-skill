# write

A Claude skill with writing rules for prose: emails, site copy, LinkedIn posts, blog posts, edits. It bans the patterns that make text read as AI-written and pushes Claude toward plain, specific sentences.

Claude loads it on its own when you ask it to write or edit a text. You can also call it with `/write`.

## What it covers

- Voice: start with the answer, short paragraphs, contractions, numbers and names over adjectives.
- Vocabulary: 82 banned words, including delve, leverage, seamless and robust.
- Reframes: "This isn't X. It's Y." and its softer variants, including ones split across 2 sentences.
- Staged twists: taglines built so the second beat lands as a punchline.
- Analogies: off by default, with a 5-point test for when one is allowed.
- A 14-step final pass Claude runs before sending.

The full rules are in [write/SKILL.md](write/SKILL.md). They also work as a style guide for people.

## Install

### Claude Code

```bash
git clone https://github.com/tetreis/write-skill.git
mkdir -p ~/.claude/skills && cp -r write-skill/write ~/.claude/skills/
```

Start a new Claude Code session. The skill shows up as `/write`.

### Claude app (web and desktop)

Zip the `write` folder and upload it in Settings → Capabilities → Skills.

### Other tools

Copy everything below the frontmatter in `SKILL.md` into your custom instructions, `AGENTS.md` or Cursor rules.

## Customizing

The rules are written in the first person ("Read this before writing to me or for me"), so once installed they speak for you. Edit them: add words you can't stand, drop bans you disagree with.

The `description` at the top of `SKILL.md` decides when Claude loads the skill. It lists trigger phrases in English and Portuguese.

## License

MIT. Use, change and share it, and keep the copyright notice. See [LICENSE](LICENSE).
