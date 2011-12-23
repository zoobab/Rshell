Rshell, the recorded shell
==========================

About
-----

Rshell is a recorded shell based on TTYRec. It saves the output of the console,
and allows to track what your users have been changing by auditing their root
sessions.

Dependencies
------------

ttyrec, date, bash or zsh

Install
-------

1. As root, create a directory named /var/log/ttyrec:
    mkdir -pv /var/log/ttyrec

2. Copy rshell to somewhere in your path (in this example, /usr/local/bin/):
    cp -v rshell /usr/local/bin/


Todo
----

1. Make an /etc/rshell/rshell.conf config file
2. Add the sudoers config
