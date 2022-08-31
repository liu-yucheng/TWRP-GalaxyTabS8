## TWRP Device Tree 

- For Samsung Galaxy Tab S8.
- Branch `main` is for Android 12.1.
- Tested on models: X700 (WiFi version, CSC: CHN).

## Compilation Preparation

- Open a terminal and `mkdir` a compilation directory.
- `cd` to the compilation directory.
- Run exactly the following commands in the terminal.

```bash
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
repo sync
mkdir ./device/samsung
mkdir ./device/samsung/gts8
```

- `cd` to the `./device/samsung/gts8` directory.
- Clone this GitHub repository by running `git clone <link-to-this-repository>`.
- Move all the files in the cloned repository to the `./device/samsung/gts8` directory.
- Now, the compilation directory is ready for the compilation.

## Compilation

- Open a terminal and `cd` to the compliation directory.
- Run exactly the following commands in the terminal.

```bash
export ALLOW_MISSING_DEPENDENCIES=true
. ./build/envsetup.sh
lunch twrp_gts8-eng
make recoveryimage
```

- Find the compiled recovery images in the `./out/target/product/gts8` directory.

# Kernel Source
https://github.com/mohammad92/android_kernel_samsung_sm8450
