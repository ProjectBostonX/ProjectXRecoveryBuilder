# Project X Boston Recovery

Project X Boston Recovery is a Boston-optimized universal Android recovery builder built around the existing Action Recovery Builder workflow.

This repository is designed to help build Android recovery images for the Motorola Moto G Stylus 5G 2024, codename `boston`, while also remaining reusable for other recovery targets using a similar recovery workflow.

## What this repository does

- Builds recovery images through GitHub Actions
- Accepts recovery type and manifest inputs from the workflow UI
- Supports TWRP-first Boston builds and additional recovery flavors
- Uploads generated recovery artifacts to GitHub Releases
- Keeps the workflow structured for reuse on similar devices

## Boston defaults

- Device codename: `boston`
- Model family: Motorola Moto G Stylus 5G 2024
- Recovery default: `twrp`
- Main manifest: `https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git`
- Manifest branch: `twrp-12.1`
- Device tree: `https://github.com/PizzaG/android_device_motorola_boston.git`
- Device tree branch: `TWRP`
- Device path: `device/motorola/boston`
- Makefile: `twrp_boston`
- Build target: `recovery`

## Credits

This project builds on work and knowledge from the Android, TWRP, and custom recovery communities.

- ProjectXGang
  - Project owner and builder maintainer
- Motorola Moto G Stylus 5G 2024 community
  - Boston codename and device reference
- Team Win Recovery Project (TWRP)
  - Recovery build structure and device tree conventions
- Android Open Source Project (AOSP)
  - Source tree and recovery build system
- XDA Developers community
  - Device tree and recovery troubleshooting references
- PizzaG / `android_device_motorola_boston`
  - Primary Boston device tree reference
- TNDRP / `android_device_motorola_boston`
  - Secondary Boston device tree source
- twrpdtgen / `android_device_motorola_boston`
  - Generated TWRP device tree reference
- Custom ROM and recovery maintainers across the Android ecosystem
  - Shared build knowledge and recovery compatibility work

## How to use

1. Open the GitHub Actions tab.
2. Run `Universal Recovery Builder`.
3. Choose the recovery type and manifest.
4. Fill in the Boston device values or swap in another device tree.
5. Run the workflow.
6. Download the generated artifacts from the GitHub Release page.

## Release visibility

Successful builds are uploaded to GitHub Releases so they can be reviewed before further release or distribution.

## Important note

The device tree, kernel, and vendor information must match the real board configuration of the target device for a successful build. Boston-specific defaults are meant as a starting point and may need adjustment depending on the installed vendor tree and partition layout.

---

Project X Boston Recovery
Built for the Motorola Moto G Stylus 5G 2024 (`boston`) recovery community.