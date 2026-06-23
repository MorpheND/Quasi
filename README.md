# Quasi

Private packaged build repository for local-network connectivity testing.

## Recommended download

Download the latest packaged ZIP from the repository's **Releases** page,
extract the complete archive, then launch:

```text
Windows/ActionRoguelike.exe
```

Do not use GitHub's green **Code → Download ZIP** button. Source archives may
contain Git LFS pointer files rather than runnable Windows binaries, which can
produce the message “This app can't run on your PC.”

## Git/LFS download

Developers can clone the build repository instead:

```powershell
git lfs install
git clone https://github.com/MorpheND/Quasi.git
cd Quasi
git lfs pull
git lfs checkout
```

The complete `Windows` directory is required in either case. Do not download or
copy only the executable.

## Updating

The repository stores packaged Unreal binaries through Git LFS. Replace the
contents of `Windows`, then commit and push the complete build.

For non-technical testers, also create a GitHub Release and attach a normal ZIP
containing the hydrated `Windows` directory. Include its SHA-256 checksum.
