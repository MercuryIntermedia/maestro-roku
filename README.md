<p align="center">
  <img src="docs/maestroLogo.png" alt="Maestro for roku" />
</p>
<h3 align="center">
A development platform for building roku channels in brighterscript.
</h3>


[![Build Status](https://travis-ci.org/georgejecook/maestro-roku.svg?branch=master)](https://travis-ci.org/georgejecook/maestro-roku)
[![GitHub](https://img.shields.io/github/release/georgejecook/maestro-roku.svg?style=flat-square)](https://github.com/georgejecook/maestro-roku/releases)

# maestro for roku

## Sample app

 - `git clone git@github.com:georgejecook/maestro-roku.git`
 - `cd maestro-roku/samples`
 - `npm install`
 - `npm run ropm`
 - `code .`
 - update `.env` file with your roku ip and password
 - launch the app

## Why maestro?

### Maestro Makes roku development easier, especially for experienced software engineers from other platforms:

Roku develpoment can be challenging, and is steepd in nuance that makes it really hard for a developer with less than 6 months to be productive. Usually by that time, they've made an unmitigated mess of everything and are stuck with diminishing velocity and a cpl years worth of misery before a sudden roku change renders their architecture void, and they are forced to start again.

I believe that experienced developers from android, ios, c#, web, node, etc, should be able to be productive on a roku app in no more than a week, just as they would on any other platform. So I wrote maestro to make that possible.

Maestro is built to:

 - Raise velocity
 - Increase productivity
 - Reduce learning
 - Simply cross-skilling
 - Make roku development more fun
 - Produce roku apps that can be maintained by non roku developer
 - Produce roku apps that can be unit tested easily
 - Write code that can be tested and breakpoint debugged, outside of SG views (which are slow as hell, and prone to crashing when breakpoint debugging)

### How does maestro do this?

Maestro provides the following:

 - Familiar view lifecycles (`onShow`, `onHide`, `onFirstShow`, `onGainedFocus`, etc)
 - Simple key handlings (`onKeyPressXXX`, long key presses, key press locking)
 - Focus management that works, without guessing/debugging
 - Familiar aggregate views (`TabController`, `NavController`, `DynamicView`)
 - Pluggable and extensible view transitions
 - Improved task observers (use function pointers, not strings, get values unpacked automatically)
 - Base classes for all common activites (`BaseView`, `BaseScreen`, `NodeClass`, etc)
 - Wrapped utility methods on base class methods, for easy stubbing and mocking
 - IOC mechanism (`mioc.getInstance("foo")`, `mioc.setInstance("foo", bar)`, `@inject("foo")` annotationso for class fields)
 - MVVM base classes with xml binding support (`<Button text='{{title}}' selected='{(onSelect())}' />`)
 - Code generation for Node classes, and Tasks, making writing unit testable controls and tasks, easier than ever
 - Animation library (`myFade a = mv.animations.FadeTo(m.button, 1, 0.5)`, `myFade.onFraction( 0.5, function(f)...`, etc)
 - Wrappers for all main roku components to make them easy to style and use in mvvm via a `style` property
 - `StyleManager`, and `FontManager`, for caching style and fonts
 - Node level `Map`, and `Set` implementations, and `collections` library
 - SDP adhering OOAD, class based brighterscript code, throughout

Maestro is easy to use:

 - Delivered as ropm module for easy installation
 - Has sample app, which is ready to roll for production ready roku apps

Maestro is aligned with community best practices and tools

 - Uses ropm
 - Written in [brighterscript](https://github.com/rokucommunity/brighterscript)
 - Uses brighterscript plugins for compile time and IDE diagnostics
 - No need for complex build scripts or bespoke build processes (like bash/gulp etc); maestro apps can run simply by executing `bsc`  (brighterscript compiler)


Maestro is performant

 - Runs great on all roku devices
 - Maestro apps launch quick and are snappy

Maestro is installed on millions of devices

Been in production for > 2 years at:

  - applicaster, and their various clients
  - smithsonian
  - corco
  - other clients (names pending permission ;) )

