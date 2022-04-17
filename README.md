### about
slaptbuild is simple wrapper for managing slackbuild.org tree. This application not offically related with slackbuild.org

### installation

#### using .tgz package
grab latest version from the release tag https://github.com/zendbit/slaptbuild/releases
install using installpkg command
```
# installpkg slaptbuild-x.x.x-x86_64-arros.tgz
```

#### manual installation
the installation not required headache dependencies only need extract tool (tar), wget, git, sed, grep
- dowload source
- copy file to /usr/sbin/
- set as executable
- done!
```
# get from stable version https://github.com/zendbit/slaptbuild/archive/refs/tags/vx.x.x.tar.gz
> wget https://github.com/zendbit/slaptbuild/archive/refs/tags/v0.0.1.tar.gz
> tar -xvf v0.0.1.tar.gz
> cp slaptbuild-0.0.1/slaptbuild /usr/sbin/
> chmod +x /usr/sbin/slaptbuild
```

### slaptbuild
slaptbuild is simple wrapper for managing slackbuilds.org tree. This application not offically related with slackbuild.org

### usage
```
slaptbuild [options] [parameters]

options:
  update      : update git from slaptbuild then rebuild the db, ex: slaptbuild update
  search      : search package(s), ex: slaptbuild search zoom-linux xfce4 etc.
  install     : install package(s), ex: slaptbuild install zoom-linux xfce4 etc.
  reinstall   : reinstall package(s), ex: slaptbuild reinstall zoom-linux xfce4 etc.
  installpkg  : install package(s) directly .tgz .txz.
  remove      : remove package(s), ex: slaptbuild remove zoom-linux xfce4 etc.
  info        : show package info, ex: slaptbuild info zoom-linux
  installed   : show installed package(s), ex: slaptbuild installed [xfce4 zoom-linux etc]
  upgrade     : upgrade installed package, ex: slaptbuild upgrade
  blacklist   : blacklist package left it unmodified, ex: slaptbuild blacklist ostree gstreamer
  whitelist   : whitelist package allow to modify, ex: slaptbuild whitelist ostree gstreamer
  blacklisted : show backlisted package
```
### first time todo is update the slackbuilds tree
update command will clone current slackbuilds tree into /usr/slackbuilds
```
slaptbuild update
```

### example install inkscape from slackbuilds.org
```
slaptbuild install inkscape
```
### what todo next?
- *DONE* resolving dependencies when installing package, any suggestion? using formula like homebrew? (done with checking depedencies by read REQUIRES in .info file)
- this version only support for slackware current (slackbuilds master) aka rolling release
