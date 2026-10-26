# Personel İzin Takip — Android proje kaynağı

Bu Android Studio projesi, çevrimdışı çalışan mobil izin takip arayüzünü WebView içinde açar.

## APK oluşturma (Android Studio)
1. ZIP dosyasını bir klasöre çıkarın.
2. Android Studio'da `PersonelIzinTakipAndroid` klasörünü açın.
3. Gradle senkronizasyonunun tamamlanmasını bekleyin.
4. `Build > Build Bundle(s) / APK(s) > Build APK(s)` seçin.
5. APK şu konumda oluşur: `app/build/outputs/apk/debug/app-debug.apk`

## GitHub Actions ile APK oluşturma
1. Proje dosyalarını yeni bir GitHub deposuna yükleyin.
2. `Actions` sekmesinden **Build Android APK** iş akışını çalıştırın (veya `main` dalına push edin).
3. Tamamlanan iş akışındaki `personel-izin-takip-apk` artifact'ini indirin; ZIP içindeki `app-debug.apk` kurulum dosyasıdır.

## Mevcut sürümün sınırları
- Veriler cihazdaki uygulama WebView depolamasında tutulur.
- Bu sürümde ortak sunucu, kullanıcı hesabı veya cihazlar arası eşitleme yoktur.
- Verilerin kaybolmaması için uygulamadaki Yedekleme ekranından JSON yedeği alın.
- Bu proje kaynak paketi APK'nın kendisi değildir; Android SDK/Gradle ile derlenmesi gerekir.
