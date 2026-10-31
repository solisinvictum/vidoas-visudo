# vidoas-visudo

**This repository has moved into [vidoas](https://github.com/solisinvictum/vidoas) and is archived.**

vidoas-visudo adds `/usr/bin/visudo` as a symlink to [vidoas](https://github.com/solisinvictum/vidoas), so vidoas works as a drop-in replacement for visudo on systems without sudo (e.g. with opendoas-sudo or doas-sudo-shim).

Since vidoas 1.2.0 it is built from the vidoas repository as a split package:

- Arch Linux: install [vidoas-visudo from the AUR](https://aur.archlinux.org/packages/vidoas-visudo) (pkgbase `vidoas`).
- Other systems: `ln -s vidoas /usr/local/bin/visudo`

The old PKGBUILD in this repository was removed: it created the symlink with `$(which vidoas)` at build time (an empty link when vidoas was not installed on the build machine) and depended on opendoas-sudo only.
