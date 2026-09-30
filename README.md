# SplashScreenKit
### A New Splash Screen for SwiftUI

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

| Region | Languages |
| :--- | :--- |
| **Global** | [English](./README.md) |
| **Asia** | [廣東話](./Readme/README_HK.md) [繁體中文](./Readme/README_TW.md) [简体中文](./Readme/README_CN.md) [日本語](./Readme/README_JP.md) [한국어](./Readme/README_KR.md) [Indo](./Readme/README_ID.md) [हिन्दी](./Readme/README_HI.md) |
| **Europe** | [Français](./Readme/README_FR.md) [Deutsch](./Readme/README_DE.md) [Español](./Readme/README_ES.md) [Русский](./Readme/README_RU.md) [Polski](./Readme/README_PL.md) [Türkçe](./Readme/README_TR.md) |
| **ME & Africa** | [العربية](./Readme/README_AR.md) [Kiswahili](./Readme/README_SW.md) |

## Version
**27.0.2 (iOS 17-compatible fork)** <br>
*All three modes support iOS 17. Includes automatic carousel sizing for smaller phones.*

- **Simple Mode:** Full-screen text-first splash screen with configurable SF Symbol logo, gradient background, footer copy, and inline privacy link.
- **Seamless Infinite Carousel:** New virtual-index logic prevents "flying cards" and ensures smooth infinite rotation.
- **Performance Optimized:** Metal-accelerated rendering (`drawingGroup`) and efficient per-frame updates via `RunLoop`.
- **Momentum Scrolling:** Butter-smooth, velocity-based interactive gestures with native deceleration feel.
- **AsyncImage Support:** Pre-validated URL handling for lag-free remote image loading.
- **Three Display Modes:** Choose between dynamic `.carousel`, elegant `.static`, and lightweight `.simple` layouts.
- **Advanced Text Effects:** Beautiful text rendering and transitions using SwiftUI 6.0 features.

## Requirements
- iOS 17.0+ or macOS 14.0+
- Swift 6.0 / Xcode 16.0+ to compile the package
- iOS 18 is **not** required by a consuming app. The per-glyph text effect uses iOS 18 / macOS 15 when available; older systems use a fade-and-offset entrance.

Minimum supported versions and tested versions are different: this release is verified with Xcode 16.4 and 27.0, iOS 17.5 / 27.2 Simulator, and macOS 14 deployment builds. See [verification](docs/IOS17-COMPATIBILITY.md).

## Install this fork

In Xcode, choose **File → Add Package Dependencies**, enter the URL below and select **Up to Next Major Version**, starting at **27.0.2**:

```text
https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI
```

For a Swift package:

```swift
.package(
    url: "https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI",
    from: "27.0.2"
)
```

Use this fork URL; the original `1998code` repository requires iOS 18. If an existing project resolves an older revision, update the package requirement and resolve dependencies again.

## How to use
Add the package to your project: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Carousel Mode (Default)
The classic interactive experience with rotating images.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Remote URLs supported!
    ],
    title: "Welcome to",
    product: "Apple TV",
    caption: "Browse all movies, TV shows, and more.",
    cta: "Watch Now"
) {
    print("Action Button Tapped")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Static Mode
A clean, scrollable layout perfect for product introductions.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Creator Studio",
    product: "3 months of Creator Studio for free.",
    caption: "Bring your vision to life with powerful apps.",
    features: [
        SplashFeature(title: "Feature 1", icon: "video"),
        SplashFeature(title: "Feature 2", icon: "waveform")
    ],
    footer: "Terms and conditions apply.",
    cta: "Accept Offer",
    secondaryCta: "See All Plans",
    secondaryAction: {
        print("Secondary action tapped")
    }
) {
    print("Primary action tapped")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

### Simple Mode (NEW)
A text-first, Apple Sports-inspired welcome screen for lightweight onboarding.
```swift
SplashScreen(
    mode: .simple,
    logoSystemName: "apple.logo",
    title: "Welcome to",
    product: "Sports",
    caption: "Get real-time scores, stats, and standings for the teams and leagues you follow.",
    footer: "Apple may use information about your subscriptions to show relevant offers. Device identifiers may be used to keep scores and other data up to date.",
    footerLink: "See how your data is managed...",
    footerLinkURL: URL(string: "https://www.apple.com/legal/privacy/data/en/apple-sports/"),
    cta: "Continue"
) {
    print("Continue tapped")
}
```

`logoSystemName` accepts any SF Symbol name and defaults to `"apple.logo"`. Simple Mode does not require images, so the `images` parameter can be omitted.

<img width="670" height="752" alt="Simple2" src="https://github.com/user-attachments/assets/b3e52e6c-8e7b-4eef-8ef6-0f6557b216ef" />

## Known Issues
- On iOS 18+, carousel text uses SwiftUI `TextRenderer` for per-glyph animation. On iOS 17, the same layout and content use a fade-and-offset text entrance.
- The carousel automatically fits its existing card layout to smaller screens. No app-specific scale wrapper is needed. Static mode scrolls its content, and Simple Mode scales from the device width.
- An empty carousel image array is supported; the title, caption and action remain usable.

## Copyright
App Store Screenshots © 2025 Apple Inc.

## Reference
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Related Posts on X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Combinations
Use [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) together, 2X effective!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## License
MIT

## Supported By
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
<br/><br/>

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/1998code/19-Splash-Screen-for-SwiftUI)
