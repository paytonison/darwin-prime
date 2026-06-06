# License Notes

This repository is for coordination material around Darwin Prime. It is not a
license override for Apple source.

## XNU

The XNU fork in `../darwin-prime-xnu` carries Apple's upstream license files and
license headers. Do not remove, rewrite, or normalize those headers as part of
project hygiene.

## Local Artifacts

Do not commit:

- SDKs or KDKs
- private Apple headers or binaries
- generated kernel build products
- DerivedData or Xcode result bundles
- `.dSYM`, `.o`, `.a`, `.dylib`, or generated `.kext` outputs

Tracked `.kext` directories that already exist in Apple XNU source, such as
`config/System.kext`, are upstream source-tree material and should not be
treated as generated local artifacts.
