Place the `15_iso` file into /etc/grub.d/ .

Place iso images into subfolders with the distributions name in `/iso` . (You can customize the search paths in the case ... esac block near the end of the script)

When runnung `grub-mkconfig -o /boot/grub/grub.cfg` or `update-grub` (depending on your distribution) grub will detect isos and create menu entries for booting them via loop devices. 

Supported isos are:
* Ubuntu and variants like Kubuntu, etc.
* Desinfect 2017 (ubuntu baased)
* Manjaro
* Grml
* ArchLinux