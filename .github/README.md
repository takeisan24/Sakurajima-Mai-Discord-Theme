<p align="center">
  <img src="https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/image/maisan.gif" width="640" alt="Sakurajima Mai wallpaper">
</p>

<h1 align="center">Sakurajima Mai Theme</h1>

<p align="center">
  A calm, lavender Discord theme inspired by Sakurajima Mai (<i>Rascal Does Not Dream of Bunny Girl Senpai</i>),<br>
  built on top of <a href="https://github.com/puckzxz/NotAnotherAnimeTheme">NotAnotherAnimeTheme</a> by puckzxz.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-3.3.0-a895d6?style=flat-square" alt="Version 2.0.0">
  <img src="https://img.shields.io/badge/Vencord-supported-a895d6?style=flat-square" alt="Vencord supported">
  <img src="https://img.shields.io/badge/BetterDiscord-supported-a895d6?style=flat-square" alt="BetterDiscord supported">
  <img src="https://img.shields.io/badge/license-Unlicense-e0b494?style=flat-square" alt="Unlicense">
</p>

---

## Features

- **Balanced glass style:** the wallpaper stays visible behind the sidebars and chat, while a dark glass layer keeps text readable. Popouts, menus, tooltips and modals are 100% solid, so they never blend into the background.
- **Lavender Dusk palette:** amethyst lavender (the saturated twin of the wallpaper's violet-grey) and porcelain peach (Mai's skin tone in the wallpaper), on surfaces stepped from the wallpaper hue so popouts feel like the same material. Change the whole theme from one block of variables.
- **Built on Discord's own design tokens:** menus, popouts, tooltips, modals and pickers are themed through the variables Discord actually uses, so they survive most Discord updates.
- **Readable everywhere:** danger actions stay red, mention badges stay red, your own reactions stay highlighted, and Light mode keeps readable text.
- **Nitro aware:** Nitro client theme gradients are neutralized so the Mai wallpaper shows through.
- **Bunny signature:** a lavender bunny logo in the title bar and the bunny hairpin home icon, plus everything from the NotAnotherAnimeTheme base (server list columns, unread rings, transparent layers).

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
  /* Wallpaper. Bundled variants of the Mai GIF:
     maisan-soft.gif (default), maisan.gif (original, more vivid),
     maisan-silhouette.gif (dark silhouette, easiest reading).
     Or any .jpg / .png / .gif URL of your own. */
  --theme-background-image: url("https://raw.githubusercontent.com/takeisan24/Sakurajima-Mai-Discord-Theme/refs/heads/master/image/maisan.gif") !important;

  /* Glass over the whole app. Lower alpha = more wallpaper.
     More glass: 0.30   Default: 0.42   Easier reading: 0.60 */
  --theme-transparency: rgb(var(--sm-glass-rgb) / 0.42) !important;

  /* Extra glass on the chat only, where text sits over Mai.
     0.15 = default (soft wallpaper), 0.35 = recommended with the original wallpaper */
  --sm-chat-glass: 0.15 !important;

  /* Lavender separators around the chat (0 hides them) */
  --sm-separator-alpha: 0.6 !important;

  /* Blur behind the bottom-left user panel (0px disables it) */
  --sm-panel-blur: 10px !important;
}
```

### All variables

| Variable | Default | What it changes |
|---|---|---|
| `--theme-background-image` | `maisan-soft.gif` | Wallpaper. Also bundled: `maisan.gif` (original), `maisan-silhouette.gif` |
| `--sm-wallpaper-color` | `#302e34` | Color around the wallpaper and while it loads |
| `--sm-wallpaper-reduced-motion` | `maisan-soft-static.png` | Still image used when the OS requests reduced motion. Set it to your own still image if you replace the wallpaper |
| `--sm-wallpaper-position`, `--sm-wallpaper-size` | `center`, `cover` | Wallpaper placement (e.g. `right bottom` / `auto 100%` for a cut-out character) |
| `--sm-glass-rgb` | `20 19 24` | Tint of every glass layer |
| `--theme-transparency` | `rgb(var(--sm-glass-rgb) / .42)` | Glass over the whole app |
| `--sm-chat-glass` | `0.15` | Extra glass on the chat and friends list (keeps text readable over Mai) |
| `--message-box-transparency` | `rgb(var(--sm-glass-rgb) / .48)` | Message box and user panel glass |
| `--sm-panel-blur` | `10px` | Blur behind the user panel |
| `--sm-separator-alpha` | `0.6` | Lavender separators around the chat (`0` hides them) |
| `--sm-accent` + `--sm-accent-rgb` | `#a895d6` / `168 149 214` | Main accent (hover, highlights, links in menus). **Change both together.** |
| `--sm-mention` | `#b9487f` | Mention badges and the "NEW" pill when mentions are off-screen |
| `--sm-accent-strong` (+ `-hover`, `-active`) | `#7d68b8` | Filled buttons. Keep it dark enough for white text. |
| `--sm-accent-2` + `--sm-accent-2-rgb` | `#e8bf9f` / `232 191 159` | Secondary accent (links, scrollbar, inline code). **Change both together.** |
| `--sm-surface-0` … `--sm-surface-3` | `#16151a` … `#28262d` | Solid surfaces for popouts, menus, tooltips, modals |
| `--sm-text`, `--sm-text-strong`, `--sm-text-subtle`, `--sm-text-muted` | `#f4f2f6`, `#fff`, `#d3d0dc`, `#a9a6b2` | Text colors |
| `--sm-nitro-profiles` | `native` | `native` keeps other people's Nitro profile colors, `mai` redraws every profile in the Mai palette |
| `--sm-radius-menu` | `12px` | Context menu corners |
| `--sm-logo-mask` | Bunny head SVG | Title-bar logo shape (any SVG/PNG used as a mask, tinted with `--sm-accent`) |
| `--home-icon-image`, `--home-icon-image-zoom`, `--home-icon-image-position` | Bunny hairpin, `82%`, `center` | Home button icon |
| `--server-listing-width` | `72px` | Server list width (from the NotAnotherAnimeTheme base) |

