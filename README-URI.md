nix build /mnt/data/general/jetpack-nixos#flash-orin-nano-super-devkit -vL --cores 10

sudo ./result/bin/initrd-flash-orin-nano-devkit

sudo dd if=./result/iso/nixos-minimal-25.11.20260118.77ef7a2-aarch64-linux.iso  of=/dev/sdb bs=1M oflag=sync status=progress
