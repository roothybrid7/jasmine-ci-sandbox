# Javascript Test environment #

Javascript Test environment skeleton.

## Copy to project ##

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
            ├── appSpec.js
            ├── fixtures
            ├── helpers
            │   ├── jasmine-jquery-1.2.0.js
            │   └── jasmine-sinon.js
            │   └── sinon-1.2.0.js
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

## Reference ##

+ Jasmine: BDD for your JavaScript:  [http://pivotal.github.com/jasmine/](http://pivotal.github.com/jasmine/)
+ velesin/jasmine-jquery - GitHub: [https://github.com/velesin/jasmine-jquery](https://github.com/velesin/jasmine-jquery}
+ #261 Testing JavaScript with Jasmine - RailsCasts: [http://railscasts.com/episodes/261-testing-javascript-with-jasmine?language=ja&view=asciicast](http://railscasts.com/episodes/261-testing-javascript-with-jasmine?language=ja&view=asciicast)
+ Sinon.JS - Versatile standalone test spies, stubs and mocks for JavaScript: [http://sinonjs.org/](http://sinonjs.org/)
+ Sinon.JS - Simplifying JavaScript testing: [http://cjohansen.no/talks/2011/xp-meetup/#1](http://cjohansen.no/talks/2011/xp-meetup/#1)
+ froots/jasmine-sinon - GitHub: [https://github.com/froots/jasmine-sinon](https://github.com/froots/jasmine-sinon)
+ Jasmine - Sinon - BrazilJS: [http://www.slideshare.net/sergiorjunior/jasmine-sinon-brasiljs](http://www.slideshare.net/sergiorjunior/jasmine-sinon-brasiljs)
