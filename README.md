Bolt Documentation Site & Content
=============================

This repository is for both the site, and content, of
[Bolt][bolt], and should be considered a counterpart of the
[Bolt repository][repo].

The documentation uses the
[Markdown][markdown] format.

There is no need to build anything to generate HTML. We parse the markdown with
PHP.

Working on this repository is advised with `git` version 2.5 or later.

Updating Documentation
----------------------

The repository uses branches to group documentation relevant to each version in
the format of `release/<version>`.

Changes should be PR-ed against the *lowest* relevant version and will then be
merged down into higher version branches as required.

e.g. if you're fixing a typo that exists in the same Markdown file in both
version 3.0 as well as in 3.1, you would checkout `release/3.0` and submit your
PR against that branch.

Local site set-up
-----------------

To run the site locally you need to complete the following steps:

  * Create the repository with `git clone`
  * Create worktrees for required versions
  * Run `composer update` to install required vendor libraries

An example that sets up work trees for both 2.2 & 3.0 is:

```
git clone git://github.com/bolt/docs.git bolt-docs
cd bolt-docs
git checkout site
git worktree add var/versions/2.2 release/2.2
git worktree add var/versions/3.0 release/3.0
composer update
```

Finally if you wish to use the built-in PHP web server, it can be run from the
`bolt-docs/` folder, pointing to `web/` as the document root.

```
php -S 0.0.0.0:8000 -t web web/index.php
```

[bolt]: http://docs.bolt.cm/
[markdown]: http://daringfireball.net/projects/markdown/
[repo]: https://github.com/bolt/bolt

