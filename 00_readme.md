Place the `15_iso` file into /etc/grub.d/ .

Place iso images into subfolders with the distributions name in `/iso` . (You can customize the search paths in the case ... esac block near the end of the script)

When runnung `grub-mkconfig -o /boot/grub/grub.cfg` or `update-grub` (depending on your distribution) grub will detect isos and create menu entries for booting them via loop devices. 

Supported isos are:
* Ubuntu and variants like Kubuntu, etc.
* Desinfect 2017 (ubuntu baased)
* Manjaro
* Grml
* ArchLinux
* Any iso that has a `loopback.cfg` grub can read (usually /boot/grub/loopback.cfg)

Dependencies:
* libcdio (needs `iso-info` for getting file list of iso in some cases)

For the EFI/bios coloring just add the 01_color file and this in `/etc/default/grub`:
```
GRUB_COLOR_EFI_NORMAL="light-red/black"
GRUB_COLOR_EFI_HIGHLIGHT="light-cyan/red"
export GRUB_COLOR_EFI_NORMAL GRUB_COLOR_EFI_HIGHLIGHT
```