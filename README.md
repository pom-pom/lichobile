[lichess.org/mobile](http://lichess.org/mobile)
--------------------

[![Build Status](https://travis-ci.org/veloce/lichobile.svg?branch=master)](https://travis-ci.org/veloce/lichobile)

![lichess mobile screenshots](portfolio.png)

Lichess mobile is the lichess.org official application. It is written
in [TypeScript](http://www.typescriptlang.org/), with a bit of Kotlin and Swift.
It is a web application that access native SDK thanks to [Ionic capacitor](https://capacitor.ionicframework.com/).
The rendering library is [mithril.js](http://mithril.js.org/).
It talks to a native [Stockfish](https://stockfishchess.org/) engine, [supporting multiple variants](https://github.com/ddugovic/Stockfish), through a
[cordova plugin](https://github.com/veloce/cordova-plugin-stockfish).
Multi-variant chess library is brought by [a JavaScript version of scalachess](https://github.com/veloce/scalachessjs).

## Required dependencies

* [node](http://nodejs.org) latest LTS version
* [ionic capacitor dependencies](https://capacitor.ionicframework.com/docs/getting-started/dependencies)

**Android:**

* in addition to capacitor dependencies, [android ndk](http://developer.android.com/tools/sdk/ndk/index.html) for stockfish compilation (to install with Android Studio).

## Initialize build

Make sure you installed all deps:

    $ npm install

Capacitor needs the web app before update, so build it:

    $ npm run build

Update capacitor:

    $ npx cap update

## Run in a browser

You need to start a web server at `http://localhost:8080`. For instance:

    $ npm install -g http-server
    $ http-server .

Once the server is running, browse to `http://localhost:8080/www

Be sure to [Toggle Device Mode](https://developers.google.com/web/tools/chrome-devtools/device-mode/) in your browser, or else you won't be able to click on anything.

## Run in a device/emulator

The easiest way to do it is to open the native IDE. Capacitor has a command
for that:

    $ npx cap open

## Advanced setup

See the [wiki](https://github.com/veloce/lichobile/wiki/Setting-a-lichess-dev-server-for-the-app).
