# LXD Package Testing
using lxd to test packages in a clean environment on gentoo

# Install LXD

I've installed LXD with the following use flags
```
[ebuild   R   ~] app-emulation/lxd-4.0.1::gentoo  USE="ipv6 nls" 
```

### Super quick note of lxc vs lxd
##### commands
All technical jargon about their methodology aside, any command of the form `lxc-copy` is an **lxc** command and a command of the form `lxc copy` is an **lxd** command.  
You can check that by doing
```
$ qfile lxc-copy
app-emulation/lxc: /usr/bin/lxc-copy

$ qfile lxc
app-emulation/lxd: /usr/bin/lxc
```
##### images
lxc images and lxd images are not compatible with each other right of the bat, there needs to be work done to change image formats.
```
$ lxc-to-lxd --help
Command line client for container migration

Usage:
  lxc-to-lxd [flags]

Flags:
      --all          Import all containers
      --containers   Container(s) to import
      --debug        Print debugging output
      --delete       Delete the source container
      --dry-run      Dry run mode
  -h, --help         Print help
      --lxcpath      Alternate LXC path (default "/var/lib/lxc")
      --rsync-args   Extra arguments to pass to rsync
      --storage      Storage pool to use for the container
      --version      Print version number
```

# lxd init

# lxd config

# Get a gentoo image 

# Fix /etc/init.d/devfs to get /dev/shm

# enjoy
