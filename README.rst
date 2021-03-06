nose-memory-grinder
===================

Captures the memory usage for each of your test cases, looking for memory
leaks.

`nose-memory-grinder` is a nose_ plugin which displays the memory usage of
each test case instead of just "ok", "FAIL" or "ERROR". It captures the memory 
usage before and after each test case, and will fail the test case if usage 
increases by 5% or more.

.. _nose: https://nose.readthedocs.org/en/latest/

Installation
============

Get the bleeding-edge, unreleased version::

  pip install -e git://github.2ndsiteinc.com/ctroup/nose-memory-grinder.git#egg=nose-memory-grinder

Use
===

The easy way::

  nosetests --with-nose-memory-grind

TODO
====

- The threshold for test failure should be configurable. You should be able to
  fail the test by specifying a percentage increase (ie: 10%) or ``x`` bytes
  as well

- Output should be configurable

- Telling nose to stop on the first failure (ie: ``-x``) doesn't work right now.

Author
======

Christopher Troup, after discovering terrible memory leaks that automated tooling should have caught!

License
=======

GPL