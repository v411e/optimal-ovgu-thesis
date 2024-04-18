## Fonts
This template requires these two fonts to be installed on your system:
- New Computer Modern
- New Computer Modern Sans

### NixOS
In your `configuration.nix`:
```nix
  fonts.packages = with pkgs; [
    liberation_ttf # here are your other fonts (liberation is just an example)
  ] ++ texlive.newcomputermodern.pkgs; # ← New Computer Modern font
```

## Development
In case you want to contribute, check out the repo into a [typst package directory](https://github.com/typst/packages?tab=readme-ov-file#local-packages) 

### Example for Linux:
Local package path: `~/.local/share/typst/packages/local/optimal-ovgu-thesis/develop`

```sh
mkdir -p ~/.local/share/typst/packages/local/optimal-ovgu-thesis
cd ~/.local/share/typst/packages/local/optimal-ovgu-thesis
git clone git@github.com:v411e/optimal-ovgu-thesis.git
mv optimal-ovgu-thesis 0.1.0
```

This will make the package available locally, so you can use `typst init "@local/optimal-ovgu-thesis:0.1.0"` to create a test-project from the template.
