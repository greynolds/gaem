# sibtest

gaem is a leiningen plugin for managing appengine-magic applications.
It replaces the plugin functionality of the appengine-magic package.

## Installation

Download from

## Usage

This plugin tries to run the whole show from project.clj.

**WARNING** Alpha software.  Seems to work for me but needs more
  bullet-proofing.  I wouldn't try to use it with existing projects.
  But it is suitable for exploring appengine-magic, not to mention
  leiningen.  Documentation will have to wait, in the meantime the
  code should be clear enough provided you understand leiningen
  templates and plugics, and mustache.

Step 1.  Create a new appengine-magic project by using the gaem template:

    $ lein new gaem myapp:app-id /path/to/gae/sdk

Here myapp is the clojure appname and app-id is the GAE application ID.

Step 2.  Configure the app - generate and install appengine-web.xml and web.xml, and install other source files to the war tree.

    $ cd myapp
    $ lein gaem config

Step 3.  Mess around wid' it.

    $ lein repl

This starts the repl and launches the webapp.  You can nrepl into the
repl, or you can edit the code and then do something like
(compojure.core/compile 'myapp.user) to load the new code for the user
servlet.

Step 4.  Deploy to the cloud:

    $ lein gaem deploy

Don't forget to set the version number in project.clj first!

## Options

## Examples

...

### Bugs

...


## License

Copyright © 2013 Gregg Reynolds

Distributed under the Eclipse Public License, the same as Clojure.
