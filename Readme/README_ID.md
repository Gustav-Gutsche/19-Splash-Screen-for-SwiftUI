# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### Layar Splash Baru untuk SwiftUI

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## Versi
**27.0.3 (Rilis Stabil)** <br>
*Dioptimalkan untuk interaksi performa tinggi tanpa hambatan.*

- **Carousel Tak Terbatas yang Mulus:** Logika indeks virtual baru mencegah "kartu terbang" dan memastikan rotasi tak terbatas yang lancar.
- **Performa Teroptimasi:** Rendering dipercepat Metal (`drawingGroup`) dan pembaruan per-frame yang efisien melalui `RunLoop`.
- **Scrolling Momentum:** Gestur interaktif berbasis kecepatan yang sangat mulus dengan nuansa deselerasi native.
- **Dukungan AsyncImage:** Penanganan URL yang telah divalidasi sebelumnya untuk pemuatan gambar jarak jauh tanpa lag.
- **Dua Mode Tampilan:** Pilih antara tata letak dinamis `.carousel` dan elegan `.static`.
- **Efek Teks Lanjutan:** Rendering teks dan transisi yang indah menggunakan fitur SwiftUI 6.0.

## Lingkungan / Diuji pada
- 📲 Memerlukan iOS 17.0+ / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## Cara Penggunaan
Tambahkan paket ke proyek Anda: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### Mode Carousel (Default)
Pengalaman interaktif klasik dengan gambar yang berputar.
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // Mendukung URL jarak jauh!
    ],
    title: "Selamat datang di",
    product: "Apple TV",
    caption: "Telusuri semua film, acara TV, dan lainnya.",
    cta: "Tonton Sekarang"
) {
    print("Tombol Aksi Diketuk")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### Mode Statis (BARU)
Tata letak bersih dan dapat digulir, cocok untuk pengenalan produk.
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "Creator Studio",
    product: "Gratis 3 bulan Creator Studio.",
    caption: "Wujudkan visi Anda dengan aplikasi yang powerful.",
    features: [
        SplashFeature(title: "Fitur 1", icon: "video"),
        SplashFeature(title: "Fitur 2", icon: "waveform")
    ],
    footer: "Syarat dan ketentuan berlaku.",
    cta: "Terima Penawaran",
    secondaryCta: "Lihat Semua Paket",
    secondaryAction: {
        print("Aksi sekunder diketuk")
    }
) {
    print("Aksi utama diketuk")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## Masalah yang Diketahui
- Fork ini mendukung iOS 17 dan macOS 14. TextRenderer digunakan pada iOS 18 / macOS 15 atau lebih baru; sistem lama memakai transisi fade dan offset.
- Perubahan Ukuran: Mode Carousel dioptimalkan untuk Pro/Pro Max. Mode Statis menyertakan ScrollView untuk menangani perangkat yang lebih kecil dan panjang konten yang bervariasi.

## Hak Cipta
Screenshot App Store © 2025 Apple Inc.

## Referensi
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## Postingan Terkait di X
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## Kombinasi
Gunakan [SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) bersama-sama, 2X lebih efektif!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## Lisensi
MIT

## Didukung Oleh
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
