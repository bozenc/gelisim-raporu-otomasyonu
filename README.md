# 📋 Gelişim Raporu Asistanı - BRKNET Digital

> BRKNET Digital tarafından öğretmenler için geliştirilen, E-Okul gelişim raporu formlarını otomatik dolduran, not tabanlı veya manuel çalışabilen, organik çeşitlilik üreten ve çevrimdışı simülatör desteği sunan premium Chrome eklentisi.  
> **Giriş gerektirmez · %100 Yerel ve Güvenli · Organik Varyasyon Teknolojisi.**

---


## 🚀 Kurulum

1. Zip olarak indirin.
2. Masaüstüne çıkartın.
3. chrome://extensions/   yoluna gidin ve https://prnt.sc/OOP6XOm8XpvG  resimdeki gibi "Paketlenmemiş Öğe Yükle" ile çıkardığınız klasörü seçin.
4. E-Okul gelişim raporu sayfasını açın — eklenti otomatik olarak devreye girer.
| 🎮 **Çevrimdışı Simülatör** | [Simülasyon Sayfasını Aç (Yerel)](demo.html) |



---

## 📌 Nedir?

**Gelişim Raporu Asistanı (BRKNET Digital)**, Millî Eğitim Bakanlığı'nın E-Okul sistemi üzerindeki gelişim raporu formlarını hızlı, hatasız ve organik bir şekilde doldurmak için tasarlanmış bir Chrome tarayıcı eklentisidir.

Desteklenen resmi sayfalar:
- **Ortaöğretim** → `e-okul.meb.gov.tr/OrtaOgretim/OKL/OOK07015.aspx`
- **İlköğretim** → `e-okul.meb.gov.tr/IlkOgretim/OKL/IOK10016.aspx`

---

## ✨ Özellikler

