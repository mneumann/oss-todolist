# DragonFly BSD Todos

## Kernel

- [x] Deprecate / Remove `bus_dma` filter and filterarg (like FreeBSD):

    https://leaf.dragonflybsd.org/~mneumann/0001-busdma-Remove-filter-functionality.patch

- [ ] Bring in `sys/dev/hid` from FreeBSD

- [ ] Port `sys/dev/usb/input/usbhid.c` from FreeBSD (depends on `sys/dev/hid`)

- [ ] Port `iichid.c` from FreeBSD (depends on `sys/dev/hid`)

- [ ] Make evdev the default?

- [ ] Bring in changes to `mixer` from FreeBSD
  [link][https://wiki.freebsd.org/SummerOfCode2021Projects/SoundMixerImprovements]

## Userland

## Documentation

- [ ] Make webman resposive (similar to man.openbsd.org)

- [ ] Fix man `hammer2(8)` saying that the default of `sysctl
  vfs.hammer2.cluster_writes` is 4, but it is `0`. Or is the default wrong?


