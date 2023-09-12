## Change root password
- Reboot the system
- On the GRUB 2 boot screen, use the down arrow key on your keyboard to select the rescue mode.
- Press the `E` key to interrupt the boot process.
- Go to the end of the line that starts with `linux`
- Add `init=/bin/bash` to the end of the line starting with `linux`, and change `ro` to `rw`.
- Press `Ctrl+X` to start the system with the changed parameters.
- `passwd`       //To reset the root password
- `touch /.autorelabel`       //To enable the SELinux relabeling process on the following system boot
- `exec /sbin/init`
