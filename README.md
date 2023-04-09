# lein-scalac

Compile Scala source from Leiningen.

## Usage

Add `[lain-scalac "0.1.2]` for scala 2.12 to `:plugins` project.clj.
Add `[lein-scalac "0.2.13"]` for scala 2.13 to `:plugins` project.clj. (Or
`:dev-dependencies` on Leiningen versions earlier than 1.7.0)

Set `:scala-source-paths` in project.clj, usually to "src/scala", and
place your `.scala` source files in there.

Run `lein scalac` to compile them to `.class` files.

If you want `scalac` to run automatically, add `:prep-tasks ["scalac"]`
to `project.clj`

For Leiningen 1.x support, need to add `leiningen.hooks.scalac` to
`:hooks` in project.clj.

If you need runtime features of Scala you'll have to declare a
dependency on `scala-library` like so:

`:dependencies [org.scala-lang/scala-library "2.12.17"]`

`:dependencies [org.scala-lang/scala-library "2.13.10"]`

## License

Copyright © 2012 Phil Hagelberg and Scott Clasen

Copyright © 2023 Alex Menshov

Distributed under the Eclipse Public License, the same as Clojure.
