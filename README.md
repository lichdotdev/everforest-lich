<h2 align="center">Everforest for lich</h2>

<p align="center">A green based color scheme designed to be warm and soft in order to protect developers' eyes</p>

<p align="center">
    <a href="https://github.com/sainnhe/everforest">
        <img src="https://img.shields.io/badge/community-everforest-a7c080?labelColor=2d353b&style=for-the-badge" />
    </a>
</p>

## Usage

1. Open lich → **Settings → Appearance → Import**.
2. Paste the repository URL: `https://github.com/lichdotdev/everforest-lich`
3. Click **Install**.
4. Pick a variant in the theme picker. The terminal picker defaults to
   **Match app theme**, so one pick dresses both — or choose a different variant
   there if you want the panes to differ.

To take a later release, hit **Update** on the theme's row.

### Local install

An absolute path is an accepted remote, so a clone installs the same way:

```bash
git clone https://github.com/lichdotdev/everforest-lich.git
```

Then paste the absolute path of the clone into **Settings → Appearance → Import**.

## Variants

Everforest ships each background at three contrasts (hard, medium, soft). This
pack carries the default, **medium**.

| Theme | `id` | `scheme` |
|---|---|---|
| Everforest Dark | `everforest-dark` | dark |
| Everforest Light | `everforest-light` | light |

## Status tones

`tone-pass` and `tone-wait` are what lich 0.53.0 reads for "passed" and "waiting
on you". The status line sets them at 12px, where WCAG asks 4.5:1 with no
large-text exemption, so where the palette value did not clear that against the
card it sits on, its lightness was moved and its hue and saturation kept: the
same move lich makes for its own two.

| Variant | `tone-pass` | `tone-wait` |
|---|---|---|
| Everforest Dark | `#a7c080` (green) | `#dbbc7f` (yellow) |
| Everforest Light | `#657301` (green, darkened) | `#8d6500` (yellow, darkened) |

## Thanks to

- [omartelo](https://github.com/omartelo) — port author
- [sainnhe](https://github.com/sainnhe) — original palette

## Contributing

Each variant is one lich theme file — `everforest-dark.json`,
`everforest-light.json` — beside the `lich-theme.json` manifest that carries the
pack's version. Colors come from the palette in
[`autoload/everforest.vim`](https://github.com/sainnhe/everforest/blob/master/autoload/everforest.vim),
and the terminal ANSI colors follow the mapping in `colors/everforest.vim`.

To propose a tweak:

1. Fork the repo.
2. Edit the relevant variant file.
3. Validate the **whole directory** — a repository installs all or nothing:
   `node validate.mjs .` (ships with the lich `theme` skill).
4. Bump `version` in `lich-theme.json` in the same commit. An unbumped version
   ships nothing: **Update** compares only that number.
5. Open a PR.

## License

[MIT](./LICENSE)