| Özellik | Açıklama |
|---|---|
| 📊 **Dinamik Not Modu** | E-Okul'dan dönem puanlarını otomatik çeker; özelleştirilebilir puan barajlarına göre seviye belirler. |
| 🎲 **Organik Çeşitlilik** | Raporların yapay görünmesini engellemek için öğrencilerin gelişim düzeylerini doğal olasılıklarla (±1 seviye) dalgalandırır. |
| 📏 **Seviye Kaydırma (Bias)** | Tüm sınıfın seviyesini genel düzeylerine göre toplu olarak yukarı (+1, +2) veya aşağı (-1, -2) kaydırır. |
| ⚙️ **Özel Puan Barajları** | Hangi notun hangi seviyeye (1-5) denk geleceğini öğretmenlerin kendisi yapılandırabilir. |
| 🎮 **İnteraktif Simülatör** | E-Okul'a giriş yapmadan eklentiyi sanal öğrencilerle test edebileceğiniz yerleşik sandbox ortamı (`demo.html`). |
| 👁️ **Popup Önizlemesi** | Eklenti simgesine tıklandığında açılan menü üzerinden panelin premium tasarımını doğrudan inceleme imkanı. |
| ✏️ **Gelişmiş Manuel Mod** | Belirli bir seviyede sabit, rastgele veya tanımlanan bir aralıkta formu doldurur. |
| 📂 **Ünite Seçimi** | Sayfadaki üniteleri/kazanımları otomatik tarar; doldurulacak üniteleri seçmenizi sağlar. |
| 🧹 **Güvenli Temizleme** | Rapor cevaplarını tek tıkla siler (E-Okul'un "Yeşil Temizle" butonlarıyla tam uyumludur). |
| 🔒 **Gizlilik & Güvenlik** | Hiçbir sunucuya veri göndermez; tüm işlemler tarayıcıda yerel olarak gerçekleşir. |

---

## 🎮 Çevrimdışı Simülasyon & Test

Eklentiyi e-Okul sayfalarını açmadan test etmek ve özelliklerini incelemek için iki seçenek sunulmuştur:

1. **Popup Arayüz Önizlemesi:** Tarayıcı çubuğundaki eklenti simgesine tıklayıp **"Panel Önizlemesi"** sekmesine geçerek panelin premium arayüz tasarımını inceleyebilirsiniz.
2. **İnteraktif Simülatör (Sandbox):** Popup'ta yer alan **"Simülasyon Sayfasını Aç ⚡"** butonuna basarak `demo.html` sayfasını açabilirsiniz. Bu sayfada:
   - **"Getir"** butonuna basarak mock öğrencileri içeri aktarabilir,
   - **"Üniteleri Tara"** diyerek kazanımları panele tanıtabilir,
   - **"Başlat"** diyerek otomasyonun çalışmasını canlı olarak izleyebilirsiniz.

---

## 📖 Kullanım Kılavuzu (Not Tabanlı Mod)

1. E-Okul'da **sınıf** ve **ders** seçin, **"Listele"** butonuna basın.
2. Eklenti panelinde **"Getir"** butonuna tıklayarak öğrenci notlarını çekin.
3. Gerekirse listedeki öğrencilerin onay kutularını kaldırarak otomasyondan hariç tutun.
4. Tercihinize göre **Seviye Kaydırma (Bias)** veya **Organik Çeşitlilik** seçeneklerini ayarlayın.
5. **"Başlat"** butonuna tıklayarak işlemi başlatın.

> **Varsayılan Puan → Seviye Dönüşüm Tablosu (Ayarlardan değiştirilebilir):**
> 
> | Puan Aralığı | Gelişim Seviyesi |
> |------|--------|
> | 85 ve üzeri | 5 (Çok İyi) |
> | 70 – 84 | 4 (İyi) |
> | 50 – 69 | 3 (Orta) |
> | 25 – 49 | 2 (Geliştirilmeli) |
> | 25'in altı | 1 |

---

## 🗂️ Proje Yapısı

```
gelisim-raporu-asistani-main/
├── manifest.json        # Eklenti manifest dosyası (Manifest V3)
├── background.js        # Service Worker — sekme yönetimi, iletişim ve simülasyon desteği
├── demo.html            # Çevrimdışı test ve simülasyon sandbox sayfası
├── content/
│   ├── panel.js         # Rapor sayfasına enjekte edilen premium arayüz ve otomasyon motoru
│   └── scraper.js       # Not sayfasından öğrenci notlarını çeken betik
├── popup/
│   ├── popup.html       # Eklenti popup arayüzü ve tasarım şablonu önizlemesi
│   └── popup.js         # Popup kontrol mantığı (simülatör tetikleyici, sekme geçişleri)
└── icons/
    ├── icon.svg         # Vektörel logo (BRKNET Indigo Teması)
    ├── icon16.png       # 16x16 eklenti simgesi
    ├── icon48.png       # 48x48 eklenti simgesi
    └── icon128.png      # 128x128 eklenti simgesi
```

---

## 🔧 Teknik Özellikler

- **Manifest Sürümü:** V3
- **İzinler:** `storage`, `tabs`
- **Host İzni:** `https://e-okul.meb.gov.tr/*`
- **Sürüm:** 2.2.0

---

## 🔒 Gizlilik & Güvenlik

- ✅ Giriş bilgileriniz (Kullanıcı adı, şifre) asla talep edilmez ve saklanmaz.
- ✅ Çekilen öğrenci notları ve ayarlarınız sadece tarayıcınızın yerel depolama alanında (`chrome.storage.local`) tutulur.
- ✅ Eklenti yalnızca `e-okul.meb.gov.tr` alan adında ve yerel simülasyon sayfasında (`demo.html`) aktifleşir.

---

## 📬 İletişim & Destek

Geri bildirimleriniz ve destek talepleriniz için:

- 📧 **E-posta:** [info@brknet.com](mailto:info@brknet.com?subject=Gelişim%20Raporu%20Asistanı%20-%20Geri%20Bildirim)
- 🌐 **Web Sitesi:** [brknet.com](https://brknet.com)

---

Telif Hakkı © 2026 BRKNET Digital. Tüm hakları saklıdır.

<p align="center">
  <b>Gelişim Raporu Asistanı - BRKNET Digital</b> · v2.2.0 · Öğretmenler için ❤️
</p>
