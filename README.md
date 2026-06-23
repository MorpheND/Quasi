# Quasi

Packaged build repository for local-network connectivity testing.

## Recommended download

Download the latest packaged ZIP from the repository's **Releases** page,
extract the complete archive, then launch:

```text
Windows/ActionRoguelike.exe
```

Do not use GitHub's green **Code -> Download ZIP** button. Source archives may
contain Git LFS pointer files rather than runnable Windows binaries, which can
produce the message "This app can't run on your PC."

## Git/LFS download

Developers can clone the build repository instead:

```powershell
git lfs install
git clone https://github.com/MorpheND/Quasi.git
cd Quasi
git lfs pull
git lfs checkout
```

The complete `Windows` directory is required. Do not download or copy only the
executable.

## Updating the packaged build

Replace the contents of `Windows`, then stage the changed files:

```powershell
git add .gitattributes .gitignore README.md Windows
git lfs status
git status --short
```

Large `.exe`, `.dll`, `.pak`, `.ucas`, and `.utoc` files should appear as Git
LFS objects after staging.

Do not commit release ZIP files. Git LFS stores individual repository assets;
GitHub Releases store the downloadable ZIP intended for testers.

For non-technical testers, create a GitHub Release and attach a normal ZIP
containing the hydrated `Windows` directory. Include its SHA-256 checksum.

## Source assets

This repository is prepared to store Unreal source assets through Git LFS if
source is added later. `.uasset`, `.umap`, and common large media formats are
already covered.

Generated source-project directories such as `Binaries`, `Intermediate`,
`Saved`, and `DerivedDataCache` should remain ignored.

## Never commit

- API keys or `.env` files
- Game-session tickets
- Runtime logs and crash dumps
- Development `.pdb` symbols for tester builds
- Generated release ZIP files
