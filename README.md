# 🤖 GitHub Issue to Google Sheets Automation

Bu proje, GitHub üzerindeki iş akışını otomatize etmek için tasarlanmıştır. Zapier kullanarak geliştirilen bu sistem, ekiplerin hata takibini (bug tracking) Google Sheets üzerinden canlı olarak izlemesine olanak tanır.

## 🛠️ Sistem Nasıl Çalışıyor?

### 1. Otomatik Kayıt (Creation Zap)
- **Tetikleyici:** GitHub'da yeni bir `issue` açıldığında çalışır.
- **Eylem:** Issue başlığı, içeriği, açılış tarihi ve benzersiz URL'sini Google Sheets'e yeni bir satır olarak ekler.

### 2. Otomatik Güncelleme (Update Zap)
- **Tetikleyici:** GitHub'da bir `issue` kapatıldığında (State = Closed) çalışır.
- **Eylem:** Google Sheets'teki benzersiz URL'yi arayıp bulur ve o satırdaki `Status` bilgisini anında "Closed" olarak günceller.

## 📁 Proje Dosyaları
- `documentation/`: Zapier konfigürasyon adımlarının ekran görüntüleri.
- `sample-data/`: Otomasyon sonucunda oluşan Google Sheets tablosu örneği.

## 🚀 Kazanımlar
- Manuel veri girişi ortadan kaldırıldı.
- Hata takip süreçlerinde %100 güncellik sağlandı.
- Pro Proje gereksinimleri, arama ve güncelleme mantığıyla simüle edildi.
