# SplashScreenKit
### Ein neuer Splash-Screen für SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Version
**2.2.3 (Stabile Version)** <br>
*Optimiert für Hochleistungs-Interaktion ohne Ruckeln.*

- **Nahtloses unendliches Karussell:** Neue virtuelle Index-Logik verhindert „fliegende Karten“ und sorgt für eine reibungslose unendliche Rotation.
- **Leistungsoptimiert:** Metal-beschleunigtes Rendering (`drawingGroup`) und effiziente Updates pro Frame via `RunLoop`.
- **Momentum-Scrolling:** Butterweiche, geschwindigkeitsbasierte interaktive Gesten mit nativem Verzögerungsgefühl.
- **AsyncImage-Unterstützung:** Vorvalidierte URL-Handhabung für verzögerungsfreies Laden von Remote-Bildern.
- **Zwei Anzeigemodi:** Wählen Sie zwischen dynamischen `.carousel`- und eleganten `.static`-Layouts.
- **Erweiterte Texteffekte:** Wunderschönes Text-Rendering und Übergänge mit SwiftUI 6.0 Funktionen.

## Umgebung / Getestet auf
- 📲 iOS 17.0+ / macOS 14.0+ erforderlich
- Swift 6.0
- Xcode 16.0+

## Verwendung
Fügen Sie das Paket zu Ihrem Projekt hinzu: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Karussell-Modus (Standard)
Das klassische interaktive Erlebnis mit rotierenden Bildern.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Remote-URLs werden unterstützt!
    ],
    title: "Willkommen bei",
    product: "Apple TV",
    caption: "Durchsuchen Sie alle Filme, TV-Sendungen und mehr.",
    cta: "Jetzt ansehen"
) {
    print("Aktions-Button getippt")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Statischer Modus (NEU)
Ein klares, scrollbares Layout, perfekt für Produktpräsentationen.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Creator Studio",
    product: "3 Monate Creator Studio kostenlos.",
    caption: "Erwecken Sie Ihre Vision mit leistungsstarken Apps zum Leben.",
    features: [
        SplashFeature(title: "Feature 1", icon: "video"),
        SplashFeature(title: "Feature 2", icon: "waveform")
    ],
    footer: "Es gelten die allgemeinen Geschäftsbedingungen.",
    cta: "Angebot annehmen",
    secondaryCta: "Alle Abos anzeigen",
    secondaryAction: {
        print("Sekundäraktion getippt")
    }
) {
    print("Primäraktion getippt")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Bekannte Probleme
- Ab iOS 18 nutzt der Karusselltext SwiftUI `TextRenderer` für die Animation einzelner Zeichen. Unter iOS 17 bleiben Layout und Inhalt erhalten; der Text erscheint mit einer kombinierten Einblend- und Verschiebungsanimation.
- Größenänderung: Der Karussell-Modus ist für Pro/Pro Max optimiert. Der statische Modus enthält eine ScrollView, um kleinere Geräte und unterschiedliche Inhaltslängen zu unterstützen.

## Urheberrecht
App Store Screenshots © 2025 Apple Inc.

## Referenz
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Verwandte Beiträge auf X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Kombinationen
Verwenden Sie [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) zusammen, 2X effektiver!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Lizenz
MIT

## Unterstützt von
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
