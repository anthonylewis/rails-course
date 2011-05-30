# Issues with Rake

The next release of Rails (3.0.8) will correct the problem with rake.  In the mean time, there are a few things you can do to correct this yourself.

## Downgrade rake

First, add the following line in your Gemfile:

    gem 'rake', '0.8.7'

Then execute the `bundle` command to update the rake gem:

    bundle update rake

Finally, uninstall rake version 0.9.0:

    sudo gem uninstall rake -v 0.9.0

Remember if you are using Windows you do not have to type sudo.

## If you are using rvm

There might be a slight complication if you are using rvm.  You may need to uninstall rake 0.9.0 from the global gemset, like this:

    rvm use @global
    gem uninstall rake -v 0.9.0

The global gemset is shared by all other gemsets. So even if you uninstall rake 0.9.0 in your current gemset, it may still be present.

