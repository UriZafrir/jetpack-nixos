nix build /mnt/data/general/jetpack-nixos#flash-orin-nano-super-devkit -vL --cores 10

sudo ./result/bin/initrd-flash-orin-nano-devkit
