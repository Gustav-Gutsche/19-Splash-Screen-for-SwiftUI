# iOS 17 compatibility in this fork

Version 27.0.2 supports iOS 17.0 and macOS 14.0. The package requires a Swift 6 toolchain (Xcode 16 or newer); this compiler requirement does not raise the app's minimum operating-system version.

## Integration

Use `https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI`, with a version requirement starting at `27.0.2`. Add the `SplashScreenKit` product to the app target, keep its deployment target at iOS 17.0 or later, and `import SplashScreenKit`.

The original `1998code` URL points to a different package that requires iOS 18. Existing projects pinned to an older commit must update their requirement to consume this release.

## Behavior

- Carousel, Static and Simple Mode run on iOS 17. The rotating photos continue to animate there.
- Per-glyph `TextRenderer` transitions use iOS 18 / macOS 15 when available. Earlier systems use the same text with a fade-and-offset entrance.
- The carousel fits its existing 840-point minimum canvas to the available height. Smaller phones no longer require a scale wrapper in the consuming app.
- Transient zero-height layout passes are guarded. An empty image array no longer triggers a modulo-by-zero crash; text and the action remain available.
- Bundled images are supported by `Photo("AssetName")`. Remote URLs remain optional and retain their existing loading behavior.

## Verification on 2026-09-30

| Scope | Minimum supported | Actually tested | Evidence |
| --- | --- | --- | --- |
| iOS package and all display modes | iOS 17.0 | iOS 17.5, iPhone SE (3rd generation) Simulator | Four UI tests passed: Carousel, Static, Simple, empty Carousel; each verifies action reachability and transition to the demo's completion screen |
| Newer-system text path and modes | iOS 18.0 for the per-glyph effect | iOS 27.2, iPhone 17e Simulator | Three UI tests passed: Carousel, Static, Simple |
| Swift package / macOS compilation | macOS 14.0 | macOS 27.0.1, SwiftPM with Xcode 27.0 (27A266a) | `swift test` builds the package for its macOS 14 target; existing placeholder test passes |
| Compiler and older SDK compatibility | Swift 6 / Xcode 16 | Xcode 16.4 (16F6), Swift 6.1.2, plus Xcode 27.0 | SwiftPM cross-build for `arm64-apple-ios17.0-simulator` with the iOS 18.5 SDK, and macOS 14 build using Xcode 16.4; final iOS 17 UI suite built/run using Xcode 27.0 |

Local result bundles: `.build/iOS17-release-final.xcresult` and `.build/iOS27-release-qa.xcresult`. Simulator screenshots are retained under `.build/qa/`. These generated files are excluded from Git.

Native macOS rendering and physical iOS devices were not tested for this release. The Xcode 16.4 checks compile the library; simulator UI tests use Xcode 27.0. The default demo uses the bundled reference images already present in this repository; no Repeatly-specific photos or app logic are included.

The text attribute helper is explicitly marked iOS 18 / macOS 15, like its renderer and transition. Older SDKs therefore never require its modern protocol in the iOS 17 path. Xcode 16.4 build logs: `.build/qa/swift16.4-ios-build.log` and `.build/qa/swift16.4-macos-build.log`.
