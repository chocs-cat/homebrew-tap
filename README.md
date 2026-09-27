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

`Formula/corral-herdr.rb` is updated by hand after each PyPI release: bump
`url`/`sha256` to the new sdist, then refresh the dependency resources with
`brew update-python-resources corral-herdr`. That command ignores packages
uploaded in the last 24 hours, so wait a day after the release, or copy the
versions from corral's `uv.lock`.

It moved here from `johnfoland/tap`, which migrates existing installs on
`brew update`.
