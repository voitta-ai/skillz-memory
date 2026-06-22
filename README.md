# skillz-memory

Shared **memory** vault for the [voitta-ai/skillz](https://github.com/voitta-ai/skillz)
ecosystem: *specifics* — a single cause->fix, an API gotcha, a config detail, a
project quirk. The companion to the skills catalog.

## Skill vs memory

Per [skillz#72](https://github.com/voitta-ai/skillz/issues/72), one cut:

- **Skill** = a repeatable *procedure* with judgment. Lives in
  [voitta-ai/skillz](https://github.com/voitta-ai/skillz) (always-on, PR-reviewed,
  installable). The agent *does* something.
- **Memory** = a specific *recollection* (cause->fix, gotcha, config, quirk). Lives
  here. The agent *recalls* something.

The split exists for economics: every catalog entry's name + description is injected
into the agent's context every session, so cataloging a one-off fact taxes context
and prompt-cache forever ([skillz#70](https://github.com/voitta-ai/skillz/issues/70)).
Memory is recalled on demand instead, so it scales without that tax.

## Recall (two tiers)

- **Long tail** — voitta-rag indexes this folder; recalled via semantic `search`.
  No context cost, no auto-fire.
- **Hot set** — a handful of broadly-useful notes are symlinked into the agent's
  project memory dir for always-on auto-recall.

## Format

One file per memory, `<slug>.md`, with frontmatter:

    ---
    name: <short-kebab-case-slug>
    description: <one-line summary — used for recall relevance>
    metadata:
      type: user | feedback | project | reference
    ---

    <the fact. Link related memories with a portable link: [text](other-slug.md).>

`MEMORY.md` is the one-line-per-memory index.

## Conventions

Aligned with [method-and-apparatus/hq#112](https://github.com/method-and-apparatus/hq/issues/112)
(Obsidian-as-lens): the repo folder *is* the vault.

- Portable Markdown only — standard `[text](path.md)` links. No `[[wikilinks]]`,
  Dataview, or embeds in committed files (GitHub won't render them and agents need
  portable text). Obsidian plugins are for viewing only.
- `.obsidian/` is git-ignored (machine-local config).

## Provenance

Specifics migrated out of the skillz catalog per
[skillz#77](https://github.com/voitta-ai/skillz/issues/77).
