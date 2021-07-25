### installation
the installation not required headache dependencies only need extract tool (tar), wget
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
slaptbuild is simple wrapper for managing slackbuild.org tree. This application not offically related with slackbuild.org

### usage
```
slaptbuild [options] [parameters]

options:
  update    : update git from slaptbuild then rebuild the db, ex: slaptbuild update
  search    : search package(s), ex: slaptbuild search zoom-linux xfce4 etc.
  install   : install package(s), ex: slaptbuild install zoom-linux xfce4 etc.
  remove    : remove package(s), ex: slaptbuild remove zoom-linux xfce4 etc.
  info      : show package info, ex: slaptbuild info zoom-linux
  installed : show installed package(s), ex: slaptbuild installed [xfce4 zoom-linux etc]
  upgrade   : upgrade installed package, ex: slaptbuild upgrade
```

### example
```
slaptbuiild install dos2unix double-conversion potrace gdl inkscape
```
