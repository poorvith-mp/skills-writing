# skills-writing

Claude / Agent **skills** library by **Poorvith M P**.

- Version: **v0.1**
- Last updated: **July 2026**
- License: **MIT**
- Skills in this repo: **9**

Part of the **[open-claude-skills](https://github.com/prvthmpcypher/open-claude-skills)** multi-repo hub.

## Install

### Claude Code
```bash
# copy one skill
cp -R skills/<skill-id> ~/.claude/skills/<skill-id>
# or project-local
cp -R skills/<skill-id> .claude/skills/<skill-id>
```

### Claude.ai
Zip a single `skills/<skill-id>` folder and upload via **Settings → Capabilities → Skills**.

## Skill index

| Skill ID | Title |
|----------|-------|
| `bio-writer` | Bio Writer |
| `book-outline-builder` | Book Outline Builder |
| `case-study-writer` | Case Study Writer |
| `ebook-chapter-writer` | Ebook Chapter Writer |
| `ghostwriter` | Ghostwriter |
| `press-release-writer` | Press Release Writer |
| `story-hook-writer` | Story Hook Writer |
| `technical-writer` | Technical Writer |
| `thread-to-blog-converter` | Thread to Blog Converter |

## Structure

Each skill follows skill-creator conventions:

```text
skills/<skill-id>/
├── SKILL.md
├── references/NOTE.md   # empty tips for future progressive disclosure
└── assets/NOTE.md       # empty tips for future templates
```

## Author

Copyright (c) 2026 Poorvith M P
