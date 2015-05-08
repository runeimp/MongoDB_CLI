MongoDB CLI
===========

This is a simple CLI script for managing a local `mongod` instance.


Installation
------------

Ensure that `mongodb` is copied or linked into your path. On Linux systems be sure to include the `ostype` script as well so that the `mongodb` script can handle shutdown appropriately.


Usage
-----

```
# Get MongoDB CLI help
mongodb help

# Start a mongod instance
mongodb start

# Stop a mongod instance
mongodb stop

# See which storage engine is being used with your mongod instance
mongodb storage

# Show the version of mongod installed
mongodb version
```


Rational
--------

With the changes to MongoDB 3.x and utilizing the WiredTiger storage engine it seemed almost impossible to continue utilizing [launchctl][] ([lunchy][] in my case) for [`launchd`][] to autostart `mongod` and keep it running. So this script was created to handle launching my local `mongod` instance and has grown a bit and I still have some plants for it. Thus here it is on GitHub as open source. Hopefully it will be found useful to others.  :-)


ToDo
----

* [ ] Add `setup` command to auto link the scripts
* [ ] &hellip;

[launchctl]:https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/launchctl.1.html
[launchd]:http://en.wikipedia.org/wiki/Launchd
[lunchy]:https://github.com/eddiezane/lunchy