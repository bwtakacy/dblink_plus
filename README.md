dblink_plus
=======
This tools enables to connect from PostgreSQL server to other databases.
Currently it supports to connect to PostgreSQL, Oracle Database, MySQL, Sqlite3.
This is a repository for development. The formal repo is git://git.code.sf.net/p/interdbconnect/code.

Branches
---
* master [![Build Status](https://travis-ci.org/bwtakacy/dblink_plus.svg)](https://travis-ci.org/bwtakacy/dblink_plus)

Quick Introduction
---
With dblink_plus, users can throw SQL to external databases like below:

    =# BEGIN;
    =# SELECT dblink.connect('ora_conn', 'server_oracle', false);
    =# SELECT dblink.query('ora_conn', 'SELECT c1, c2 FROM tbl') AS t(c1 int, c2 text); -- get rows
    =# SELECT dblink.exec('ora_conn', 'UPDATE tbl SET c3 = 999 WHERE c1=1'); -- modify rows
    =# COMMIT;

Please take a look to documentation http://interdbconnect.sourceforge.net/dblink_plus/dblink_plus-ja.html .

