This is the proof-of-concept Ruby on Rails project for Hydra.



RAILS INSTALLATION:
---

You need Ruby 1.9.3 or newer.  You need a working installation of SQLite3.

FIXME:  YOU NEED A HYDRA FEDORA + SOLR RUNNING.

For Ubuntu 15.10 use

    apt-get install ruby sqlite3 libsqlite3-dev clamav libclamav-dev
    # gem update --system # is not necessary on Debian.
    gem install bundler rails


The toy project is in `project1`.   To ensure all dependencies are met:

    cd project1
    bundle install



Running the project from the command line:
---

To run the project, be in the `project1` directory:

    bin/rails server

Restart the server after changes.


Running the project from IntelliJ
---

TODO: Import project, running project, handling reloads.