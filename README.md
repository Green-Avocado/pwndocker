# pwndocker

Create a lightweight docker container for solving CTF challenges

## Setup

### Prerequisites

Requires that docker is installed and running.

### ArchLinux

```
makepkg -si
```

### Other

```
make install
```

## Usage

### Download glibc deb file

Use `libc-fetch LIBC` to download a matching deb file from the Ubuntu archives.

### Create docker container

Run `sudo pwndocker EXEC_CMD` from your working directory.
The binary should be given as a relative path.

Optionally pass a glibc deb file as a second argument.

### Connect to docker container

Connect to socat using:

```
$ nc localhost 1337
```

### Connect to gdbserver

Connect to the gdbserver using:
```
(gdb) target extended-remote localhost:13337
```

## Uninstall

```
make remove
```
