#  Mac-NTFS-3G-Loader

This project provides a file system bundle to allow NTFS volumes to be mounted with [NTFS-3G](https://www.tuxera.com/community/open-source-ntfs-3g/) and [FUSE](https://osxfuse.github.io), which is a solution for writable NTFS volumes on macOS.

The bundle is named after Tuxera since NTFS-3G is the community version of their product Tuxera NTFS.

## Caveats

At the moment, this bundle **ONLY** contains metadata and necessary scripts. The drivers are **NOT** included and their paths are hard-coded. Thus you should use Homebrew NTFS-3G.

## Installation

### Homebrew
Please follow the instructions in <https://brew.sh>.

### FUSE
```bash
$ brew cask install osxfuse
```

### NTFS-3G
```bash
$ brew install ntfs-3g
```

### Filesystem Bundle

- Download and unzip the bundle from [releases](https://github.com/hguandl/Mac-NTFS-3G-Loader/releases).

- Put `tuxera_NTFS.fs` to `/Library/Filesystems`.
```bash
$ sudo mv tuxera_NTFS.fs /Library/Filesystems
```

- Set permissions
```bash
$ sudo chown -R root:wheel /Library/Filesystems/tuxera_NTFS.fs
```

- Reboot
