# gradle-todo-plugin [![Build Status](https://travis-ci.org/AutoScout24/gradle-todo-plugin.png)](https://travis-ci.org/AutoScout24/gradle-todo-plugin) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.autoscout24.gradle/gradle-todo-plugin/badge.svg)](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.autoscout24.gradle%22%20AND%20a%3A%22gradle-todo-plugin%22) [![License MIT](http://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/AutoScout24/gradle-todo-plugin/blob/master/LICENSE)

A Gradle plugin for finding // TODO comments.

## Basic usage

Add to your build.gradle

```gradle
buildscript {
    repositories {
        mavenCentral()
    }
    dependencies {
        classpath 'com.autoscout24.gradle:gradle-todo-plugin:1.0'
    }
}

apply plugin: 'com.autoscout24.gradle.todo'
```

## Advanced usage

Add to your build.gradle

```gradle
todo {
    teamCityLog = true
    todoPattern = "//[\t\s]*TODO(.*)"
    todoSuffixPattern =  '(someText|otherText)(.*)'
    failIfFound = true
    sourceFolder = "your source folder"
    fileExtensions = ["java", "groovy"]
}
```

* `teamCityLog`: Add features for [TeamCity](http://www.jetbrains.com/teamcity/)
* `todoPattern`: Regex for TODO
* `todoSuffixPattern`: Regex suffix for TODO
* `failIfFound`: Fail build if TODO found
* `sourceFolder`: Folder name for your sources
* `fileExtensions`: List of file extension for searching for TODOs

## Changelog

[Releases](https://github.com/AutoScout24/gradle-todo-plugin/releases)

## License

gradle-todo-plugin is available under the MIT license. See the LICENSE file for more info.
