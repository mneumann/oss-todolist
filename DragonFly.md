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

- [x] Make evdev the default?

- [ ] Bring in changes to `mixer` from FreeBSD
  [link](https://wiki.freebsd.org/SummerOfCode2021Projects/SoundMixerImprovements)

- [ ] Figure out why OpenGL is broken on i915 (UHD Graphics 620)

- [ ] Bring in some ELF-loader related changes from FreeBSD into
      our bootloader and kernel. Loading i915.ko currently fails with
      "readin failed".

- [ ] setting `boot_verbose="NO"` in /boot/loader.conf
      enables verbose booting as `howto_names` only checks if a value
      is set or not.

- [ ] Bring in some changes for `acpi_panasonic`: https://patchwork.kernel.org/project/linux-acpi/patch/20090114060117.GM4791@prithivi.gnumonks.org/

- [ ] i915 - loading DMC firmware fails. The modules are registered under different
      names in port devfw-i915 than refered to in the kernel driver.

## Ports

- [ ] Fix dport editors/helix:
      https://github.com/DragonFlyBSD/DeltaPorts/blob/master/ports/editors/helix/Makefile.DragonFly

- [ ] Bring up-to-date version of Rust into dports

- [ ] adb from android-tools does not work

- [ ] Create a port for ART: https://bitbucket.org/agriggio/art

## Documentation

- [ ] Make webman resposive (similar to man.openbsd.org)

- List all past releases on homepage.

- [x] Fix man `hammer2(8)` saying that the default of `sysctl
  vfs.hammer2.cluster_writes` is 4, but it is `0`. Or is the default wrong?


[bug-psm-spurious]: https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=231058
[active-aux-port-mux]: https://svnweb.freebsd.org/base?view=revision&revision=340913
