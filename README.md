# FLAP Kernel

Simple x86-64 I made, includes my *unaudited* post-quantum encrypted transport protocol, CARROT.

Currently in-development. A lot will change.

Source code will be released when I'm comfortable with it. For now, this repo only contains the installer image, optional rich presence binary, and documentation.

## Requirements

- VirtualBox 7

Current features include

- A bootloader
- Ring-3 process isolation
- an ELF loader
- PQ key generation
- a persistent filesystem
- directories and file management
- an OS installer
- optional Discord rich presence (on host machine while FLAP is running on VirtualBox)
- video and audio output
- an included package manager (run pkg.elf)
- Networking
- Quake II Port (separate repo)

Please don't distribute as yours. Don't use for sensitive operations, obvious things are obvious.

Quick Start and User Manual are in "documentation." folder. Please read them to avoid confusion.

The optional prebuilt Discord rich presence companion is in the "Discord Rich Presence" folder. Run the EXE on the host machine while FLAP is running in VirtualBox.
