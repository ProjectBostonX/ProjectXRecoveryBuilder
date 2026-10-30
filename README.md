# Project X Boston Recovery

Project X Boston Recovery is a Boston-specific GitHub Actions recovery builder for the Motorola Moto G Stylus 5G 2024, codename `boston`.

This repository is configured for a Team Win Recovery Project (TWRP) build using the Boston device tree and defaults for this device.

## Boston defaults

- Recovery type: `twrp`
- Manifest URL: `https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git`
- Manifest branch: `twrp-12.1`
- Device tree URL: `https://github.com/PizzaG/android_device_motorola_boston.git`
- Device tree branch: `TWRP`
- Device path: `device/motorola/boston`
- Device name: `boston`
- Makefile: `twrp_boston`
- Build target: `recovery`

## Brand and creator customization for Boston

To make your recovery image display `Project X Boston` and your creator name in the device/recovery metadata, add the branding values inside the Boston device tree before building.

The most relevant file is the TWRP makefile in the Boston device tree:

- `device/motorola/boston/twrp_boston.mk`

Use values like this:

```make
PRODUCT_DEVICE := boston
PRODUCT_NAME := ProjectXBoston
PRODUCT_BRAND := ProjectX
PRODUCT_MODEL := Project X Boston
PRODUCT_MANUFACTURER := ProjectXGang
PRODUCT_RELEASE_NAME := Project X Boston
```

Then copy the custom build metadata into the device tree’s `system.prop` or `BoardConfig.mk` for recovery UI display and build metadata:

```make
TW_DEVICE_VERSION := Project X Boston by Your Name
```

And optionally:

```properties
ro.product.model=Project X Boston
ro.product.name=ProjectXBoston
ro.vendor.product.model=Project X Boston
```

These values are what make the build show the project and creator details in the recovery environment, when TWRP is built from your Boston device tree.

## How to run the build

1. Open the repository on GitHub.
2. Go to the Actions tab.
3. Select `Recovery Build`.
4. Click `Run workflow`.
5. Use the Boston defaults listed above.
6. Wait for the build to finish and download the recovery image from the release output.

## Notes

- The GitHub Actions workflow is only the builder.
- The actual custom name you want shown on the device must be added to the Boston device tree before the recovery image is built.
- The device tree, kernel, vendor configuration, and board files must match the real Boston hardware for a working build.

---

Project X Boston Recovery
Built for the Motorola Moto G Stylus 5G 2024 (`boston`) recovery community.