## Nitro behavior

| Nitro feature | Behavior |
|---|---|
| **Client theme** (your own app gradient) | Neutralized, so the Mai wallpaper is visible |
| **Profile theme** (other people's popout and profile colors) | **Kept exactly as the owner chose**, with a lavender ring. Profiles without a Nitro theme use the solid Mai palette |

Prefer every profile in the Mai palette? Add this to QuickCSS:

```css
:root { --sm-nitro-profiles: mai !important; }
```

## Roadmap

The theme is being refined component by component toward a stable release for the NotAnotherAnimeTheme community folder:

- [x] Rebuild on Discord's design tokens; fix popout, menu, tooltip, badge and scrollbar regressions (v2.0.0)
- [x] Palette and wallpaper pass: Lavender Dusk palette, centered wallpaper with readable chat glass (v2.1.0)
- [x] App frame: lavender gradient separators framing the chat, softened wallpaper (v2.2.0)
- [x] Title bar bunny logo, channel header and search polish (v2.3.0)
- [x] Server list: unread dot, selected ring, hover lift, rose mention badges, BetterFolders-friendly (v2.4.0)
- [x] Channel list: selected rail, lavender categories, diamond-notch unread with glowing glyph, hover slide, lavender "NEW" feature badges (v2.5.0)
- [x] Chat: rose-mauve mentions, lavender quotes, calm spoilers, Mai syntax palette for Discord's highlighter, readable names over the wallpaper, reaction pop (v2.6.1). Plugin colors (ShikiCodeblocks, role-colored mentions) are left untouched
- [x] Message input: lavender edge, focus ring, lavender button hover, lavender typing dots; app-wide input borders (v2.7.0)
- [x] Member list: lavender hover wash and 2px slide; Nitro nameplates untouched (v2.8.0)
- [x] User panel and app frame outlines: lavender frame borders (--app-frame-border), lavender settings gear on hover; Nitro nameplates untouched (v2.9.0)
- [x] Nitro profiles: native colors + lavender ring by default, `--sm-nitro-profiles: mai` switch (v3.0.0)
- [x] Menus, tooltips, modals and pickers verified live: solid Mai surfaces, red danger actions kept, lavender selection (no extra CSS needed thanks to the token layer)
- [x] Lavender keyboard focus rings (v3.1.0)
- [x] Voice and call screens verified live on a community server (status colors kept)
- [x] UX pass: lavender jump highlight, message hover rail, avatar bounce, sliding link underline, button press, lavender switches/checkboxes, reply bar and jump-to-present bar (v3.3.0)
- [x] Reduced motion: still wallpaper and no hover motion when the OS asks for it (v3.2.0)
- [ ] Preview screenshots and community submission

## Troubleshooting

- **Theme not updating:** the base stylesheet is served from jsDelivr, which can cache for a while. Press <kbd>Ctrl</kbd>+<kbd>R</kbd> to reload Discord.
- **Something looks broken after a Discord update:** open an [issue](https://github.com/takeisan24/Sakurajima-Mai-Discord-Theme/issues) with a screenshot.
- **Problems with the server list or base layout:** these may come from the NotAnotherAnimeTheme base. Check its [issues](https://github.com/puckzxz/NotAnotherAnimeTheme/issues) or [support server](https://discord.gg/FdZhbjY).

## Project structure

| Path | Owner | Purpose |
|---|---|---|
| `SakurajimaMai.theme.css` | This theme | The Sakurajima Mai theme |
| `image/maisan*.gif`, `image/maisan-soft-static.png`, `image/bunny-hairpin.*` | This theme | Wallpapers (original, soft, silhouette, still) and home icon |
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
