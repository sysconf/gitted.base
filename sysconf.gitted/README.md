# Gitted: Import/export machine sate through git push/pull

* See new official website: http://gitted.io/
* Official Git repository on GitHub: https://github.com/sysconf/sysconf.gitted

Gitted solves 2 problems:

* website software *installation* (for example, a CMS like Drupal) can
  be complex to install and configure, because of the dependencies
  that are needed on the system ;

* website *state* (for example, MySQL data) is difficult to manage:
  doing simple database dumps are often not enough, if it needs file
  uploads, applicative plugins, etc.

To address these issues, Gitted helps you manage the website
software *and* the changing data as one unique thing, which is stored
as a GIT repository.


## Documentation

* See official website: **http://gitted.io/**
  * [Setup a new Gitted Sysconf repository](http://gitted.io/tutorial/setup-gitted-sysconf/)
* Documentation in [doc/](doc/) is OBSOLETE (related to v0, now gitted.io is about v1):


## Authors & history

This tool was was designed and implemented is maintained so far by
Jean-Francois Gigand <jf@gigand.fr>.

* Early 2014: first version of [the script](tree/usr/bin/sysconf)
* Spring 2014: released as Free Software on GitHub
* Early 2015: rewrite from v0 to v1 (with [gitted-target](tree/usr/bin/gitted-target))
