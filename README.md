# GTA 6 Bar

Omarchy's status bar, dressed up for the GTA VI theme. A drop-in replacement for the built-in `omarchy.bar` plugin.

![Floating islands across the top of the screen](screenshots/bar.png)

| Tray closed | Tray open |
|---|---|
| ![Right island with the tray closed](screenshots/tray-closed.png) | ![Right island grown to fit the tray drawer](screenshots/tray-open.png) |

- **Floating islands:** the left, center and right sections each float in their own rounded island, with the wallpaper showing between them and a small gap above.
- **Sunset border:** each island has a soft border in the theme's window-border gradient, sweeping from sunset orange through Vice pink to twilight purple.
- **Lined up with windows:** the side islands start at Omarchy's default 10px window gap, so their outer edges line up with the windows below.
- **Snug tray:** the right island starts at the tray's chevron rather than the space reserved for hidden apps, and grows as the drawer slides open.

The islands only appear while the current theme is GTA VI (`gta6` when installed with `omarchy theme install`, or `gta-vi`) and the bar is at the top or bottom. On every other theme, or on a left or right bar, it looks and behaves exactly like the stock bar. Your widgets, layout and settings in `shell.json` are used as they are.

Pairs well with [GTA 6 Workspaces](https://github.com/dbohry/omarchy-gta6-workspaces), whose sliding Vice pink pill matches the islands.

## Install

```bash
omarchy plugin add https://github.com/dbohry/omarchy-gta6-bar.git
omarchy bar use gta6-bar
omarchy restart shell
```

The restart makes sure the stock bar is fully unloaded.

## Tuning

The island settings sit near the top of `Bar.qml`: `islandGap` (space above the islands), `islandPadding` (space inside each island), `islandEdge` (distance from the screen sides; match it to your Hyprland `gaps_out`), and the island `radius` and border `opacity` in the `Island` component.

## Uninstall

```bash
omarchy bar use omarchy.bar
omarchy plugin remove gta6-bar
omarchy restart shell
```

This is a fork of a built-in plugin, so it does not get Omarchy's later bar fixes on its own.

## License

MIT. Based on the `omarchy.bar` plugin from [Omarchy](https://github.com/basecamp/omarchy), which is also MIT licensed.
