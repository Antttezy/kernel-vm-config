# Linux kernel VM .config file

Linux kernel configuration to run as a Guest. I removed as much drivers as I could to minimize size and build time, but it still has a lot of  things to remove.
It works fine inside a KVM/QEMU VM. Virtio, VirtualBox, and VMWare graphics drivers are included.

Usage:
 - ```git clone https://github.com/Antttezy/kernel-vm-config.git```
 - Copy .config to your linux source code directory
 - Run ```make``` (with build parameters (i.e. ```-j$(nproc)```))
 
 What I removed:
  - A lot of LAN drivers (Because only virtual adapters are used)
  - All USB ethernet, USB Wi-Fi and USB bluetooth drivers
  - WAN and WWAN drivers
  - Touchscreen support
  - Wireless devices
  - NVidia, AMD, and Intel graphics (because virtual adapter is used)
  - BTRFS Support
  - NVME drivers
 
