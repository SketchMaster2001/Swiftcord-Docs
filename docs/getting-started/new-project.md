# Creating a new Swiftcord bot

This guide will take you through the steps for creation a Discord Bot with Swiftcord. 

If you have not yet installed Swift, then be sure to do so first. More information on installing Swift can be found here on [Swift.org](https://www.swift.org/getting-started/#installing-swift).

## New Project

To start off, create a folder in which you'd like the bot to reside in:

```sh
mkdir SwiftcordBot
cd SwiftcordBot
```

This creates a folder named `SwiftcordBot` and moves you to it. Once you are in this folder, you can initialize a new Swift project by using:

```sh
swift package init --type executable
```

By default, this command will create a Swift executable project which will include a `Package.swift` file. Open this in your favourite text editor and add Swiftcord as a dependency.

Take a look at this example `Package.swift`.
```swift
// swift-tools-version: 5.3
import PackageDescription

let package = Package(
    name: "yourswiftexecutablehere",
    dependencies: [
        .package(url: "https://github.com/SketchMaster2001/Swiftcord", .branch("master"))
    ],
    targets: [
      .target(
        name: "yourswiftexecutablehere",
        dependencies: ["Swiftcord"]
      )
    ]
)
```
!!! note
    After the package url, the branch master is listed which means you will always have the latest changes applied. To set Swiftcord to a specific version, replace `.branch("master")` to `from: "0.9.3"`. Check the releases on the [Swiftcord Github](https://github.com/SketchMaster2001/Swiftcord) for the specific release numbers.



