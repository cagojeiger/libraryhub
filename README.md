# LibraryHub

This public repository runs LibraryHub CI on GitHub-hosted runners. The
private LibraryHub Core repository owns the application, request authority,
and result and recovery state.

The Gate and Rust jobs each validate the bound request using the same pinned
private control revision. The Rust job fetches the exact tested commit and
revokes its scoped reader token before executing checks. Private build
output and GitHub command files are suppressed.

The shell helpers in `.github/scripts/` adapt
[Mossden's public CI control](https://github.com/cagojeiger/mossden/tree/59a794da3f5df39243b62d3e7f64e2e774e277aa)
for LibraryHub. They are provided under [GPL-3.0](LICENSE).
