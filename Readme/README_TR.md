# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### SwiftUI için Yeni Bir Karşılama Ekranı

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Versiyon
**27.0.3 (Stabil Sürüm)** <br>
*Sarsıntısız ve yüksek performanslı etkileşimler için optimize edildi.*

- **Kesintisiz Sonsuz Atlıkarınca:** Yeni sanal dizin mantığı "uçan kartları" önler ve akıcı bir sonsuz rotasyon sağlar.
- **Performans Odaklı:** Metal hızlandırmalı oluşturma (`drawingGroup`) ve `RunLoop` aracılığıyla verimli kare güncellemeleri.
- **Momentum Kaydırma:** Yerel yavaşlama hissi veren, hıza dayalı ve pürüzsüz etkileşimli jestler.
- **AsyncImage Desteği:** Lag içermeyen uzak görüntü yükleme için önceden doğrulanmış URL işleme.
- **İki Ekran Modu:** Dinamik `.carousel` ve zarif `.static` düzenleri arasında seçim yapın.
- **Gelişmiş Metin Efektleri:** SwiftUI 6.0 özelliklerini kullanarak harika metin oluşturma ve geçişler.

## Ortam / Test Edilen Platformlar
- 📲 iOS 17.0+ gereklidir / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Nasıl Kullanılır
Paketi projenize ekleyin: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Atlıkarınca Modu (Varsayılan)
Dönen görüntülerle klasik etkileşimli deneyim.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Uzak URL'ler desteklenir!
    ],
    title: "Hoş geldiniz",
    product: "Apple TV",
    caption: "Tüm filmlere, TV şovlarına ve daha fazlasına göz atın.",
    cta: "Şimdi İzle"
) {
    print("Aksiyon Butonuna Tıklandı")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Statik Mod (YENİ)
Ürün tanıtımları için mükemmel, temiz ve kaydırılabilir bir düzen.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Yaratıcı Stüdyo",
    product: "3 ay boyunca ücretsiz Yaratıcı Stüdyo.",
    caption: "Güçlü uygulamalarla vizyonunuzu hayata geçirin.",
    features: [
        SplashFeature(title: "Özellik 1", icon: "video"),
        SplashFeature(title: "Özellik 2", icon: "waveform")
    ],
    footer: "Şartlar ve koşullar geçerlidir.",
    cta: "Teklifi Kabul Et",
    secondaryCta: "Tüm Planları Gör",
    secondaryAction: {
        print("İkincil aksiyona tıklandı")
    }
) {
    print("Birincil aksiyona tıklandı")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Bilinen Sorunlar
- Bu fork iOS 17 ve macOS 14 destekler. iOS 18 / macOS 15 ve sonrasında TextRenderer, eski sistemlerde solma ve kaydırma geçişi kullanılır.
- Yeniden Boyutlandırma: Atlıkarınca modu Pro/Pro Max için optimize edilmiştir. Statik mod, daha küçük cihazları ve değişen içerik uzunluklarını yönetmek için bir ScrollView içerir.

## Telif Hakkı
App Store Screenshots © 2025 Apple Inc.

## Referans
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## X Üzerindeki İlgili Gönderiler
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Kombinasyonlar
[SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) ile birlikte kullanın, 2 kat etkili!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Lisans
MIT

## Şunlar Tarafından Desteklenmektedir
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
