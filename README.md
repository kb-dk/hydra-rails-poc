This is the proof-of-concept Ruby on Rails project for Hydra.



RAILS INSTALLATION:
---

You need:

* Ruby 1.9.3 or newer.
* A working installation of SQLite3.
* Hydra-aware Fedora + Solr running in a container.


For Ubuntu 15.10, get coffee and use

    sudo apt-get install ruby ruby-dev sqlite3 libsqlite3-dev clamav libclamav-dev nodejs
    # gem update --system # is not necessary on Debian.
    sudo gem install bundler rails

The proof-of-concept project is in `project1`.  To ensure all
dependencies are met:

    cd project1
    bundle install # may ask for root password 



Running the project from the command line:
---

To run the project, be in the `project1` directory:

    bin/rails server

Restart the server after changes.  By default it listens to

    http://localhost:3000

only, so you must run your browser on the same machine.  To be visible
to others launch the Rails server with

    bin/rails server -b 0.0.0.0




Running the project from IntelliJ
---

Follow these instructions to import the project:

<https://confluence.jetbrains.com/display/RUBYDEV/Opening+Rails+projects+in+IntelliJ+IDEA>

It is important to have the Rails facet detected, and a Ruby SDK assigned.

Run -> Edit configuration.  Add a Rails type configuration for the project.

The Run and Debug buttons should now be available.  In Debug mode
the Console contains clickable stack traces.


Running the project from Eclipse
---
TODO:  KTC write-up.
