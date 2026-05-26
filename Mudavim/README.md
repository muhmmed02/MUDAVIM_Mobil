# 📱 MUDAVIM Mobil Uygulama

MUDAVIM SaaS platformunun müşteri taraflı mobil web uygulaması. Sipariş verme, sadakat puanı takibi, kupon kullanımı ve işletme menüsü görüntüleme özelliklerini içerir.

---

## 🛠️ Teknoloji

- **Dil:** React (CDN üzerinden, build gerektirmez)
- **Stil:** Vanilla CSS
- **Dosya Yapısı:** Tek sayfa uygulama (SPA) — `index.html`
- **Backend:** Django REST (MUDAVIM backend reposu)

---

## 📁 Dosyalar

```
MUDAVIM_Mobil/
├── index.html       ← Ana uygulama (tüm ekranlar buradadır)
├── styles.css       ← Stil dosyası
├── manifest.json    ← PWA manifest
├── sw.js            ← Service Worker (offline destek)
└── api-config.js    ← Sunucu URL ayarı (bunu güncelle!)
```

---

## 🚀 Kurulum & Çalıştırma

### Gereksinimler
- Sadece modern bir tarayıcı yeterli (Chrome, Safari, Firefox)
- Backend sunucusunun çalışıyor olması gerekir ([MUDAVIM Backend](https://github.com/abuzerduzen/MUDAVIM))

### Adımlar

**1. Repoyu klonla:**
```bash
git clone https://github.com/muhmmed02/MUDAVIM_Mobil.git
```

**2. Backend URL'sini ayarla:**

`api-config.js` dosyasını aç ve `API_BASE_URL` değerini backend sunucunun adresine göre güncelle:

```js
// Yerel geliştirme için:
const API_BASE_URL = "http://127.0.0.1:8001";

// Cloudflare Tunnel veya ngrok ile dışarıdan erişim için:
const API_BASE_URL = "https://senin-tunnel-adresin.trycloudflare.com";
```

**3. Uygulamayı aç:**

`index.html` dosyasını tarayıcıda direkt aç **ya da** basit bir HTTP sunucusu başlat:

```bash
# Python ile yerel sunucu (opsiyonel):
python -m http.server 3000
# Sonra tarayıcıda: http://localhost:3000
```

> ✅ Build gerekmez, npm/node kurmanıza gerek yok.

---

## 🔗 Backend Bağlantısı

Bu uygulama [MUDAVIM Backend](https://github.com/abuzerduzen/MUDAVIM) ile çalışır.

Backend çalışmadan uygulama veri çekemez. Backend kurulumu için o reponun README'sine bakın.

---

## 📲 PWA (Telefona Ekle)

Uygulama Progressive Web App (PWA) olarak tasarlanmıştır:

1. Chrome'da uygulamayı aç
2. Adres çubuğunun yanındaki **"Yükle"** veya **"Ana Ekrana Ekle"** butonuna bas
3. Uygulama telefona native app gibi kurulur

---

## 🌍 Dil Desteği

Uygulama **Türkçe** ve **İngilizce** dil desteğine sahiptir. Profil ekranından dil değiştirilebilir.

---

## 📂 Notlar

- `fix.js`, `fix.py`, `fix2.py` geliştirme sürecinde kullanılan geçici dosyalardır, üretimde gerekmez
- `index_broken.html` yedek dosyadır, silinebilir
