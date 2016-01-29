Mirrors [SWFSemanticVersion](https://github.com/samuelwford/SWFSemanticVersion) using [Rome](https://github.com/neonichu/Rome) to create a Carthage-compatible Xcode project.

### To install:

- Add `github "n8chur/SWFSemanticVersion"` to your `Cartfile`.

### To update to a new version:

- Update the gems and pods:
```
$ bundle update
$ bundle exec pod update
```
- Remove the current shared scheme
```
$ rm -rf Pods/Pods.xcodeproj/xcshareddata
```
- Share the scheme that builds `SWFSemanticVersion.framework` in `Pods.xcodeproj`
- Archive the framework using Carthage:
```
$ carthage build --no-skip-current
$ carthage archive SWFSemanticVersion
```
- Create a new tag that matches the SWFSemanticVersion version in `Podfile.lock`
- Create a GitHub release for the tag and upload `SWFSemanticVersion.framework.zip` as an attachment
