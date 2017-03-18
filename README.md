# chrome-import-async-bug

The second component importing a common component will fail if it's currently being imported async and the second component not importing it async.

Tested with Polymer 1.8.1 and Chrome 58.

Example pages provided here for demonstrating the bug.

1. Install polymer with `bower install`.
2. Open example-index.html in Chrome (Blink) browser.
3. The h1 from x-header does not display. It should.


* x-header sync and x-main sync works as expected
* x-header sync and x-main async works as expected
* x-header async and x-main async works as expected
* x-header async and x-main sync do not work in chrome
