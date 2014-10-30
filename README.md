# gradle-todo-plugin [![Build Status](https://travis-ci.org/AutoScout24/gradle-todo-plugin.png)](https://travis-ci.org/AutoScout24/gradle-todo-plugin)

A Gradle plugin for finding // TODO comments.

## Basic usage

Add to your build.gradle

```gradle
buildscript {
    repositories {
        mavenCentral()
    }
    dependencies {
        classpath 'com.autoscout24.gradle:gradle-todo-plugin:0.1.0'
    }
}

apply plugin: 'todo'
```

## Advanced usage

Add to your build.gradle

```gradle
todo {
    teamCityLog = true
    todoSuffixPattern =  '(someText|otherText)(.*)'
    failIfFound = true
}
```

* `teamCityLog`: Add features for [TeamCity](http://www.jetbrains.com/teamcity/)
* `todoSuffixPattern`: Regex suffix for TODO
* `failIfFound`: Fail build if TODO found

## Changelog

[Releases](https://github.com/AutoScout24/gradle-todo-plugin/releases)

## License

gradle-todo-plugin is available under the MIT license. See the LICENSE file for more info.
