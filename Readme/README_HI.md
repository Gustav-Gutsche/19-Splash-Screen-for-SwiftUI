# SplashScreenKit

> **Fork release 27.0.3:** iOS 17.0+ / macOS 14.0+. [Current installation and verification](../README.md#install-this-fork).
### SwiftUI के लिए एक नया स्पलैश स्क्रीन

| Region | Languages |
| :--- | :--- |
| **Global** | [English](../README.md) |
| **Asia** | [廣東話](./README_HK.md) [繁體中文](./README_TW.md) [简体中文](./README_CN.md) [日本語](./README_JP.md) [한국어](./README_KR.md) [Indo](./README_ID.md) [हिन्दी](./README_HI.md) |
| **Europe** | [Français](./README_FR.md) [Deutsch](./README_DE.md) [Español](./README_ES.md) [Русский](./README_RU.md) [Polski](./README_PL.md) [Türkçe](./README_TR.md) |
| **ME & Africa** | [العربية](./README_AR.md) [Kiswahili](./README_SW.md) |

<img width="1585" alt="Screenshot 2025-02-10 at 8 18 53 PM" src="https://github.com/user-attachments/assets/7f35a079-f74d-4c35-8f25-ea3239cc645f" />

## वर्शन
**27.0.3 (स्थिर रिलीज़)** <br>
*बिना किसी लैग के उच्च-प्रदर्शन इंटरैक्शन के लिए अनुकूलित।*

- **निर्बाध अनंत हिंडोला (Carousel):** नया वर्चुअल-इंडेक्स लॉजिक "उड़ते हुए कार्ड" को रोकता है और सुचारू अनंत रोटेशन सुनिश्चित करता है।
- **प्रदर्शन अनुकूलित:** मेटल-त्वरित रेंडरिंग (`drawingGroup`) और `RunLoop` के माध्यम से कुशल प्रति-फ़्रेम अपडेट।
- **मोमेंटम स्क्रॉलिंग:** देशी मंदी के अनुभव के साथ मक्खन जैसा चिकना, वेग-आधारित इंटरैक्टिव जेस्चर।
- **AsyncImage समर्थन:** बिना किसी देरी के रिमोट इमेज लोडिंग के लिए पूर्व-सत्यापित URL हैंडलिंग।
- **दो डिस्प्ले मोड:** गतिशील `.carousel` और सुरुचिपूर्ण `.static` लेआउट के बीच चयन करें।
- **उन्नत टेक्स्ट प्रभाव:** SwiftUI 6.0 सुविधाओं का उपयोग करके सुंदर टेक्स्ट रेंडरिंग और ट्रांज़िशन।

## वातावरण / परीक्षण किया गया
- 📲 iOS 17.0+ आवश्यक / macOS 14.0+
- Swift 6.0
- Xcode 16.0+

## उपयोग कैसे करें
अपने प्रोजेक्ट में पैकेज जोड़ें: ```https://github.com/Gustav-Gutsche/19-Splash-Screen-for-SwiftUI```

### हिंडोला मोड (डिफ़ॉल्ट)
घूमती छवियों के साथ क्लासिक इंटरैक्टिव अनुभव।
```swift
SplashScreen(
    images: [
        Photo("ImageName1"),
        Photo("https://example.com/image.jpg") // रिमोट URL समर्थित!
    ],
    title: "में आपका स्वागत है",
    product: "Apple TV",
    caption: "सभी फ़िल्में, टीवी शो और बहुत कुछ ब्राउज़ करें।",
    cta: "अभी देखें"
) {
    print("एक्शन बटन दबाया गया")
}
```

<img src="https://github.com/user-attachments/assets/28c8a5dc-cb8c-4aa4-b0a8-d7139ce3cefc" width="350" />

### स्थिर मोड (नया)
एक साफ, स्क्रॉल करने योग्य लेआउट उत्पाद परिचय के लिए उपयुक्त।
```swift
SplashScreen(
    mode: .static,
    images: [Photo("https://url.to/header_image.jpg")],
    title: "क्रिएटर स्टूडियो",
    product: "3 महीने का क्रिएटर स्टूडियो मुफ़्त।",
    caption: "शक्तिशाली ऐप्स के साथ अपनी दृष्टि को जीवंत करें।",
    features: [
        SplashFeature(title: "सुविधा 1", icon: "video"),
        SplashFeature(title: "सुविधा 2", icon: "waveform")
    ],
    footer: "नियम और शर्तें लागू।",
    cta: "ऑफर स्वीकार करें",
    secondaryCta: "सभी प्लान देखें",
    secondaryAction: {
        print("माध्यमिक क्रिया दबाई गई")
    }
) {
    print("प्राथमिक क्रिया दबाई गई")
}
```

<img src="https://github.com/user-attachments/assets/44f9aeef-7906-4251-b338-f9504b30b278" width="350" />

## ज्ञात समस्याएँ
- यह फ़ोर्क iOS 17 और macOS 14 का समर्थन करता है। iOS 18 / macOS 15 और नए संस्करणों में TextRenderer इस्तेमाल होता है; पुराने संस्करणों में फ़ेड और ऑफ़सेट ट्रांज़िशन होता है।
- आकार बदलना: हिंडोला मोड Pro/Pro Max के लिए अनुकूलित है। स्थिर मोड में छोटे उपकरणों और अलग-अलग सामग्री लंबाई को संभालने के लिए ScrollView शामिल है।

## कॉपीराइट
App Store स्क्रीनशॉट © 2025 Apple Inc.

## संदर्भ
[Creating visual effects with SwiftUI - Apple Developer](https://developer.apple.com/documentation/swiftui/creating-visual-effects-with-swiftui)

## X पर संबंधित पोस्ट
https://x.com/1998design/status/2019418746553790664 <br>
https://x.com/1998design/status/1888641485303878110 <br>
https://x.com/1998design/status/1888945523845140677

## संयोजन
[SwiftNEWKit](https://github.com/1998code/SwiftNEWKit) का एक साथ उपयोग करें, 2X प्रभावी!
<br><br>
<img height=300 src="https://github.com/user-attachments/assets/cc88b31d-326f-4a43-9e6a-5f583fcf153b" />

## लाइसेंस
MIT

## द्वारा समर्थित
<a href="https://m.do.co/c/ce873177d9ab">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/SVG/DO_Logo_horizontal_blue.svg" width="201px">
</a>
