# ESP32 Tabanlı RFID Kontrol Sistemi

Bu proje, **ESP32 tabanlı bir RFID kontrol sistemi tasarımını** içermektedir. Sistem; RFID kart okuma, kullanıcı bilgilendirme, röle kontrolü ve ekran üzerinden durum gösterimi işlevlerini tek bir donanım yapısı üzerinde birleştirmek amacıyla geliştirilmiştir.

Bu çalışma, **Akelsan Teknik Güvenlik Sistemleri ve Yönetim Danışmanlığı Tic. Ltd. Şti.** bünyesinde yaptığım staj sırasında, şirketin talebi doğrultusunda tarafımca tasarlanmış ve geliştirilmiştir.

Proje kapsamında güç yönetimi, mikrodenetleyici bağlantıları, RFID haberleşmesi, LCD ekran entegrasyonu, röle sürme devresi ve sesli/görsel bildirim yapısı birlikte ele alınmıştır.

---

# Proje Özeti

Bu tasarım, RFID kart veya etiket okutulduğunda ilgili bilgiyi işleyebilen, kullanıcıya ekran ve bildirim elemanları üzerinden geri dönüş verebilen ve gerekli durumda röle çıkışı ile harici bir yükü kontrol edebilen gömülü bir sistem altyapısı sunmaktadır.

Sistem özellikle aşağıdaki uygulamalar için uygun bir altyapı sunar:

- Erişim kontrol sistemleri
- Kartlı geçiş uygulamaları
- Akıllı kilit sistemleri
- RFID tabanlı yetkilendirme sistemleri
- Gömülü otomasyon uygulamaları

---

# Sistem Bileşenleri

Projede yer alan temel donanım blokları aşağıdaki gibidir.

## Güç Katı

- 12V giriş hattı
- 5V regülasyon
- 3.3V regülasyon
- Filtreleme ve bypass kapasitörleri

## Mikrodenetleyici Katı

- ESP32-WROOM-32 modülü
- UART programlama başlığı
- Boot ve Enable butonları
- Gerekli pull-up ve pull-down bağlantıları

## RFID Arabirimi

- RFID okuyucu modül bağlantısı
- SPI haberleşme hatları
- 3.3V besleme altyapısı

## LCD Ekran Arabirimi

- I2C haberleşmeli LCD yapı
- PCF8574 tabanlı arayüz
- Kullanıcıya metin tabanlı bilgi gösterimi

## Röle Sürme Devresi

- Röle kontrol çıkışı
- 2N2222 NPN transistör ile sürme
- Koruma diyodu
- Harici yük anahtarlama altyapısı

## Bildirim Katı

- Buzzer sürme devresi
- LED uyarı çıkışı
- Görsel ve sesli kullanıcı geri bildirimi

---

# Projenin Amacı

Bu projenin temel amacı aşağıdaki konularda uygulamalı mühendislik deneyimi kazanmaktır:

- ESP32 tabanlı donanım tasarımı
- RFID modülü entegrasyonu
- Güç katı tasarımı
- Röle sürme devresi geliştirme
- I2C tabanlı LCD ekran entegrasyonu
- Kullanıcı bildirim devrelerinin tasarlanması
- Çok bloklu gömülü sistem mimarisi oluşturma

---

# Kullanılan Teknolojiler ve Bileşenler

- ESP32-WROOM-32
- RFID okuyucu modülü
- I2C LCD ekran altyapısı
- Röle
- 2N2222 transistör
- Buzzer
- LED bildirim devresi
- 5V ve 3.3V regülatör yapıları
- Şematik ve PCB tasarım araçları

---

# Teknik İçerik

Bu proje kapsamında aşağıdaki teknik başlıklara odaklanılmıştır:

- 12V girişten çoklu besleme hattı oluşturulması
- ESP32 için uygun besleme ve çevresel bağlantıların tasarlanması
- RFID haberleşme hatlarının mikrodenetleyiciye bağlanması
- I2C ekran arayüzünün sisteme entegre edilmesi
- Röle sürme devresinde transistör ve koruma diyodu kullanımı
- Buzzer ve LED ile kullanıcı bildirim altyapısı oluşturulması
- Modüler blok yapıda şematik organizasyonu

---

# Uygulama Alanları

Bu sistem aşağıdaki uygulamalarda kullanılabilir:

- Kartlı geçiş sistemleri
- Akıllı kilit sistemleri
- Yetkilendirme ve erişim kontrol sistemleri
- Gömülü otomasyon sistemleri
- RFID tabanlı kullanıcı doğrulama projeleri

---

# Proje Görselleri

## Ana Şematik

![Sematik](SCH1.png)
![Sematik](SCH2.png)

## RFID Okuyucu Kartı

![PCB](d-d.png)
![PCB](a-a.png)

---

# Geliştirme Potansiyeli

Proje aşağıdaki yönlerden geliştirilebilir:

- PCB tasarımının tamamlanması ve üretime hazırlanması
- Harici muhafaza tasarımı
- Yetkili / yetkisiz kart veritabanı yapısının eklenmesi
- Wi-Fi veya Bluetooth tabanlı uzaktan yönetim
- Log kayıt sistemi
- Kapı kilidi veya manyetik kilit entegrasyonu
- Gerçek zaman saati (RTC) eklenmesi
- Mobil uygulama veya web arayüzü ile kontrol

---

# Sonuç

Bu proje, RFID tabanlı kontrol sistemleri için gerekli temel donanım bloklarını bir araya getiren modüler bir gömülü sistem tasarımıdır.  

Güç elektroniği, mikrodenetleyici bağlantıları, haberleşme arayüzleri, kullanıcı bildirim elemanları ve röle kontrolü gibi farklı alt sistemleri tek bir mimari içinde birleştirmesi açısından kapsamlı bir mühendislik çalışmasıdır.
