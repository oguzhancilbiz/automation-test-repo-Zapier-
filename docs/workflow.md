# 🔄 İş Akış Şeması

Projenin mantıksal veri akışı aşağıdaki gibidir:

```mermaid
graph TD
    A[GitHub: Yeni Issue Açıldı] -->|Zapier 1| B(Google Sheets: Yeni Satır Ekle)
    C[GitHub: Issue Kapatıldı] -->|Zapier 2| D{Sheet'te URL'yi Bul}
    D -->|Eşleşme Tamam| E[Status Sütununu Güncelle: Closed]
