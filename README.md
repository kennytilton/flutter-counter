# Flutter Test Drive Counter Example, in ClojureDart

One nooby's port of the [Flutter Test Drive Counter example](https://docs.flutter.dev/get-started/test-drive) to [ClojureDart](https://github.com/Tensegritics/ClojureDart), a Clojure version of Dart.

Borrowed massively from Artur Demchov's [Minataurus](https://github.com/Liverm0r/minataurus/tree/custom-widget) and the [ClojureDart Quickstart]( https://github.com/Tensegritics/ClojureDartPreview/blob/main/doc/flutter-quick-start.md).

Caveat lector: I am a nooby at both ClojureDart and Dart/Flutter, and my work has yet to be reviewed by anyone. Hint. (Reviews/corrections welcome.)

## My workflow (Mac OS X only)

In a terminal:

* clone this repo
* `cd <this repo location>`
* Start the Flutter debugger: `dart devtools`.
  * This ^^^ command does not return. After a few seconds, look for a new browser tab "DevTools for Futter". We like to tear that off and keep it handy because that will be our console.
* In a new terminal, `open -a Simulator`. An iPhone simulator should open somewhere on your Mac
* That ^^^ open command returns, so in the same terminal: `clj -M -m cljd.build flutter`
  * That ^^^ build command does _not_ return, and takes about thirty seconds before you should see "Flutter Test Drive" on the simulator.

The build command ends by displaying something like:
```
The Flutter DevTools debugger and profiler on iPhone 12 is available at: http://127.0.0.1:9101?uri=http://127.0.0.1:61927/mq2Vp_UbNtE=/
```
We will need that info to connect the Flutter DevTools browser app to our app.

* copy the displayed URL, in this case `http://127.0.0.1:9101?uri=http://127.0.0.1:61927/mq2Vp_UbNtE=/` and paste it into the Flutter Devtools input field under "Connecting to a Running App";
* click "Connect" to the right of the input field;
* the DevTools interface will change to be a Flutter Inspector.

If you look at the Flutter Inspector console you will see any print diagnostics in the latest commit.

Ping @kennytilton on #clojurians Slack for help!


