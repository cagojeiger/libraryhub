# LibraryHub

This public repository runs LibraryHub CI on GitHub-hosted runners. The
private LibraryHub Core repository owns the application, request authority,
and result and recovery state.

The Rust job validates the bound request using Core's CI control. It fetches
the exact tested commit and revokes its scoped reader token before executing
checks. Core records the actual control and public workflow revisions. Private
build output and GitHub command files are suppressed.

The workflow follows [Mossden's public CI control](https://github.com/cagojeiger/mossden/tree/7706e75f5e8a1587c454fe9f439c08268dd8eef1)
and is provided under [GPL-3.0](LICENSE).
