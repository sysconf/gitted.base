# This is a Sysconf repository

This repository builds a basic Gitted system.
You can build the machine or setup an existing one, for example:
```
./gitted-target init lxc:my-container
./gitted-target init dockerfile:../docker-definition/
./gitted-target init ssh:server.com
```


## Git subtrees

These Sysconf profiles are maintained externally.

Here is how to pull changes from upstream:
```
git subtree pull -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree pull -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master
```

To push changes upstream (change with your own clone):
```
git subtree push -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree push -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master
```


## How this repository was built

```
git init my-app
cd my-app
git checkout -b sysconf/master
cat <<EOF >README.md
# This is a Sysconf repository
## Git subtrees

git subtree push -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree push -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master

git subtree pull -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree pull -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master
EOF
git add README.md
git commit -m "initial commit"

git subtree add -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master
git subtree add -P sysconf.base git@github.com:sysconf/sysconf.base.git master
mkdir actual
echo sysconf.gitted >actual/deps

ln -s sysconf.base/tree/usr/bin/sysconf-target
ln -s sysconf.gitted/tree/usr/bin/gitted-target
echo compiled/ >.gitignore

git add actual sysconf-target gitted-target .gitignore
git commit -m "gathered sysconf profiles"
```


## Author

* Jean-Francois Gigand <jf@geonef.fr> @jfgigand
