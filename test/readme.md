Included in this directory
--------------------------

- ol.html - the web page used to run the test suite.

- spec - includes the OpenLayers test/spec files.

- jasmine-1.2.0 - includes the Jasmine Testing Framework.
  https://github.com/pivotal/jasmine

- jasmine-extensions.js - includes OpenLayers-specific extensions to Jasmine.

- phantom-jasmine - a PhantomJS script and a console reporter to for headless
  testing. Comes from https://github.com/jcarver989/phantom-jasmine.

Run the test suite with PhantomJS
---------------------------------

With PhantomJS installed, and assuming phantomjs is in the PATH:

    $ phantomjs phantom-jasmine/run_jasmine_test.coffee ol.html

(Works with PhantomJS 1.6.1, untested with other versions.)

This command can also be run by doing `make test` at the root of ol3.

Tip for TDD'ers: to make PhantomJS run the test suite continuously each time
a spec file is changed you can use nosier (http://pypi.python.org/pypi/nosier)
and do `nosier -p test -p src "make test"`.
