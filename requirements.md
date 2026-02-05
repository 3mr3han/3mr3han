# Personel Giriş/Çıkış Kart Okuma Sistemi Gereksinimleri

## 1. Amaç ve Kapsam
Bu doküman, personelin kart üzerinden giriş/çıkış hareketlerinin donanım tarafından okunarak kayıt altına alındığı, puantaj ve mesai süreçlerinin yönetildiği masaüstü (EXE) uygulamasının gereksinimlerini tanımlar.

## 2. Kurulum ve Dağıtım
- Uygulama bir **Windows EXE** olacaktır.
- Kurulum paketi, **birden fazla bilgisayara kolay kurulum** yapılabilecek şekilde hazırlanacaktır.
- Donanım ile bağlantı kuracak sürücü/servisler kurulumla birlikte otomatik yapılandırılacaktır.

## 3. Kart Okuma ve Kayıt Kuralları
- Okumalar **donanım üzerinden** yapılacaktır.
- **Puantaj için** bir personelin **ilk ve son kart okuma saati** esas alınacaktır.
- **Ara okumalar**, süper admin ve admin tarafından tanımlanan **çalışma/mola saatleri** içinde ayrıca kayıt altına alınacaktır.
- Mesai başlangıcına **10 dakika tolerans** uygulanacaktır.

## 4. Mesai (Ekstra Mesai) Yönetimi
- Ekstra mesaiye kalacak personel **program üzerinden seçilecektir** (admin belirler).
- Mesai bitiminde sistem **otomatik olarak ekstra mesaiye geçecektir**.
- Mesaiye eklenmeyi unutulan personel, **admin yetkisiyle sonradan eklenebilecektir**.
- Eklenen personelin **kayıt/okuma saati neyse sistemde o saat geçerli olacaktır**.

## 5. Çalışma Takvimi ve Tatiller
- İşyeri çalışma saatleri **admin ve süper admin tarafından manuel olarak girilecektir**.
- **Hafta sonları, bayramlar ve resmi tatiller** tanımlanabilir olacaktır.

## 6. Ücret ve Bölüm Bilgileri
- Her personelin **bölümü** ve **ücreti** sistemde tanımlı olacaktır.
- **Kayıtsız personel olmayacaktır** (tüm personel kaydı zorunlu).
- **Ücretleri süper admin** belirler.

## 7. Kullanıcı Rolleri ve Yetkiler
Uygulama arayüzünde 3 rol bulunacaktır:

### 7.1 Süper Admin
- **Tek kişi** (işletme sahibi/müdür).
- **Tüm izinlere sahiptir**.

### 7.2 Admin
- Bölüm şefi ve müdürler.
- **Ekleme/çıkarma/değişiklik** yetkileri vardır.
- Ekstra mesai atama ve gün içi mesai belirleme yetkisine sahiptir.

### 7.3 İzleyici (Seyirci)
- Muhasebe ve kayıt çıktısı alma görevindedir.
- **Sadece görüntüleme ve rapor/çıktı** yetkisi vardır.

## 8. Not Ekleme
- Admin, personele ait kayıtlara **not ekleyebilir**.

## 9. Veri Çıktısı ve Arşivleme
- İzleyici rolü, kayıtların **çıktısını alabilir** ve **arşivleme** yapabilir.

## 10. Açık Noktalar (Onay Bekleyen)
Bu maddeler proje başlangıcında netleştirilmelidir:
- Kullanılacak kart okuma cihazı ve sürücü/SDK bilgileri.
- Veri tabanı tipi (lokal mi, merkezi mi?).
- Rapor formatları (PDF/Excel vb.).
- Çoklu bilgisayar kurulumunda veri senkronizasyon yöntemi.
