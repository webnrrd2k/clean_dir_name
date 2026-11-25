# clean_dir_name (`cn`)

Rust port of `dirname-clean` from my
[dotfiles](https://github.com/webnrrd2k/dotfiles). It reads lines from stdin and
turns each into a lowercase, ASCII, filesystem-safe name.

```bash
echo 'Café & Łódź  Notes!' | cn -f     # prints: cafe+lodz_notes
echo 'Café & Łódź  Notes!' | cn        # creates the directory cafe+lodz_notes
```

`-f` / `--filter` prints the cleaned text instead of creating directories.

## Install

```bash
sudo dnf install cargo      # if needed
cargo install --root ~/.local --git https://github.com/webnrrd2k/clean_dir_name
```

This puts `cn` in `~/.local/bin`. Or run `install.sh` from the dotfiles repo,
which offers to do it.
