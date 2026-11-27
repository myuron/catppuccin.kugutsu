# Catppuccin for Kugutsu

Soothing pastel theme for [Kugutsu](https://github.com/myuron/kugutsu).

## Flavors

| Flavor | Theme name |
| --- | --- |
| 🌻 Latte | `catppuccin-latte` |
| 🪴 Frappé | `catppuccin-frappe` |
| 🌺 Macchiato | `catppuccin-macchiato` |
| 🌿 Mocha | `catppuccin-mocha` |

## Usage

Add the plugin to `~/.config/kugutsu/init.lua` and select a flavor:

```lua
kugutsu.plugins.setup({ "myuron/catppuccin.kugutsu" })
kugutsu.opt.theme = "catppuccin-mocha"
```

Then resolve and clone it:

```sh
kugutsu lock
kugutsu install
```

Reload the configuration with `Ctrl-b` `r` (or restart Kugutsu).

Alternatively, copy one of the files in [`colors/`](colors/) to `~/.config/kugutsu/colors/`.

## Development

The files in `colors/` are generated from [`kugutsu.tera`](kugutsu.tera) with [whiskers](https://github.com/catppuccin/whiskers). Edit the template, then regenerate:

```sh
whiskers kugutsu.tera
# or, with Nix
nix run nixpkgs#catppuccin-whiskers -- kugutsu.tera
```

## License

[MIT](LICENSE)
