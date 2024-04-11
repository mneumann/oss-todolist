# DragonFly BSD (Ideas/Todo's)

## Kernel

- [x] Deprecate / Remove `bus_dma` filter and filterarg (like FreeBSD):
  [See commit](https://gitweb.dragonflybsd.org/dragonfly.git/commit/030b0c8c4cf27c560ccec70410c8e21934ae677d)

- [x] psm: Fix spurious mouse jumps similar to what is reported
  [here][bug-psm-spurious] and this [commit][active-aux-port-mux] related to
  active AUX port multiplexing.

  https://lists.dragonflybsd.org/pipermail/kernel/2024-April/336558.html

  Waiting for feedback/testing before merging.

- [x] Figure out how to make the touchpad work on Panasonic Letsnote CF-SV
      Works with above patches.

- [ ] Port uvideo from NetBSD or OpenBSD (uvc "webcam")

- [ ] Bring in `sys/dev/hid` from FreeBSD

- [ ] Port `sys/dev/usb/input/usbhid.c` from FreeBSD (depends on `sys/dev/hid`)

- [ ] Port `iichid.c` from FreeBSD (depends on `sys/dev/hid`)

- [ ] Make evdev the default?

- [ ] Bring in changes to `mixer` from FreeBSD
  [link](https://wiki.freebsd.org/SummerOfCode2021Projects/SoundMixerImprovements)

- [ ] Figure out why OpenGL is broken on i915 (UHD Graphics 620)

- [ ] Bring in some ELF-loader related changes from FreeBSD into
      our bootloader and kernel. Loading i915.ko currently fails with
      "readin failed".

## Userland

- [ ] Fix dport editors/helix:
      https://github.com/DragonFlyBSD/DeltaPorts/blob/master/ports/editors/helix/Makefile.DragonFly

## Documentation

- [ ] Make webman resposive (similar to man.openbsd.org)

- [x] Fix man `hammer2(8)` saying that the default of `sysctl
  vfs.hammer2.cluster_writes` is 4, but it is `0`. Or is the default wrong?


[bug-psm-spurious]: https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=231058
[active-aux-port-mux]: https://svnweb.freebsd.org/base?view=revision&revision=340913
