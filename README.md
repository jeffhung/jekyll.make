jekyll.make
===========

The `jekyll.make` file is a `Makefile` module for maintaining a [Jekyll][jekyll] site.


Usage
-----

Use the `-f` option to load and use `jekyll.make`:

	$ make -f jekyll.make
	Usage: make [ TARGET ... ]
	
	These jekyll-* make targets help you manage a Jekyll site.
	
	  jekyll-help       - show this help message
	  jekyll-init       - bootstrap a virtualenv runtime environment
	  jekyll-publish    - publish articles
	  jekyll-theme T    - change Jekyll theme to M

Or you can write your main makefile like following to merge `jekyll.make` make
targets in:

	.PHONY: all
	all: jekyll-help
	
	...
	
	include jekyll.make


Install
-------

The installation depends on where you plan to publish the site to:

### [Github Pages][gh-pages]

The `jekyll.make` file will assume it is contained in a git repository cloned
from [github][github]. It will detect the repository name on github, and
publish it as an user/organization site or as a project site.

  * The base URL for an user/organization site would be: http://username.github.io
  * The base URL for a project site would be: http://username.github.io/project

#### Publish as an user/organization site

To publish to Github Pages as an user/organization site, please fork the
`jekyll.make` project directly on Github to a project named `whatever` under
your account.

For example, fork `jekyll.make` to a project called `blog`. The resulting site
will be located at http://username.github.io/blog.

#### Publish as a project site

To publish to Github Pages as a project site, please fork the `jekyll.make`
project directly on Github to a project named `username.github.io` under your
account.

For example, fork `jekyll.make` to a project called `username.github.io`. The
resulting site will be located at http://username.github.io/.


[jekyll]:   http://jekyllrb.com/
[gh-pages]: https://pages.github.com/
[github]:   https://github.com/

