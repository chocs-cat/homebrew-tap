# chocs-cat/tap

Homebrew formulae from chocs-cat.

```sh
brew install chocs-cat/tap/tack
brew install chocs-cat/tap/corral-herdr
```

| Formula | What it is |
|---|---|
| [`tack`](https://github.com/chocs-cat/tack) | Deploy agent skills to Claude Code and Codex from one manifest, and audit projects so either agent sees the same instructions, skills and hooks. |
| [`corral-herdr`](https://github.com/chocs-cat/corral) | Round up your projects into [herdr](https://herdr.dev) workspaces, from a TUI or a CLI. |

`Formula/tack.rb` is written by tack's release workflow after each PyPI
release; don't edit it by hand.

## corral

The formula is `corral-herdr` (its PyPI name) because homebrew/core's `corral`
is the Pony package manager; both install a `corral` binary, so they conflict.
herdr is not a dependency, so installing corral never upgrades a running herdr.
Install it with `brew install herdr`.

`Formula/corral-herdr.rb` is written by corral's release workflow after each
PyPI release, with its dependencies at the versions in that release's
`uv.lock`; don't edit it by hand.

It moved here from `johnfoland/tap`, which migrates existing installs on
`brew update`.
