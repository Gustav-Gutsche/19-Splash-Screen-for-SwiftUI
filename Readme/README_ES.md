# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### Una nueva pantalla de inicio para SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Versión
**27.0.3 (Versión Estable)** <br>
*Optimizado para interacciones de alto rendimiento sin interrupciones.*

- **Carrusel Infinito Fluido:** Nueva lógica de índice virtual que evita "cartas voladoras" y asegura una rotación infinita suave.
- **Rendimiento Optimizado:** Renderizado acelerado por Metal (`drawingGroup`) y actualizaciones eficientes por frame a través de `RunLoop`.
- **Desplazamiento con Inercia:** Gestos interactivos basados en la velocidad, ultra fluidos con una sensación de desaceleración nativa.
- **Soporte para AsyncImage:** Gestión de URL pre-validada para una carga de imágenes remotas sin retrasos.
- **Dos Modos de Visualización:** Elija entre diseños dinámicos `.carousel` y elegantes `.static`.
- **Efectos de Texto Avanzados:** Hermoso renderizado de texto y transiciones utilizando las funciones de SwiftUI 6.0.

## Entorno / Probado en
- 📲 Requiere iOS 17.0+ / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Cómo usar
Agregue el paquete a su proyecto: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Modo Carrusel (Predeterminado)
La experiencia interactiva clásica con imágenes rotativas.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // ¡Compatible con URL remotas!
    ],
    title: "Bienvenido a",
    product: "Apple TV",
    caption: "Explore todas las películas, programas de TV y más.",
    cta: "Ver ahora"
) {
    print("Botón de acción pulsado")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Modo Estático (NUEVO)
Un diseño limpio y desplazable, perfecto para presentaciones de productos.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Estudio del Creador",
    product: "3 meses de Estudio del Creador gratis.",
    caption: "Haga realidad su visión con aplicaciones potentes.",
    features: [
        SplashFeature(title: "Característica 1", icon: "video"),
        SplashFeature(title: "Característica 2", icon: "waveform")
    ],
    footer: "Se aplican términos y condiciones.",
    cta: "Aceptar oferta",
    secondaryCta: "Ver todos los planes",
    secondaryAction: {
        print("Acción secundaria pulsada")
    }
) {
    print("Acción primaria pulsada")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Problemas conocidos
- Este fork admite iOS 17 y macOS 14. TextRenderer se usa desde iOS 18 / macOS 15; los sistemas anteriores usan una transición con desvanecimiento y desplazamiento.
- Redimensionamiento: El modo carrusel está optimizado para Pro/Pro Max. El modo estático incluye una ScrollView para manejar dispositivos más pequeños y diferentes longitudes de contenido.

## Derechos de autor
Capturas de pantalla de la App Store © 2025 Apple Inc.

## Referencia
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Publicaciones relacionadas en X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Combinaciones
¡Use [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) juntos, 2 veces más efectivo!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Licencia
MIT

## Apoyado por
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
