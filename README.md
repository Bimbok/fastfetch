# Fastfetch Config

Personal `fastfetch` setup with:

- `config.jsonc` for the full layout with the `anya.png` logo
- `config-tmux.jsonc` for a compact tmux-friendly layout without the image logo

## Preview

### Logo

![Anya logo used by fastfetch](anya.png)

### Samples

![Default fastfetch sample](sample/2026-04-24-124236_hyprshot.png)

![Tmux fastfetch sample](sample/2026-04-24-124244_hyprshot.png)

## Files

- `config.jsonc`
- `config-tmux.jsonc`
- `anya.png`
- `sample/`

## Usage

Run the normal config:

```bash
fastfetch --config ~/.config/fastfetch/config.jsonc
```

Use the tmux-aware launcher:

```bash
if [[ -n "$TMUX" ]]; then
    fastfetch --config ~/.config/fastfetch/config-tmux.jsonc
else
    fastfetch
fi
```

## Notes

- The default config expects Kitty image support because it uses `"type": "kitty-direct"` for the logo.
- If your default fastfetch config path already points here, `fastfetch` is enough outside tmux.
