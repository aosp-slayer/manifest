### Get started: ###

**Download the source code**

# Initialize local repository
```bash
repo init -u https://github.com/aosp-slayer/manifest.git -b s
```
# Sync

```bash
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```

**Build the rom**
```bash
. build/envsetup.sh
lunch aosp_($Device)-userdebug
make otapackage
```