# Buildroot Setup

- Get buildroot source from official repo
- Copy the sample defconfig (see configs folder)
- Run `make menuconfig` if you want to tweak settings
- Run `make` (this takes a while)
- When done, you will find:
  - `bzImage` → kernel image
  - `rootfs.ext2` → root filesystem
