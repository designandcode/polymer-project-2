# \<polymer-project-2\>

Match flags to their countries!

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create builds of your application in the `build/` directory, optimized to be served in production. You can then serve the built versions by giving `polymer serve` a folder to serve from:

```
$ polymer serve build/default
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

## App Route and Data Flow

polymer-project-2-app
 - Handles routing between two views
   - polymer-project-2-home.html (Default)
   - polymer-project-2-game.html
 - passes async data (countries.json) to views (this is non-trivial since views are rendered before async callback so need to use observable properties in the views to update them with this data)


polymer-project-2-home
 - imports one “partial” 
   - flag-rotator.html (Image Slideshow Container)
 - passes async data (countries.json) to partial (see above for how this is achieved)


polymer-project-2-game
 - imports one “partial”
   - flag-selector.html (Image Display Container)
 - passes sync data (country) to partial

## View Live App Here
https://polymer-project-2.firebaseapp.com/
