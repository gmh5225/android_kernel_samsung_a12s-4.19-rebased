# Rebased Galaxy A12s Kernel
## How to build
### 1. Clone this repository
```
git clone https://github.com/rsuntk/android_kernel_samsung_a12s-4.19-rebased.git rebaseda12s && cd rebaseda12s
```
### 2. Edit arch/arm64/config/(devicename)_defconfig 
### 3. Get this [build script](https://github.com/rsuntk/kernel-build-script) or
```
make -C $(pwd) O=$(pwd)/out KCFLAGS=-w CONFIG_SECTION_MISMATCH_WARN_ONLY=y (devicename)_defconfig && make -C $(pwd) O=$(pwd)/out KCFLAGS=-w CONFIG_SECTION_MISMATCH_WARN_ONLY=y
```
### 3. Check directory out/arch/arm64/boot/Image or Image.gz
### 4. Put Image.gz/Image to Anykernel3 zip, don't forget to modify the boot partition path in anykernel.sh
### 5. Done, enjoy.

## Credit
- [Physwizz](https://github.com/physwizz) for OEM kernel source
- [Rissu](https://github.com/rsuntk)
