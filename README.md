# Embedded Linux Basics

This repo is a small guide + playground for learning the basics of  
**Buildroot, Kernel, and Embedded Linux setup**.  

It is not production code.  
It is more like step-by-step notes that I followed when learning.

---

## What’s inside

- `docs/` → Notes in plain words, one topic per file
- `configs/` → Example Buildroot + Kernel configs
- `hello-app/` → A tiny C program built with a Makefile

---

## Quick Start (QEMU target)

1. Clone Buildroot:
   ```sh
   git clone https://github.com/buildroot/buildroot.git
   cd buildroot
   ```

2. Copy provided defconfig:
   ```sh
   cp ../configs/buildroot_defconfig .config
   ```

3. Build:
   ```sh
   make
   ```

4. Boot in QEMU:
   ```sh
   qemu-system-x86_64 -kernel output/images/bzImage \
                      -drive file=output/images/rootfs.ext2,format=raw \
                      -append "root=/dev/sda console=ttyS0" -serial stdio
   ```

---

## Why this repo

I wanted one place with all my beginner notes about embedded Linux.  
It starts with Buildroot, then kernel basics, then rootfs, then  
how to add a custom C program, and finally how to run everything in QEMU.  

---

## License

MIT – use however you like.
