# REFrostedViewController

iOS 7 style blurred view controller that appears on top of your view controller.

<img src="https://github.com/romaonthego/REFrostedViewController/raw/master/Screenshot.png" alt="REFrostedViewController Screenshot" width="400" height="568" />
<img src="https://github.com/romaonthego/REFrostedViewController/raw/master/Demo.gif" alt="REFrostedViewController Screenshot" width="320" height="568" />

## Requirements
* Xcode 5 or higher
* Apple LLVM compiler
* iOS 6.0 or higher
* ARC

## Demo

Build and run the `REFrostedViewControllerExample` project in Xcode to see `REFrostedViewController` in action.

## Installation

### CocoaPods

The recommended approach for installating `REFrostedViewController` is via the [CocoaPods](http://cocoapods.org/) package manager, as it provides flexible dependency management and dead simple installation.
For best results, it is recommended that you install via CocoaPods >= **0.23.0** using Git >= **1.8.0** installed via Homebrew.

Install CocoaPods if not already available:

``` bash
$ [sudo] gem install cocoapods
$ pod setup
```

Change to the directory of your Xcode project:

``` bash
$ cd /path/to/MyProject
$ touch Podfile
$ edit Podfile
```

Edit your Podfile and add REFrostedViewController:

``` bash
platform :ios, '6.0'
pod 'REFrostedViewController', '~> 1.0.1'
```

Install into your Xcode project:

``` bash
$ pod install
```

Open your project in Xcode from the .xcworkspace file (not the usual project file)

``` bash
$ open MyProject.xcworkspace
```

Please note that if your installation fails, it may be because you are installing with a version of Git lower than CocoaPods is expecting. Please ensure that you are running Git >= **1.8.0** by executing `git --version`. You can get a full picture of the installation details by executing `pod install --verbose`.

### Manual Install

All you need to do is drop `REFrostedViewController` files into your project, and add `#include "REFrostedViewController.h"` to the top of classes that will use it.

## Example Usage

``` objective-c
self.menuViewController = [[REFrostedViewController alloc] init];
[self.menuViewController presentFromViewController:self animated:YES completion:nil];
```

## Customization

You can customize the following properties of `REFrostedViewController`:

``` objective-c
@property (strong, readwrite, nonatomic) UIColor *blurTintColor;
@property (assign, readwrite, nonatomic) CGFloat blurRadius;
@property (assign, readwrite, nonatomic) CGFloat blurSaturationDeltaFactor;
@property (assign, readwrite, nonatomic) CGFloat threshold;
@property (assign, readwrite, nonatomic) NSTimeInterval animationDuration;
```

## Credits

Inspired by a [Dribbble shot](http://dribbble.com/shots/1173945-Menu-Concept-1), author [Jackie Tran](http://dribbble.com/jackietrananh).

UI Control structure and View Controller containment practices adopted from [Ryan Nystrom](https://github.com/rnystrom) and [Matthias Tretter](https://github.com/myell0w).

The blur algorithm comes from WWDC 2013's session 208, "What's New in iOS User Interface Design".

## Contact

Roman Efimov

- https://github.com/romaonthego
- https://twitter.com/romaonthego
- romefimov@gmail.com

## License

REFrostedViewController is available under the MIT license.

Copyright © 2013 Roman Efimov.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
