This is the proof-of-concept Ruby on Rails project for Hydra.



RAILS INSTALLATION:
---

You need:

* Ruby 1.9.3 or newer.
* A working installation of SQLite3.
* Hydra-aware Fedora + Solr running in a container.
* Redis server running on localhost port 6379 (standard port)


For Ubuntu 15.10, get coffee and use

    sudo apt-get install ruby ruby-dev sqlite3 libsqlite3-dev clamav libclamav-dev nodejs
    # gem update --system # is not necessary on Debian.
    sudo gem install bundler rails

The proof-of-concept project is in `project1`.  To ensure all
dependencies are met:

    cd project1
    bundle install # may ask for root password 

    rails generate curation_concerns:install
    rake db:migrate

Now the projects have the needed default configs, some of which needs moification to be able to talk to the Fedora and Solr backends.
The configurations files which need editing is:
    config/fedora.yml
    config/solr.yml
    config/blacklight.yml

If you're using the internal 'SB' fedora + solr package update as follows
For fedora.yml update the 'development' section as follows:
    Set 'password' to: fedoraAdminPass
    Set 'url' to: http://localhost:8080/fcrepo/rest

For solr.yml update the 'development' section as follows:
    Set 'url' to: http://localhost:8080/solr/#/production

For blacklight.yml update the 'development' section as follows:
    Set 'url' to: http://localhost:8080/solr/#/production

Now a new type of objects should be created (otherwise searching will fail, as there's no object types).
Creating a new type 'avis' run the following (the fedora and solr instances needs to be running):
    rails generate curation_concerns:work avis

Now the you should be ready to start the application, see below.

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
