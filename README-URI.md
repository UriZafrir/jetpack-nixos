#see options
nix flake show .

nix build /mnt/data/general/jetpack-nixos#flash-orin-nano-super-devkit -vL --cores 10

sudo ./result/bin/initrd-flash-orin-nano-devkit

#only iso
nix build .#iso_minimal

#from github (slower)
nix build github:anduril/jetpack-nixos#iso_minimal

#for flashing
nix build .#flash-orin-nx-super-devkit

sudo dd if=./result/iso/nixos-minimal-25.11.20260118.77ef7a2-aarch64-linux.iso  of=/dev/sdb bs=1M oflag=sync status=progress
