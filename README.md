# Broccoli

[![Build Status](https://travis-ci.org/joliss/broccoli.png?branch=master)](https://travis-ci.org/joliss/broccoli)

A fast, reliable asset pipeline, supporting constant-time rebuilds. Like
Sprockets, but with more modern architecture and not tied to Rails.

For the command line interface, see [broccoli-cli](https://github.com/joliss/broccoli-cli).

For a sample app, see [joliss/ember-app-kit#broccoli](https://github.com/joliss/ember-app-kit/tree/broccoli).
Be sure to `npm link` (symlink) the current master branch of Broccoli into
your `node_modules`, as releases are infrequent and usually out-of-date.

**This is pre-alpha work-in-progress. It's not usable for building actual JavaScript applications yet.**

Windows is not yet supported.

## Design goals

* Reliable: No dodgy cache invalidation or left-over files. You should never
  have to `rm -rf tmp` or restart the server.

* Fast: Rebuilding should be O(1) and take less than 200ms.

* Universal: Not just for JavaScript, but also for CSS, HTML, images, and
  other types of assets.

* Package manager integration: It should not matter whether files come from
  your local repository or are supplied by a package manager (like bower).
