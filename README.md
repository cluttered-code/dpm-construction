# DPM Construction

[![Stories in Backlog](https://badge.waffle.io/cluttered-code/dpm-construction.svg?label=backlog&title=Backlog)](http://waffle.io/cluttered-code/dpm-construction)
[![Stories in Ready](https://badge.waffle.io/cluttered-code/dpm-construction.svg?label=ready&title=Ready)](http://waffle.io/cluttered-code/dpm-construction)
[![Stories in In Progress](https://badge.waffle.io/cluttered-code/dpm-construction.svg?label=in-progress&title=In Progress)](http://waffle.io/cluttered-code/dpm-construction)

[![Sauce Build Status](https://saucelabs.com/browser-matrix/dpm-construction.svg)](https://saucelabs.com/beta/builds/02c82c99df70441381bf5549613ab6d6)

[![Travis Build Status](https://travis-ci.org/cluttered-code/dpm-construction.svg?branch=master)](https://travis-ci.org/cluttered-code/dpm-construction)

### Setup

##### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli

### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve --open


### Build

This command performs HTML, CSS, and JS minification on the application
dependencies, and generates a service-worker.js file with code to pre-cache the
dependencies based on the entrypoint and fragments specified in `polymer.json`.
The minified files are output to the `build/unbundled` folder, and are suitable
for serving from a HTTP/2+Push compatible server.

In addition the command also creates a fallback `build/bundled` folder,
generated using fragment bundling, suitable for serving from non
H2/push-compatible servers or to clients that do not support H2/Push.

    polymer build

### Preview the build

This command serves the minified version of the app at `http://localhost:8080`
in an unbundled state, as it would be served by a push-compatible server:

    polymer serve build/unbundled

This command serves the minified version of the app at `http://localhost:8080`
generated using fragment bundling:

    polymer serve build/bundled

### Run tests

This command will run
[Web Component Tester](https://github.com/Polymer/web-component-tester) against the
browsers currently installed on your machine.

    polymer test
