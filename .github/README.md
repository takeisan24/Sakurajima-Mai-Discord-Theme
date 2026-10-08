<p align="center">
  <img src="https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/image/maisan.gif" width="640" alt="Sakurajima Mai wallpaper">
</p>

<h1 align="center">Sakurajima Mai Theme</h1>

<p align="center">
  A calm, lavender Discord theme inspired by Sakurajima Mai (<i>Rascal Does Not Dream of Bunny Girl Senpai</i>),<br>
  built on top of <a href="https://github.com/puckzxz/NotAnotherAnimeTheme">NotAnotherAnimeTheme</a> by puckzxz.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-2.0.0-a895d6?style=flat-square" alt="Version 2.0.0">
  <img src="https://img.shields.io/badge/Vencord-supported-a895d6?style=flat-square" alt="Vencord supported">
  <img src="https://img.shields.io/badge/BetterDiscord-supported-a895d6?style=flat-square" alt="BetterDiscord supported">
  <img src="https://img.shields.io/badge/license-Unlicense-e0b494?style=flat-square" alt="Unlicense">
</p>

---

## Features

- **Balanced glass style:** the wallpaper stays visible behind the sidebars and chat, while a dark glass layer keeps text readable. Popouts, menus, tooltips and modals are 100% solid, so they never blend into the background.
- **One editable palette:** amethyst lavender (Mai's eyes) and blush porcelain (skin warmth) on deep violet surfaces. Change the whole theme from one block of variables.
- **Built on Discord's own design tokens:** menus, popouts, tooltips, modals and pickers are themed through the variables Discord actually uses, so they survive most Discord updates.
- **Readable everywhere:** danger actions stay red, mention badges stay red, your own reactions stay highlighted, and Light mode keeps readable text.
- **Nitro aware:** Nitro client theme gradients are neutralized so the Mai wallpaper shows through.
- **Bunny hairpin home icon**, plus everything from the NotAnotherAnimeTheme base (server list columns, unread rings, transparent layers).

## Installation

### Vencord / Vesktop

**Option A: online link (updates automatically)**

1. Open **User Settings → Vencord → Themes → Online Themes**.
2. Paste this link:
   ```
   https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css
   ```

**Option B: local file**

1. Download [`SakurajimaMai.theme.css`](https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css).
2. Open **User Settings → Vencord → Themes → Open Themes Folder** and put the file there.
3. Enable **Sakurajima Mai Theme** in the theme list.

### BetterDiscord

1. Download [`SakurajimaMai.theme.css`](https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/SakurajimaMai.theme.css).
2. Open **User Settings → Themes → Open Themes Folder** (usually `%AppData%\BetterDiscord\themes`) and put the file there.
3. Enable **Sakurajima Mai Theme**.

> In **User Settings → Appearance**, the **Dark** theme is recommended. Light mode is supported, but the theme is designed around dark surfaces.

## Customization

Do **not** edit the theme file itself. It is replaced every time the theme updates. Put your overrides in **QuickCSS** instead (Vencord: *Themes → Edit QuickCSS*; BetterDiscord: *Custom CSS*). Your overrides then survive updates.

Copy the variables you want to change, for example:

```css
:root {
  /* Your own wallpaper (any .jpg / .png / .gif URL) */
  --theme-background-image: url("https://example.com/my-wallpaper.jpg") !important;

  /* Glass darkness behind the sidebars and chat.
     Lower alpha = more wallpaper, higher = easier to read.
     More glass: 0.30   Default: 0.42   Easier reading: 0.60 */
  --theme-transparency: rgba(16, 14, 20, 0.42) !important;
  --message-box-transparency: rgba(20, 18, 26, 0.48) !important;

  /* Blur behind the bottom-left user panel (0px disables it) */
  --sm-panel-blur: 10px !important;
}
```

### All variables

| Variable | Default | What it changes |
|---|---|---|
| `--theme-background-image` | Mai GIF | Wallpaper |
| `--theme-transparency` | `rgba(16,14,20,.42)` | Glass layer behind sidebars and chat |
| `--message-box-transparency` | `rgba(20,18,26,.48)` | Message box and user panel glass |
| `--sm-panel-blur` | `10px` | Blur behind the user panel |
| `--sm-accent` + `--sm-accent-rgb` | `#a895d6` / `168 149 214` | Main accent (hover, highlights, links in menus). **Change both together.** |
| `--sm-accent-strong` (+ `-hover`, `-active`) | `#7d68b8` | Filled buttons. Keep it dark enough for white text. |
| `--sm-accent-2` + `--sm-accent-2-rgb` | `#e0b494` / `224 180 148` | Secondary accent (links, scrollbar, inline code). **Change both together.** |
| `--sm-surface-0` … `--sm-surface-3` | `#141218` … `#24202f` | Solid surfaces for popouts, menus, tooltips, modals |
| `--sm-text`, `--sm-text-strong`, `--sm-text-subtle`, `--sm-text-muted` | `#f4f2f6`, `#fff`, `#d0cce0`, `#a8a8b4` | Text colors |
| `--sm-radius-menu` | `12px` | Context menu corners |
| `--home-icon-image`, `--home-icon-image-zoom`, `--home-icon-image-position` | Bunny hairpin, `82%`, `center` | Home button icon |
| `--server-listing-width` | `72px` | Server list width (from the NotAnotherAnimeTheme base) |

## Nitro behavior

| Nitro feature | Current behavior |
|---|---|
| **Client theme** (your own app gradient) | Neutralized, so the Mai wallpaper is visible |
| **Profile theme** (other people's popout colors) | Shown in the solid Mai palette |

Planned (see the roadmap): keep other people's Nitro profile colors with Mai accents by default, plus a one-line QuickCSS switch to force the Mai palette.

## Roadmap

The theme is being refined component by component toward a stable release for the NotAnotherAnimeTheme community folder:

- [x] Rebuild on Discord's design tokens; fix popout, menu, tooltip, badge and scrollbar regressions (v2.0.0)
- [ ] Palette and wallpaper pass
- [ ] Glass layer, server list, channel list, chat, member list, user panel
- [ ] Nitro profiles: native colors + Mai accents by default, `--sm-nitro-profiles` switch
- [ ] Menus, tooltips, modals, settings, pickers, voice and call
- [ ] Performance and accessibility options (static wallpaper, reduced motion, glass amount)
- [ ] Preview screenshots and community submission

## Troubleshooting

- **Theme not updating:** the base stylesheet is served from jsDelivr, which can cache for a while. Press <kbd>Ctrl</kbd>+<kbd>R</kbd> to reload Discord.
- **Something looks broken after a Discord update:** open an [issue](https://github.com/takeisan24/Sakurajima-Mai-Discord-Theme/issues) with a screenshot.
- **Problems with the server list or base layout:** these may come from the NotAnotherAnimeTheme base. Check its [issues](https://github.com/puckzxz/NotAnotherAnimeTheme/issues) or [support server](https://discord.gg/FdZhbjY).

## Project structure

| Path | Owner | Purpose |
|---|---|---|
| `SakurajimaMai.theme.css` | This theme | The Sakurajima Mai theme |
| `image/maisan.gif`, `image/bunny-hairpin.*` | This theme | Wallpaper and home icon |
| `.github/README.md` | This theme | This page |
| `css/v3/`, `build/v3/` | NotAnotherAnimeTheme | Base stylesheet imported by the theme |
| `NotAnotherAnimeTheme.theme.css`, `README.md`, `community/`, `css/*csl.css` | NotAnotherAnimeTheme | The original theme, its README and community themes |

Files owned by NotAnotherAnimeTheme are kept identical to upstream, so upstream fixes can be merged without conflicts. The original project README is [`README.md`](../README.md).

## Credits

- **[puckzxz](https://github.com/puckzxz)**: author of [NotAnotherAnimeTheme](https://github.com/puckzxz/NotAnotherAnimeTheme), the base this theme is built on. If you enjoy it, consider [supporting the original author](https://www.paypal.me/ChrisBock).
- **[V-X](https://github.com/ImVexed)** and **[Qu4k3](https://github.com/Qu4k3)**: CDN hosting and long-term help on NotAnotherAnimeTheme.
- **[takeisan24](https://github.com/takeisan24)**: Sakurajima Mai theme, palette, wallpaper integration and home icon.
- Sakurajima Mai and *Seishun Buta Yarou* belong to Hajime Kamoshida, Keji Mizoguchi and their publishers. This is a non-commercial fan theme.

## License

Released into the public domain under [The Unlicense](../LICENSE), same as NotAnotherAnimeTheme.
