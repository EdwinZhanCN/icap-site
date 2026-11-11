# ICAP Learning Agent: docs site

The site at [icap.edwinzhan.space](https://icap.edwinzhan.space): a guide, the format reference, and the plugin's own interface shown live. Astro Starlight, in English and Simplified Chinese.

The pages import the plugin's Svelte components and stylesheet from `plugin/src`. `plugin/` is the [plugin repository](https://github.com/EdwinZhanCN/obsidian-icap-agent) as a git submodule. `src/demo/obsidian.ts` stands in for Obsidian's API.

```bash
git clone --recursive <this repo>        # or: git submodule update --init
pnpm install
pnpm dev                                 # local preview
pnpm build                               # dist/
pnpm run deploy                          # build, then wrangler deploy (Cloudflare Workers static assets)
```

To show a newer version of the plugin's interface, move the submodule and commit it:

```bash
git -C plugin pull origin main && git add plugin
```

Write pages to [STYLE.md](STYLE.md) (ASD-STE100 rules, both languages). A page and its translation change together.
