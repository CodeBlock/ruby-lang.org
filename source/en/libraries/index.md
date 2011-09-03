---
layout: page
title: "Libraries"
---

As most programming languages, Ruby leverages a wide set of third-party
libraries.

Most of them are released in the form of a **gem**. [**RubyGems**][1] is
a Ruby packaging system designed to facilitate the creation, sharing and
installation of libraries (in some ways, it is a distribution packaging
system similar to, say, `apt-get`, but targeted at Ruby software). Ruby
1.9 comes with RubyGems by default, while previous Ruby versions require
to [install it by hand][2].

Some other libraries are released as archived (.zip or .tar.gz)
directories of **source code**. Installation processes may vary,
typically a `README` or `INSTALL` file is available with instructions.

Let’s take a look at finding libraries and installing them for your own
use.

## Finding libraries

The main place where libraries are hosted is [**RubyGems.org**][3],
providing Ruby libs as gems. You may browse the website directly, or use
the `gem` command.

Using the `gem search -r` command, you can inspect RubyGems repository.
For instance, `gem search -r rails` will return a list of Rails-related
gems. Without the `remote` (`-r`) option, you would perform a local
search through you installed gems. To install a gem, use `gem install
[gem]`. Browsing installed gems is done with `gem list`. For more
information about the `gem` command, see below or head to
[RubyGems’ docs][1].

There are other source of libraries though. [RubyForge][4] used to be a
popular home for Ruby libraries, but last years saw the rise of
[**Github**][5] as one of the main ruby-related content repository. Most
often a gem source code will be hosted on Github while being published
as a fully-fledged gem to RubyGems.org.

The [Ruby Application Archive][6] (or RAA) is a directory of all manner
of Ruby software, categorized by function, but it is not quite used
anymore. You probably don’t want to go there.

## A few more words about RubyGems

Here is a quick review of the `gem` command for your daily use.
[More detailed documentation][7] is available, covering all aspects of
this packaging system.

### Searching among available gems

The **search** command can be used to look for gems, based on a string.
Gems which names contain the specified string will be listed in return.
For instance, to search for the “html”-related gems:

    $ gem search -r html

     *** REMOTE GEMS ***

     html-sample (1.0, 1.1)
        A sample Ruby gem, just to illustrate how RubyGems works.

The `--remote` / `-r` flag indicates that we want to inspect the
official RubyGems.org repository. Without this flag, you would perform a
local search (among your installed gems).

### Installing a gem

Once you know which gem you would like to **install**, for instance the
popular Rails:

    $ gem install rails

You can even install just a certain version of the library, using the
`--version` / `-v` flag:

    $ gem install rails --version 3.0

### Listing all gems

For a complete **list** of all gems available on RubyGems.org:

    $ gem list -r

To list only local gems:

    $ gem list

### Help!

Documentation is available inside your terminal:

    $ gem help

For instance, `gem help commands` is very useful as it outputs a list of
all `gem`’s commands.

### Crafting your own gems

[RubyGems.org][8] has several guides about this topic. You may also want
to investigate on [Bundler][9], a generic tool which helps you manage an
application’s dependencies and may be used along RubyGems.

[1]: http://docs.rubygems.org
[2]: http://rubygems.org/pages/download
[3]: http://rubygems.org
[4]: http://rubyforge.org/
[5]: http://github.com
[6]: http://raa.ruby-lang.org/
[7]: http://docs.rubygems.org/
[8]: http://guides.rubygems.org
[9]: http://gembundler.com
