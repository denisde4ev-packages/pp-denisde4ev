
# "universal" sel-building package script

* "universal" *will* be able to build for Arch and Alpine build systems
* requires `thepkg` for option `-i`

```
$ USER=root fakeroot ./THEPKGBUILD -i
 -> pkgver...
 -> source...
 -> package...
 -> tar...
 -> thepkg...
ERROR: ld.so: object 'libfakeroot.so' from LD_PRELOAD cannot be preloaded (cannot open shared object file): ignored.
Password: 
 -> Extracting the pkg 'pp-denisde4ev'...
mkdir: created directory '/var/db/thepkg/pp-denisde4ev'
usr/
usr/bin/
usr/bin/pp
usr/share/
usr/share/man/
usr/share/man/man1/
usr/share/man/man1/pp.1
```

```
$ pp --help | head -2
Usage: pp v0.3.0(denisde4ev)
  * STDIN | pp > output -- See pp(1) for details and examples
```

```
$ alias sudo='su -c "\"\$@\"" -- root sh'
$ sudo thepkg del pp-denisde4ev
Password: 
 -> Removing the pkg 'pp-denisde4ev'...
removed 'usr/share/man/man1/pp.1'
removed 'usr/bin/pp'
removed '/var/db/thepkg/pp-denisde4ev/manifest'
removed '/var/db/thepkg/pp-denisde4ev/version'
rmdir: removing directory, '/var/db/thepkg/pp-denisde4ev'
```
