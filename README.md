# FoldNine Homebrew tap

Homebrew formulae for [FoldNine](https://foldnine.dev) open-source tools.

```bash
brew install foldnine/tap/aftergreen
```

| Formula | Description | Source |
| --- | --- | --- |
| `aftergreen` | Post-deployment verification: VERIFIED, FAILED or UNKNOWN | [foldnine/aftergreen](https://github.com/foldnine/aftergreen) |

## aftergreen

Installs the prebuilt release binary for macOS and Linux (amd64, arm64).
Homebrew checks each archive against the SHA256 in the formula before
installing.

```bash
brew install foldnine/tap/aftergreen
aftergreen http --url https://example.com --status 200 --contains "Example Domain"
# VERIFIED  HTTP outcome (HTTP 200)
```

Upgrade with `brew upgrade aftergreen`. Other install methods (install
script, Windows, direct downloads): see
[docs/install.md](https://github.com/foldnine/aftergreen/blob/main/docs/install.md).

## Maintenance

Don't edit `Formula/aftergreen.rb` by hand. It is generated from each
release's `SHA256SUMS` by
[`packaging/homebrew/render-formula.sh`](https://github.com/foldnine/aftergreen/blob/main/packaging/homebrew/render-formula.sh)
in the aftergreen repository; copy the result here in a PR. CI installs the
formula on macOS (Apple silicon, Intel) and Linux, then runs `brew test` and
`brew audit --strict`.

Apache-2.0. See [LICENSE](LICENSE).
