==============
Version 4.5.16
==============

Version 4.5.16 of mod_wsgi can be obtained from:

  https://codeload.github.com/GrahamDumpleton/mod_wsgi/tar.gz/4.5.16

Bugs Fixed
----------

* The ``WSGIDontWriteBytecode`` option wasn't available when using Python 3.3
  and later. This feature of Python wasn't in initial Python 3 versions, but
  when was later added, mod_wsgi was updated to allow it.

* The feature behind the ``startup-timeout`` option of ``WSGIDaemonProcess``
  was broken by prior fix related to feature in 4.5.10. This meant the option
  was not resulting in daemon processes being restarted when the WSGI script
  file could not be loaded successfully by the specified timeout.
