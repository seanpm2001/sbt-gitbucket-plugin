sbt-gitbucket-plugin [![Build Status](https://travis-ci.org/gitbucket/sbt-gitbucket-plugin.svg?branch=master)](https://travis-ci.org/gitbucket/sbt-gitbucket-plugin) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.github.gitbucket/sbt-gitbucket-plugin/badge.svg)](https://maven-badges.herokuapp.com/maven-central/io.github.gitbucket/sbt-gitbucket-plugin) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/gitbucket/gitbucket/blob/master/LICENSE)
========

This sbt plugin supports GitBucket plugin development.

Add a following line to your GitBucket plugin's `project/plugin.sbt`:

```scala
addSbtPlugin("io.github.gitbucket" % "sbt-gitbucket-plugin" % "1.4.0")
```

and define the target GitBucket version in `build.sbt`:

```scala
gitbucketVersion := "4.29.0"
```

This plugin provides following functionality in your GitBucket plugin project:

- Add GitBucket core library and Servlet API dependencies to the project as "provided" scope
- Enable [sbt-assembly](https://github.com/sbt/sbt-assembly) plugin to package your GitBucket plugin
- Enable [sbt-twirl](https://github.com/playframework/twirl) plugin to compile twirl templates
- Enable `sbt install` task to build and install the GitBucket plugin to the local GitBucket instance

### TODO

- Generate a plugin manifest file for network installation
