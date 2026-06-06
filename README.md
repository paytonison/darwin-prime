# Darwin Prime

Darwin Prime is a research OS project centered on Apple's open Darwin/XNU
substrate. It is not a macOS clone, a UI skin, or a redistribution of Apple
private components.

This repository is the command-center repo. It should contain project notes,
manifests, scripts, experiments, and patches that describe or drive work around
the upstream-tracked XNU fork.

## Local Layout

Expected sibling layout:

```text
~/dev/darwin-prime/
  darwin-prime/          # this command-center repo
  darwin-prime-xnu/      # fork of apple-oss-distributions/xnu
  upstreams/
    distribution-macOS/  # optional read-only reference clone
    PureDarwin/          # optional read-only reference clone
```

## Repository Boundaries

- Keep XNU source in `../darwin-prime-xnu`.
- Keep SDKs, KDKs, build products, private Apple files, and generated artifacts
  out of this repository.
- Store experimental notes and patch descriptions here before touching XNU.
- Treat upstream source and license headers as sacred unless a change is
  deliberate, reviewed, and isolated.

## First Checks

```sh
git -C ../darwin-prime-xnu status --short --branch
git -C ../darwin-prime-xnu remote -v
git -C ../darwin-prime-xnu tag --list | tail
```
