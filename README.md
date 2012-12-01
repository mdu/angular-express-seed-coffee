# Angular Express Seed

This is an Angular Express Seed project which is written in CoffeeScript and adapted from Brian Ford's awesome seed project (<https://github.com/btford/angular-express-seed>).

This project contains seed tests (Unit Test & E2E Test) for AngularJS and some modifications in the app config file (app.coffee) to run E2E tests on browser.

The Angular coffeescript files are stored under assets/js which is then managed by assets-connect middle-ware.

While writing Angular unit tests, please be noticed that the module function should return nothing (put return in that function to prevent coffeescript auto return the last line).

For Javascript version of this project, please visit <https://github.com/thanh-nguyen/angular-express-seed>

## Intro

Start an awesome app with AngularJS on the front, Express + Node on the back. This project is an
application skeleton for a typical [AngularJS](http://angularjs.org/) web app for those who want
to use Node to serve their app.

The seed contains angular libraries, test libraries and a bunch of scripts all preconfigured for
instant web development gratification. Just clone the repo (or download the zip/tarball) and
you're ready to develop your application.

The seed app shows how to wire together Angular client-side components with Express on the server.
It also illustrates writing angular partial views with the Jade templating library.

*Note: Although Jade supports interpolation, you should be doing that mostly on the client. Mixing
server and browser templating will convolute your app. Instead, use Jade as a syntactic sugar for
HTML, and let AngularJS take care of interpolation on the browser side.*

## How to use angular-express-seed

Clone the repository and start hacking!

### Running the app

Runs like a typical express app:

    node app.coffee
    OR
    nodemon app.coffee    // for auto reload server on code changes (npm install -g nodemon)

### Running tests

**Testacular is required to run angular tests (npm install -g testacular)**

For AgnularJS Unit Tests:

    scripts/test.sh

For AngularJS E2E Tests:

    scripts/e2e-test.sh

    #### Note
    Because writing in coffeescript, this project does not support running Angular e2e tests by "open localhost:3000/test/e2e/runner.html"

### Receiving updates from upstream

Just fetch the changes and merge them into your project with git.

## Directory Layout

    app.coffee                  --> app config
    assets/                     --> stylus stylesheets and js configured by assets-connect
      css/
        app.styl                --> main css file
        bootstrap.min.css       --> twitter bootstrap css
      js/
        app.coffee              --> declare top-level app module
        controllers.coffee      --> application controllers
        directives.coffee       --> custom angular directives
        filters.coffee          --> custom angular filters
        services.coffee         --> custom angular services
        lib/                    --> angular and 3rd party JavaScript libraries
          angular/
            angular.js          --> the latest angular js
            angular.min.js      --> the latest minified angular js
            angular-*.js        --> angular add-on modules
            version.txt         --> version number
    config/
      testacular-e2e.conf.js    --> testacular config file for angular e2e tests
      testacular.conf.js        --> testacular config file for angular unit tests
    logs                        --> any log files should be stored here
    package.json                --> app dependencies for npm
    public/                     --> all of the files to be used in on the client side
      css/                      --> css files
      js/                       --> javascript files
    routes/
      api.coffee                --> route for serving JSON
      home.coffee               --> route for serving HTML pages and partials
    scripts/
      e2e-test.bat              --> angular e2e test runner for windows
      e2e-test.sh               --> angular e2e test runner for unix
      test.bat                  --> angular unit test runner for windows
      test.sh                   --> angular unit test runner for unix
      watchr.rb                 --> watcher for auto re-running angular tests
    test/
      e2e/
        scenarios.coffee        --> angular e2e tests
      lib/
        angular/                --> angular library for testing
      unit/
        controllersSpec.coffee  --> angular controllers' tests
        directivesSpec.coffee   --> angular directives' tests
        filtersSpec.coffee      --> angular filters' tests
        servicesSpec.coffee     --> angular services' tests
    views/
      index.jade                --> main page for app
      layout.jade               --> doctype, title, head boilerplate
      angular/                  --> angular view partials (partial jade templates)
        sample/
          partial1.jade
          partial2.jade

## Contact

For more information on AngularJS please check out <http://angularjs.org/>.

For more on Express and Jade, <http://expressjs.com/> and <http://jade-lang.com/> are
your friends.

Any feedback is more than welcome!!!