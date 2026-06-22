# FLAP User Manual

## Path rules

`/` is the root directory. A path beginning with `/` is absolute. Other paths are relative to the current directory. `.` means the current directory and `..` means its parent. GooseFS paths may be up to 95 printable ASCII characters and cannot contain spaces, `\`, or `:`.

Fresh installations include `/bin`, `/etc`, `/home`, and `/tmp`.

## General commands and their functions

help

Displays the built-in command list.

----------------------------------------------

clear

Clears the terminal.

----------------------------------------------

about

Displays a short FLAP system description.

----------------------------------------------

uname

Displays the FLAP version and architecture.

----------------------------------------------

whoami

Displays the current shell user.

----------------------------------------------

echo TEXT

Prints `TEXT` to the terminal.

----------------------------------------------

goose

Displays the FLAP goose.

----------------------------------------------

honk

Asks the kernel to honk.

----------------------------------------------

bash

Displays information about the active FLAP shell.

----------------------------------------------

cpp

Displays information about the freestanding C++ interface.

----------------------------------------------

rust

Displays information about the `no_std` Rust interface.

----------------------------------------------

reboot

Reboots FLAP.

----------------------------------------------

## Directory and file commands

pwd

Displays the current directory.

----------------------------------------------

cd

Returns to the root directory.

----------------------------------------------

cd PATH

Changes to `PATH`. Absolute paths, relative paths, `.` and `..` are supported.

----------------------------------------------

ls

Lists files and directories in the current directory.

----------------------------------------------

ls PATH

Lists files and directories in `PATH`.

----------------------------------------------

dir [PATH]

DOS-style alias for `ls [PATH]`.

----------------------------------------------

mkdir PATH

Creates a persistent directory. Its parent must already exist.

----------------------------------------------

md PATH

DOS-style alias for `mkdir PATH`.

----------------------------------------------

rmdir PATH

Removes an empty directory.

----------------------------------------------

rd PATH

DOS-style alias for `rmdir PATH`.

----------------------------------------------

files

Displays the complete GooseFS catalog using canonical paths.

----------------------------------------------

cat PATH

Displays a text file.

----------------------------------------------

type PATH

DOS-style alias for `cat PATH`.

----------------------------------------------

write PATH TEXT

Creates or replaces a file with `TEXT`. The parent directory must exist.

----------------------------------------------

edit PATH

Opens a file in GooseEdit. Use the arrow keys to move, `Ctrl+S` to save, and `Ctrl+Q` to quit.

----------------------------------------------

rm PATH

Removes a file. Use `rmdir` for directories.

----------------------------------------------

del PATH

DOS-style alias for `rm PATH`.

----------------------------------------------

copy SOURCE DESTINATION

Copies a file. Shell copies are limited to files GooseEdit can load, currently just under 256 KiB.

----------------------------------------------

move SOURCE DESTINATION

Moves or renames a file without copying its data. Directory moves are not yet supported.

----------------------------------------------

ren SOURCE DESTINATION

DOS-style alias for `move SOURCE DESTINATION`.

----------------------------------------------

fs

Displays GooseFS status and capacity.

----------------------------------------------

fs check

Checks the directory, extents, and allocation bitmap for consistency.

----------------------------------------------

fs stress

Runs the persistent 64 KiB GooseFS write/read stress test.

----------------------------------------------

fs recovery-test

Tests mount-time interrupted-allocation recovery.

----------------------------------------------

fs fragment-test

Tests non-contiguous extent allocation and cleanup.

----------------------------------------------

## Applications and processes

elf

Displays the ELF loader status and available commands.

----------------------------------------------

elf install-demo

Installs the generated demonstration application as `hello.elf`.

----------------------------------------------

run NAME

Validates and executes a static x86-64 ELF application stored in GooseFS.

----------------------------------------------

run-pair NAME NAME

Runs two ELF applications in isolated process slots.

----------------------------------------------

proc

Displays process and syscall status.

----------------------------------------------

proc test

Runs the basic ring-3 process test.

----------------------------------------------

proc fault-test

Tests containment of a user-process fault.

----------------------------------------------

proc nx-test

Tests non-executable user memory enforcement.

----------------------------------------------

proc write-protect-test

Tests user-space write protection.

----------------------------------------------

proc schedule-test

Tests cooperative scheduling between isolated address spaces.

----------------------------------------------

proc preempt-test

Tests timer-driven preemptive scheduling.

----------------------------------------------

## Hardware and memory commands

devices

Displays detected display and audio devices.

----------------------------------------------

video test

Displays a framebuffer color-bar test and returns to text mode.

----------------------------------------------

audio test

Queues an AC97 audio DMA test period.

----------------------------------------------

heap

Displays kernel heap status.

----------------------------------------------

heap test

Tests heap allocation, freeing, alignment, and coalescing.

----------------------------------------------

entropy

Displays hardware entropy status.

----------------------------------------------

entropy test

Runs the hardware CSPRNG health test.

----------------------------------------------

## Network and CARROT commands

net

Displays GooseNet status.

----------------------------------------------

net status

Displays GooseNet interfaces and packet counters.

----------------------------------------------

net up

Enables the loopback interface.

----------------------------------------------

net down

Disables the loopback interface.

----------------------------------------------

net eth0

Displays the PCnet Ethernet interface and CARROT endpoint status.

----------------------------------------------

ping 127.0.0.1

Tests the loopback interface.

----------------------------------------------

carrot

Displays CARROT transport status.

----------------------------------------------

carrot status

Displays CARROT runtime and live-connection counters.

----------------------------------------------

carrot crypto

Displays the CARROT post-quantum cryptographic profile.

----------------------------------------------

carrot wire

Displays the CARROT wire format and endpoint.

----------------------------------------------

carrot host

Displays the kernel host-interface status used by CARROT.

----------------------------------------------

carrot runtime

Displays linked CARROT runtime counters.

----------------------------------------------

carrot handshake

Displays bounded handshake reassembly counters.

----------------------------------------------

carrot handshake-test

Runs the CARROT handshake fragment-path self-test.

----------------------------------------------

carrot hybrid

Runs the hybrid X25519, ML-KEM, ML-DSA, and key-schedule self-test.

----------------------------------------------

carrot transport

Runs the authenticated encrypted-transport self-test.

----------------------------------------------

carrot pq

Runs the ML-KEM, ML-DSA, and SLH-DSA post-quantum self-test.

----------------------------------------------

carrot fs-read PATH

Reads a GooseFS file through the CARROT host source callback.

----------------------------------------------

carrot fs-write PATH TEXT

Writes a GooseFS file through the CARROT host sink callback.

----------------------------------------------

bunnynet

Displays BunnyNet status.

----------------------------------------------

bunnynet status

Displays BunnyNet message counters.

----------------------------------------------

bunnynet streams

Displays the registered BunnyNet stream identifiers.

----------------------------------------------
