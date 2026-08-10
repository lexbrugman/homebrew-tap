# homebrew-tap

Homebrew formulae for my projects.

## Use

```sh
brew install lexbrugman/tap/<formula>
```

That taps this repository automatically; `brew tap lexbrugman/tap` first is
not necessary.

## Updating

```sh
brew update && brew upgrade <formula>
```

If a formula installs a background service, upgrading does **not** restart
it — Homebrew leaves the running process on the old binary until the next
login. A formula's own `--version` reports what is *installed*, not what is
running, so an upgrade can look complete while the old process is still
serving:

```sh
brew services restart <formula>
```

## Formulae are generated — do not edit them

Everything in `Formula/` is written and pushed by the release pipeline of
the project it belongs to, on every release. Changes made here by hand are
overwritten by the next release, silently. Fix the generator in that
project instead.

## Issues

This repository holds packaging only. Report bugs, and read the
documentation, in the repository of the project itself.
