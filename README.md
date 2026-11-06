# Night Porter marketplace

The official index of [Night Porter](https://night-porter.com) packs. A pack adds review steps,
reply styles or environment presets to Night Porter. Packs are text only (markdown, TOML, plain
text) and always pinned to a commit.

```sh
nightporter market update     # fetch this index
nightporter pack add <name>   # install a pack from it
```

## Adding a pack

1. Write the pack and push it to a public git repo. See
   [Writing packs](https://docs.night-porter.com/writing-packs).
2. Open a PR here that adds a `[[packs]]` entry to `marketplace.toml` with the pack's **full
   commit SHA** as `rev`.
3. A maintainer reads every file in the pack at that commit before merging. Updates are new PRs
   that change `rev`; users see the diff before their copy updates.

Packs can only make Night Porter stricter. They can't run code or skip its checks.

Questions: [hi@night-porter.com](mailto:hi@night-porter.com).
