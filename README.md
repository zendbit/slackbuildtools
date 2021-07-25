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
