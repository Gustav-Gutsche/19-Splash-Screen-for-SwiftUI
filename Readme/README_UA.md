# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### Новий екран привітання для SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) [Українська](./README_UA.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Версія
**27.0.3 (Стабільний реліз)** <br>
*Оптимізовано для високопродуктивної взаємодії без затримок.*

- **Безшовна нескінченна карусель:** Нова логіка віртуальних індексів запобігає «літаючим карткам» та забезпечує плавне нескінченне обертання.
- **Оптимізація продуктивності:** Рендеринг з прискоренням Metal (`drawingGroup`) та ефективне оновлення кожного кадру через `RunLoop`.
- **Інерційна прокрутка:** Неймовірно плавні інтерактивні жести, засновані на швидкості, з природним відчуттям уповільнення.
- **Підтримка AsyncImage:** Попередньо перевірена обробка URL для завантаження віддалених зображень без затримок.
- **Два режими відображення:** Вибирайте між динамічною каруселлю `.carousel` та елегантним статичним макетом `.static`.
- **Розширені текстові ефекти:** Красивий рендеринг тексту та переходи з використанням можливостей SwiftUI 6.0.

## Оточення / Протестовано на
- 📲 Потрібно iOS 17.0+ / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Як використовувати
Додайте пакет до свого проекту: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Режим каруселі (за замовчуванням)
Класичний інтерактивний досвід із обертовими зображеннями.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Підтримка віддалених URL!
    ],
    title: "Ласкаво просимо до",
    product: "Apple TV",
    caption: "Переглядайте всі фільми, телешоу та багато іншого.",
    cta: "Дивитися зараз"
) {
    print("Кнопку дії натиснуто")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Статичний режим (НОВЕ)
Чистий макет з прокручуванням, що ідеально підходить для презентації продуктів.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Студія Творця",
    product: "3 місяці Студії Творця безкоштовно.",
    caption: "Втілюйте свої ідеї в життя за допомогою потужних додатків.",
    features: [
        SplashFeature(title: "Функція 1", icon: "video"),
        SplashFeature(title: "Функція 2", icon: "waveform")
    ],
    footer: "Застосовуються правила та умови.",
    cta: "Прийняти пропозицію",
    secondaryCta: "Переглянути всі тарифи",
    secondaryAction: {
        print("Вторинну дію натиснуто")
    }
) {
    print("Основну дію натиснуто")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Відомі проблеми
- Цей форк підтримує iOS 17 і macOS 14. TextRenderer використовується починаючи з iOS 18 / macOS 15; у старіших системах застосовується перехід із плавною появою та зміщенням.
- Масштабування: Режим каруселі оптимізовано для Pro/Pro Max. Статичний режим включає ScrollView для роботи на пристроях з меншим екраном та різною довжиною контенту.

## Авторські права
Скріншоти App Store © 2025 Apple Inc.

## Посилання
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Пов'язані пости в X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Комбінації
Використовуйте разом із [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit), ефективність у 2 рази вища!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Ліцензія
MIT

## Підтримка
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
