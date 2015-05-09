MongoDB CLI
===========

This is a simple Bash CLI script for managing a local `mongod` instance.


Rational
--------

With the changes to MongoDB 3.x and utilizing the WiredTiger storage engine it seemed almost impossible to continue utilizing <code>[launchctl][]</code> (<code>[lunchy][]</code> in my case) for <code>[launchd][]</code> to autostart `mongod` and keep it running on OS X. So this script was created to handle launching my local `mongod` instance and has grown a bit and I still have some plants for it. Thus here it is on GitHub as open source. Hopefully it will be found useful to others.  :-)


Installation
------------

From within the cloned repo run:

```
./mongodb --install
```


Usage
-----

### Conventions

* Commands are for managing `mongod`, etc.
* Switches are for managing MongoDB CLI.

### Examples

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

# Show the version of MongoDB CLI
mongodb --version
```

### `ostype`

This is a simple Bash script to get general platform information. Included as a helper for `mongodb`. It's not as detailed as some that are available as the deep Exim os-type script.


ToDo
----

* [x] Add `--install` switch to auto link the scripts
* [ ] Stuff, reasons, &hellip;

[launchctl]:https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/launchctl.1.html
[launchd]:http://en.wikipedia.org/wiki/Launchd
[lunchy]:https://github.com/eddiezane/lunchy
