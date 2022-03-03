# gentoo-vmkernel
Minimal kernel configs for running Gentoo in a virtual machine

# Usage
- su
- eselect kernel list
- eselect kernel set *X*
- cd /usr/src/linux
- make mrproper
- rm .config
- curl -o /usr/src/linux/.config https://raw.githubusercontent.com/speediegamer/gentoo-vmkernel/main/config-vm
- make olddefconfig
- emerge -a app-arch/lz4
- make -j$(nproc)
- mount /dev/sdX /boot
- make install
