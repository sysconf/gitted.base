# This is a Sysconf repository
## Git subtrees

git subtree push -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree push -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master

git subtree pull -P sysconf.base git@github.com:sysconf/sysconf.base.git master
git subtree pull -P sysconf.gitted git@github.com:sysconf/sysconf.gitted.git master

