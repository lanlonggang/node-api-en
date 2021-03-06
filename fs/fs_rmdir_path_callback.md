<!-- YAML
added: v0.0.2
changes:
  - version: v7.6.0
    pr-url: https://github.com/nodejs/node/pull/10739
    description: The `path` parameters can be a WHATWG `URL` object using
                 `file:` protocol. Support is currently still *experimental*.
  - version: v7.0.0
    pr-url: https://github.com/nodejs/node/pull/7897
    description: The `callback` parameter is no longer optional. Not passing
                 it will emit a deprecation warning.
-->

* `path` {string|Buffer|URL}
* `callback` {Function}
  * `err` {Error}

Asynchronous rmdir(2). No arguments other than a possible exception are given
to the completion callback.

*Note*: Using `fs.rmdir()` on a file (not a directory) results in an `ENOENT`
error on Windows and an `ENOTDIR` error on POSIX.

