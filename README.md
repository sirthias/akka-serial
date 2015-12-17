# flow
Serial communication library for Scala, designed to be reactive, lightweight and easily integrable with Akka applications. See the [website](https://jodersky.github.io/flow) for a guide.

## Highlights
- Reactive: only does work when required (no constant polling of ports or blocking IO)
- Integrates seamlessly with Akka
- Portable to POSIX systems
- Watchable ports: react to connection of new devices

## Native side
Since hardware is involved in serial communication, a Scala-only solution is not possible. Nevertherless, the native code is kept simple and minimalistic with the burden of dealing with threads left to Scala. The code aims to be POSIX compliant and therefore easily portable.

## Directory Structure
```
flow/
├── flow-main             Main scala source files.
├── flow-native           C sources used to implement serial communication.
├── flow-samples          Runnable example projects.
├── project               SBT configuration.
└── site                  Website sources, including documentation.
```

## Build
Detailed documentation on building flow is available on the website.

Since flow integrates into the Akka-IO framework, a good resource on its general design is the framework's [documentation](http://doc.akka.io/docs/akka/2.4.1/scala/io.html).

This project is also an experiment on working with JNI and automating build infrastructure.

## Copying
flow is released under the terms of the 3-clause BSD license. See LICENSE for details.
