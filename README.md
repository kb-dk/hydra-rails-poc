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

TODO: Import project, running project, handling reloads.



Running the project from Eclipse
---
TODO:  KTC write-up.
