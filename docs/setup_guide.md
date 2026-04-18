# 🛠️ Zapier Kurulum Rehberi

Bu döküman, GitHub ve Google Sheets arasındaki otomasyonun adım adım nasıl kurulacağını açıklar.

## 1. Adım: GitHub ve Google Sheets Bağlantısı
* Zapier hesabınıza giriş yapın ve "Create Zap" butonuna tıklayın.
* **App:** GitHub, **Trigger Event:** "New Issue" seçin.
* Google Sheets hesabınızı bağlayın ve verilerin kaydedileceği dosyayı seçin.

## 2. Adım: Veri Eşleştirme (Mapping)
Yeni bir issue açıldığında aşağıdaki alanların eşleştiğinden emin olun:
- **Title:** Issue Title
- **Description:** Issue Body
- **URL:** html_url (Benzersiz anahtar olarak kullanılacak)

## 3. Adım: Güncelleme Akışı (Update Flow)
Kapatılan issue'ları takip etmek için ikinci bir Zap kurun:
- **Filter:** State = "closed" olanları filtreleyin.
- **Action:** Google Sheets "Lookup Row" adımını ekleyerek `html_url` üzerinden satırı bulun.
- **Update:** Bulunan satırın `Status` hücresini "Closed" olarak güncelleyin.
