# LUNA AI Online v1 — Android kaynak projesi

Bu dosya APK değil; Android Gradle projesidir. GitHub Actions ile `assembleDebug` derlenebilir. **Derleme ve gerçek cihaz testi yapılmamıştır.**

## Özellikler
- Birden çok kurgusal yetişkin karakter ve karakter başına sohbet geçmişi
- OpenAI uyumlu `chat/completions` HTTPS API'sine bağlanma
- OpenAI uyumlu `images/generations` HTTPS API'sinden URL veya b64_json görseli gösterme
- Sohbet ve görsel API endpoint/model/anahtarını uygulama içinden girme

## Sınırlamalar
- API anahtarı SharedPreferences içinde şifrelenmeden saklanır; üretim için Android Keystore ile korunmalıdır.
- Görseller kalıcı galeriye kaydedilmez. Karakter yüz tutarlılığı garanti edilmez.
- PIN kilidi ve ödeme entegrasyonu henüz yoktur.
- Aynı API anahtarı iki serviste geçerli olmayabilir; bu sürüm tek anahtar kullanır.
- Kullanılan sağlayıcının kuralları ve ücretleri geçerlidir. Ücretsiz veya sınırsız olduğu iddia edilmez.
- İnternet ve çalışan servis olmadan sohbet/görsel üretimi çalışmaz.

## Telefonda APK üretme
GitHub'da **private** depo açın; ZIP içeriğini (üst klasör değil, içindeki dosyaları) depoya yükleyin. Actions sekmesindeki `Android APK` iş akışını çalıştırın. Başarılıysa `LUNA-AI-debug-APK` artifact dosyasından APK alın. GitHub'a dosya yüklemek için ZIP'i açmanız gerekir. Debug APK kişisel test içindir.
