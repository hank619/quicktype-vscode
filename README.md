## Notice
This project is forked from [quicktype-vscode-refresh](https://github.com/doggy8088/quicktype-vscode-refresh) and add support to latest quicktype api, the main function is that you can use camelized key for Typescript, please have a try by toggle on the `camelizedKeyForTypescript` switch in configuration.

## FAQ

Q: There is already a [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype) extension. Why do you publish a **Refresh** version of the same extension?

A: This extension is originally from [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype) extension. It because the original extension is not updating since **9/20/2018, 11:48:28 PM**. Many of the already fixed bugs/issues are not released. That's why I published this extension with **latest** version from the [quicktype/quicktype-vscode](https://github.com/quicktype/quicktype-vscode) repo.

## Introduction

**Supports** `TypeScript`, `Python`, `Go`, `Ruby`, `C#`, `Java`, `Swift`, `Rust`, `Kotlin`, `C++`, `Flow`, `Objective-C`, `JavaScript`, `Elm`, and `JSON Schema`.

-   Interactively generate types and (de-)serialization code from JSON, JSON Schema, and TypeScript
-   Paste JSON/JSON Schema/TypeScript as code

![](https://raw.githubusercontent.com/quicktype/quicktype-vscode/master/media/demo-interactive.gif)

`quicktype` infers types from sample JSON data, then outputs strongly typed models and serializers for working with that data in your desired programming language. For more explanation, read [A first look at quicktype](http://blog.quicktype.io/first-look/).

In any JSON file, use the command "Open quicktype for JSON" to summon quicktype, which will generate types from the JSON. Invoke "Change quicktype's target language" to pick a different language. There are similar "Open quicktype" commands for JSON Schema and TypeScript.

Another way to use quicktype is to copy JSON into the clipboard and invoke "Paste JSON as code/types":

![](https://raw.githubusercontent.com/quicktype/quicktype-vscode/master/media/demo.gif)

For a more powerful experience, including custom options and the ability to generate code from multiple JSON samples, try [quicktype.io](https://app.quicktype.io).

## Installing

This extension is available for free in the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=matrixyf.quicktype-new)

## Customization
- `quicktype.camelizedKeyForTypescript`: Whether set the key as camelized key for Typescript

- `quicktype.justTypes`: Generate only types, or also produce (de)serialization code when using "Open quicktype". When using "Paste", you can pick between the commands for "types" and "code", without having to set this option.

- `quicktype.inferMaps`, `quicktype.inferEnums`, `quicktype.inferDateTimes`, `quicktype.inferUuids`, `quicktype.inferBoolStrings`, `quicktype.inferIntegerStrings`: Tell quicktype whether it should try to infer those types from the input JSON. This is not a precise science, so sometimes the guess will be wrong, which is why you can turn them off through these options. Also, quicktype doesn't support dates, UUIDs and stringified integers/booleans in all target languages yes.

- `quicktype.pickCsharpTargetLanguage`: In the .NET world, there are two popular JSON serialization/de-serialization packages. The previous version of QuickType only support for [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json) (a.k.a. Json.NET). This verion of `Paste JSON as Code (Refresh)` add support for [System.Text.Json](https://www.nuget.org/packages/System.Text.Json) package and support `DateOnly` and `TimeOnly` type that been added from .NET 6.

## Contribute!

If you find a bug, please [report it on GitHub](hhttps://github.com/hank619/quicktype-vscode).
