
# Installation Issues (with solutions)

Everyone using a Mac should make sure they have installed
Xcode. It is included on the install DVD that came with
your Mac.

For some of you, that may be all that you need to do.  If
you are still having problems, continue reading...

## If you need to update SQLite

One of your classmates updated his version of SQLite using
MacPorts. There are disk images and installation instructions
online at this address:

http://www.macports.org/install.php

Download the appropriate disk image for your version of Mac OS X
(they have Tiger, Leopard, and Snow Leopard).  Mount the dmg,
then double-click the pkg to install it.

Once the installation finishes, you can open a Terminal and type
this command to install SQLite:

    sudo port install sqlite3

If you have any trouble, MacPorts also has a User Guide at this
address:

http://guide.macports.org/

## If you were not able to install git

If git was not available for your version of Mac OS X, you can install
it using MacPorts:

    sudo port install git-core

## If you need a new version of Ruby and cannot install RVM

MacPorts also includes Ruby 1.8.7 and RubyGems 1.3.7:

    sudo port install ruby
    sudo port install rb-rubygems


