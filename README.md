# Why the need of this fork?

At baraka we don't use Cocoapods as dependency management, instead of we use SPM (Swift Package Manager). Because original repository don't support SPM, we added the support.

# Fork changes

This fork contains changes regarding adding support to newer version of Singular and SPM.

Code changes:
- Added a new `Package.swift` file to define the Swift package configuration, including dependencies on `Segment` and `Singular` libraries.
- Removed the `Info.plist` file from the `Segment-Singular-iOS` directory.
- Removed the `Segment_Singular_iOS.h` header file.
- Removed the `Segment-Singular.podspec` file, which previously defined the CocoaPods specification for the package.
- Updated `SingularIntegation.h` to include conditional imports for `SEGIntegration.h` from different possible paths.
- Updated `SingularIntegation.m` to include conditional imports for `SEGAnalyticsConfiguration.h` and `SEGAnalytics.h` from different possible paths.
- Updated `SingularIntegrationFactory.h` to include conditional imports for `SEGIntegrationFactory.h` from different possible paths.

# Usage
1. Add SPM dependency: https://github.com/barakatech/baraka-segment-singular-ios
2. Import by `import SingularSegment` on integration files

## For more infos please refer to source [documentation](https://segment.com/docs/connections/destinations/catalog/singular/)
