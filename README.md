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

Screenshot
----------

12:15 zoobab@machina ~% sudo rshell
[sudo] password for zoobab: 
12:15 root@machina ~# cd /var/log/ttyrec 
12:15 root@machina /var/log/ttyrec# l
total 12M
-rw------- 1 root root   12 Nov 25 16:28 20111125_161301-zoobab.hist
-rw-r--r-- 1 root root  16K Nov 25 16:28 20111125_161301-zoobab.ttyrec
-rw------- 1 root root  292 Nov 25 16:27 20111125_161322-zoobab.hist
-rw-r--r-- 1 root root  28K Nov 25 16:27 20111125_161322-zoobab.ttyrec
-rw------- 1 root root  177 Dec 23 11:59 20111223_115830-zoobab.hist
-rw-r--r-- 1 root root  14K Dec 23 11:59 20111223_115830-zoobab.ttyrec
-rw------- 1 root root   36 Dec 23 12:13 20111223_121253-zoobab.hist
-rw-r--r-- 1 root root  11K Dec 23 12:13 20111223_121253-zoobab.ttyrec
-rw-r--r-- 1 root root 1.1K Dec 23 12:15 20111223_121539-zoobab.ttyrec
-rw-r--r-- 1 root root    2 Nov 24 13:26 .gitignore
-rw------- 1 root root  12M Dec 23 12:15 sudolog
12:15 root@machina /var/log/ttyrec# cat 20111125_161301-zoobab.hist
su postgres
12:16 root@machina /var/log/ttyrec# exit
12:16 zoobab@machina ~%
