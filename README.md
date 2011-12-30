# Javascript Test environment #

## Preconfiguration ##

    mkdir myproject
    git clone git://github.com/roothybrid7/jasmine-ci-sandbox.git
    cd jasmine-ci-sandbox
    git checkout-index -a -f --prefix=../myproject/

## Project structure ##

    .
    ├── Gemfile
    ├── Rakefile
    ├── public
    │   ├── index.html
    │   ├── javascripts
    │   │   └── app.js
    │   │   ├── jquery-1.7.1.js
    │   │   └── knockout-2.0.0.js
    │   └── stylesheets
    └── spec
        └── javascripts
            ├── fixtures
            ├── helpers
            │   ├── jasmine-jquery-1.2.0.js
            │   └── sinon-1.2.0.js
            ├── jasmine-sinon.js
            └── support
                ├── jasmine.yml
                ├── jasmine_config.rb
                └── jasmine_runner.rb

+ Gemfile: rubygems installed by bundler for jasmine execution environment.
+ Rakefile: jasmine execute tasks.
+ public: Application Documentroot.
+ spec: Application specs.
+ public/javascripts: Application javascript directory.
+ spec/javascripts: javascript spec file directory.
+ spec/javascripts/fixtures: HTML fixture for javascript specs.
+ spec/javascripts/helpers: testing library and spec helper scripts directory.
+ spec/javascripts/support: jasmine configuration files.


## Configuration ##

*Required: bundler*

    gem install bundler
    cd myproject
    bundle install --path vendor/bundle
    bundle exec rake -T
    >>rake jasmine     # Run specs via server
    >>rake jasmine:ci  # Run continuous integration tests

