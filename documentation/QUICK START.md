# FLAP Quick Start

FLAP currently targets a BIOS-based x86-64 virtual machine. VirtualBox 7 is the tested setup.

## Install in VirtualBox

1. Download `FLAP-Installer.img` into an empty folder.
2. Convert the raw installer to a VirtualBox disk:

   ```powershell
   VBoxManage convertfromraw FLAP-Installer.img FLAP-Installer.vdi --format VDI
   ```

3. Create a new 64-bit VM with at least 256 MiB of memory, BIOS boot, an IDE controller, a PS/2 keyboard, and a VBoxVGA-compatible display.
4. Attach `FLAP-Installer.vdi` as IDE primary master: port 0, device 0.
5. Create an empty dynamically allocated disk of at least 4,160 MiB and attach it as IDE primary slave: port 0, device 1.
6. Boot the VM. Confirm that the installer identifies the second BIOS disk as its target.
7. Press `I` once. Installation overwrites the target disk's boot area.
8. When `Installation complete` appears, power off the VM.
9. Detach the installer disk. Move the newly installed system disk to IDE primary master: port 0, device 0.
10. Boot FLAP. GooseFS initializes automatically on the first boot.

Never attach an important host or virtual disk as the install target.

## First commands

At the `[flap@nest /]$` prompt, try:

```text
help
ls
cd home
mkdir projects
cd projects
write hello.txt hello-from-flap
type hello.txt
pwd
fs check
carrot pq
run pkg.elf
```

Use `cd ..` to move to the parent directory. Use `Ctrl+S` to save and `Ctrl+Q` to leave GooseEdit. The [User Manual](USER%20MANUAL.MD) documents every built-in command.
