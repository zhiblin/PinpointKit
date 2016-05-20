**PinpointKit** is an open-source iOS library in Swift that lets your your testers and user send feedback with annotated screenshots and logs using a simple gesture.

## Features

- [x] Shake to trigger feedback collection
- [x] Automatic, opt-in system log collection
- [x] Add arrows, boxes, and text to screenshots to point out problems.
- [x] Blur our sensitive information before sending screenshots
- [x] Customize everything
	- [x] The color of the arrows, and boxes
	- [x] The text in the interfaces
	- [x] How and where your feedback is sent
- [x] Absolutely free and open source
- [x] No backend required

## Requirements

* iOS 9.0+
* Xcode 7.3+

## Installation

### CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

> CocoaPods 1.0.0+ is required to build PinpointKit.

To integrate PinpointKit into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '9.0'
use_frameworks!

pod 'PinpointKit', '~> 1.0'
```

Then, run the following command:

```bash
$ pod install
```

### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that builds your dependencies and provides you with binary frameworks.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate PinpointKit into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "Lickability/PinpointKit" ~> 1.0
```

- Run `carthage update` to build the framework.
- Next, select your application project in the Project Navigator (blue project icon) to navigate to the target configuration window and select the application target under the "Targets" heading in the sidebar.
- In the tab bar at the top of that window, open the "General" panel.
- Drag the built `PinpointKit.framework` from the Carthage build folder into the "Embedded Binaries" section.

### Manually

If you prefer not to use either of the aforementioned dependency managers, you can integrate PinpointKit into your project manually.

#### Embedded Framework

- Open up Terminal, `cd` into your top-level project directory, and run the following command if your project is not initialized as a git repository:

```bash
$ git init
```

- Add PinpointKit as a git [submodule](http://git-scm.com/docs/git-submodule) by running the following command:

```bash
$ git submodule add https://github.com/Lickability/PinpointKit.git
```

- Open the new `PinpointKit/PinpointKit` folder, and drag the `PinpointKit.xcodeproj` into the Project Navigator of your application's Xcode project.

    > It should appear nested underneath your application's blue project icon. Whether it is above or below all the other Xcode groups does not matter.

- Select the `PinpointKit.xcodeproj` in the Project Navigator and verify the deployment target matches that of your application target.
- Next, select your application project in the Project Navigator (blue project icon) to navigate to the target configuration window and select the application target under the "Targets" heading in the sidebar.
- In the tab bar at the top of that window, open the "General" panel.
- Click on the `+` button under the "Embedded Binaries" section.    
- You will see two different `PinpointKit.xcodeproj` folders each with two different versions of the `PinpointKit.framework` nested inside a Products folder.
- Select the top `PinpointKit.framework` for iOS.

- And that's it!

> The `PinpointKit.framework` is automatically added as a target dependency, linked framework and embedded framework in a copy files build phase which is all you need to build on the simulator and a device.



## Usage


Once PinpointKit is installed, it’s simple to use
