# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### Новый экран приветствия для SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Версия
**27.0.3 (Стабильный релиз)** <br>
*Оптимизировано для высокопроизводительного взаимодействия без задержек.*

- **Бесшовный бесконечный карусель:** Новая логика виртуальных индексов предотвращает «летающие карточки» и обеспечивает плавное бесконечное вращение.
- **Оптимизация производительности:** Рендеринг с ускорением Metal (`drawingGroup`) и эффективные обновления каждого кадра через `RunLoop`.
- **Инерционная прокрутка:** Невероятно плавные интерактивные жесты, основанные на скорости, с естественным ощущением замедления.
- **Поддержка AsyncImage:** Предварительно проверенная обработка URL для загрузки удаленных изображений без задержек.
- **Два режима отображения:** Выбирайте между динамической каруселью `.carousel` и элегантным статическим макетом `.static`.
- **Расширенные текстовые эффекты:** Красивый рендеринг текста и переходы с использованием возможностей SwiftUI 6.0.

## Окружение / Протестировано на
- 📲 Требуется iOS 17.0+ / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Как использовать
Добавьте пакет в свой проект: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Режим карусели (по умолчанию)
Классический интерактивный опыт с вращающимися изображениями.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Поддержка удаленных URL!
    ],
    title: "Добро пожаловать в",
    product: "Apple TV",
    caption: "Смотрите все фильмы, телепередачи и многое другое.",
    cta: "Смотреть сейчас"
) {
    print("Кнопка действия нажата")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Статический режим (НОВОЕ)
Чистый, прокручиваемый макет, идеально подходящий для презентации продуктов.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Студия Создателя",
    product: "3 месяца Студии Создателя бесплатно.",
    caption: "Воплощайте свои идеи в жизнь с помощью мощных приложений.",
    features: [
        SplashFeature(title: "Функция 1", icon: "video"),
        SplashFeature(title: "Функция 2", icon: "waveform")
    ],
    footer: "Применяются правила и условия.",
    cta: "Принять предложение",
    secondaryCta: "Посмотреть все тарифы",
    secondaryAction: {
        print("Вторичное действие нажато")
    }
) {
    print("Основное действие нажато")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Известные проблемы
- Этот форк поддерживает iOS 17 и macOS 14. TextRenderer используется начиная с iOS 18 / macOS 15; на более старых системах применяется переход с плавным появлением и смещением.
- Масштабирование: Режим карусели оптимизирован для Pro/Pro Max. Статический режим включает ScrollView для работы на устройствах с меньшим экраном и разной длиной контента.

## Авторские права
Скриншоты App Store © 2025 Apple Inc.

## Ссылки
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Связанные посты в X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Комбинации
Используйте вместе с [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit), эффективность в 2 раза выше!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Лицензия
MIT

## Поддержка
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
