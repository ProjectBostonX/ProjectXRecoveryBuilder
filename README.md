# Project X Boston Recovery

Project X Boston Recovery is a Boston-specific GitHub Actions recovery builder for the Motorola Moto G Stylus 5G 2024, codename `boston`.

This repository is preconfigured to build a Team Win Recovery Project (TWRP) recovery image using the Boston device tree and defaults for this device.

## Boston defaults

The workflow is already configured with the correct default values for the Motorola Moto G Stylus 5G 2024:

- Recovery type: `twrp`
- Manifest URL: `https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git`
- Manifest branch: `twrp-12.1`
- Device tree URL: `https://github.com/PizzaG/android_device_motorola_boston.git`
- Device tree branch: `TWRP`
- Device path: `device/motorola/boston`
- Device name: `boston`
- Makefile: `twrp_boston`
- Build target: `recovery`

## What this repo does

- Builds Android recovery images from GitHub Actions
- Accepts recovery type and manifest inputs in the workflow UI
- Supports TWRP-first Boston builds
- Uploads artifacts to GitHub Releases

## How to run the build

1. Open the repository on GitHub.
2. Go to the Actions tab.
3. Select `Recovery Build`.
4. Click `Run workflow`.
5. Use the Boston defaults listed above, or adjust them only if you are intentionally changing the target.
6. Wait for the job to finish and download the generated recovery image from the release output.

## Recommended workflow inputs for Boston

```yaml
RECOVERY_TYPE: twrp
MANIFEST_URL: https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git
MANIFEST_BRANCH: twrp-12.1
DEVICE_TREE_URL: https://github.com/PizzaG/android_device_motorola_boston.git
DEVICE_TREE_BRANCH: TWRP
DEVICE_PATH: device/motorola/boston
COMMON_TREE_URL: ""
COMMON_PATH: ""
DEVICE_NAME: boston
DEVICE_CODENAME: boston
MAKEFILE_NAME: twrp_boston
BUILD_TARGET: recovery
```

## Notes

- This repository is set up as a starting point for Boston recovery builds.
- The device tree, kernel, vendor configuration, and board files must match the exact target device for a successful build.
- Output artifacts are uploaded as GitHub Release assets.

## Credits

This project is intended for the Motorola Moto G Stylus 5G 2024 (`boston`) recovery community and builds on work from the Android, TWRP, and custom recovery communities.

---

Project X Boston Recovery
Built for the Motorola Moto G Stylus 5G 2024 (`boston`) recovery community.
