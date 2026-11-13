# Outpace Scoop bucket

Install published [Outpace engine](https://github.com/outpace-stream/outpace-engine) binaries.

```powershell
scoop bucket add outpace https://github.com/outpace-stream/scoop-outpace
scoop install outpace/outpace
```

If the `outpace` bucket already points at the old engine repository, run
`scoop bucket rm outpace`, add it again using the URL above, then run `scoop update`.

## Updating

The manifest is generated from published engine release `SHA256SUMS`; never guess a checksum.
From an engine checkout, run `tools/release/package_manifests.py` with explicit
`--homebrew-root` and `--scoop-root` checkout directories, then open a PR here.
See the [release guide](https://github.com/outpace-stream/outpace-engine/wiki/Releases-and-Versions#updating-the-homebrew-formula-and-scoop-manifest).
Installation is checked on the native platform in GitHub Actions.
