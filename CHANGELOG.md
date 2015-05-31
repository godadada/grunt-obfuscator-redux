
1.0.3 / 2015-05-31
==================

 * Added ability to remove 'use strict' from obfuscated code when the `strings` option is set to `true`. This is required as currently, octal representations (which is what `obfuscator` converts all simple strings to when this option is set) are not allowed in strict mode.
 * Added pretty printed log outputs to know what happened.

1.0.1 / 2015-05-30
==================

 * Forked from https://github.com/stephenmathieson/grunt-obfuscator with new package name.
 * Add support for multiple targets.
 * Clean-up code a bit.
 * Update README with more examples.

0.1.0 / 2014-02-26
==================

 * Use any backwards compatible version of obfusactor
 * Add travis
 * Initial commit

0.0.1 / 2013-12-20
==================

  * Initial release
