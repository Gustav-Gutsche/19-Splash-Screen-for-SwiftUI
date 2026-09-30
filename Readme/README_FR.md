# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### Un nouvel écran de démarrage pour SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Version
**27.0.3 (Version Stable)** <br>
*Optimisé pour une interaction haute performance sans saccades.*

- **Carrousel Infini Fluide :** Nouvelle logique d'index virtuel pour éviter les "cartes volantes" et assurer une rotation infinie fluide.
- **Performance Optimisée :** Rendu accéléré par Metal (`drawingGroup`) et mises à jour efficaces par frame via `RunLoop`.
- **Défilement à Inertie :** Gestes interactifs basés sur la vitesse, ultra-fluides avec une sensation de décélération native.
- **Support AsyncImage :** Gestion des URL pré-validée pour un chargement d'images distantes sans latence.
- **Deux Modes d'Affichage :** Choisissez entre les mises en page dynamiques `.carousel` et élégantes `.static`.
- **Effets de Texte Avancés :** Rendu de texte et transitions magnifiques utilisant les fonctionnalités de SwiftUI 6.0.

## Environnement / Testé sur
- 📲 iOS 17.0+ requis / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Comment utiliser
Ajoutez le paquet à votre projet : ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Mode Carrousel (Défaut)
L'expérience interactive classique avec des images rotatives.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // URLs distantes supportées !
    ],
    title: "Bienvenue sur",
    product: "Apple TV",
    caption: "Parcourez tous les films, séries TV et plus encore.",
    cta: "Regarder Maintenant"
) {
    print("Bouton d'action cliqué")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Mode Statique (NOUVEAU)
Une mise en page épurée et défilable, parfaite pour les présentations de produits.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Studio Créateur",
    product: "3 mois de Studio Créateur gratuits.",
    caption: "Donnez vie à votre vision avec des apps puissantes.",
    features: [
        SplashFeature(title: "Fonctionnalité 1", icon: "video"),
        SplashFeature(title: "Fonctionnalité 2", icon: "waveform")
    ],
    footer: "Des conditions s'appliquent.",
    cta: "Accepter l'offre",
    secondaryCta: "Voir tous les forfaits",
    secondaryAction: {
        print("Action secondaire cliquée")
    }
) {
    print("Action principale cliquée")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Problèmes Connus
- Ce fork prend en charge iOS 17 et macOS 14. TextRenderer est utilisé à partir d’iOS 18 / macOS 15 ; les systèmes plus anciens utilisent une transition avec fondu et décalage.
- Redimensionnement : Le mode carrousel est optimisé pour Pro/Pro Max. Le mode statique inclut une ScrollView pour gérer les appareils plus petits et les longueurs de contenu variables.

## Droits d'auteur
App Store Screenshots © 2025 Apple Inc.

## Référence
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Articles connexes sur X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Combinaisons
Utilisez [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) ensemble, 2X plus efficace !
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Licence
MIT

## Soutenu par
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
