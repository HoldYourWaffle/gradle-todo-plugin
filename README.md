# gradle-todo-plugin (fixed)

A Gradle plugin for finding // TODO comments, originally by [Felix Schulze](https://github.com/x2on) and fixed by [me](https://github.com/HoldYourWaffle).

## Use in your project

This plugin is available through the [gradle plugin portal](https://plugins.gradle.org/plugin/info.zthings.gradletodo).

## Configuration

```gradle
//Default configuration
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

F-1.0: Fixed upstream issues. ([#3](https://github.com/AutoScout24/gradle-todo-plugin/issues/3) and a part of both [#1](https://github.com/AutoScout24/gradle-todo-plugin/issues/1) and [#2](https://github.com/AutoScout24/gradle-todo-plugin/issues/2))

## License

gradle-todo-plugin is available under the MIT license. See the LICENSE file for more info.
