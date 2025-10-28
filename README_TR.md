# Desktop Documentary - Gelişmiş Versiyon

Windows 95 nostaljisiyle modern web teknolojilerini harmanlayan, masaüstünde otomatik görsel kolajlar oluşturan gelişmiş web uygulaması. Kendi medya dosyalarınızı yükleyerek veya demo modunu kullanarak sanatsal dijital kompozisyonlar yaratın.

![Desktop Documentary TR Demo](demo-screenshot-tr.png)

## ✨ Özellikler

### 🎨 Temel Özellikler

- **Otantik Windows 95 Arayüzü**: Retro stil, görev çubuğu, masaüstü simgeleri ve klasik pencere kontrolleri
- **Akıllı Yerleştirme Sistemi**: Görsel açıdan hoş düzenler oluşturan pozisyonlama algoritması
- **Sürüklenebilir Pencereler**: Her pencereyi istediğiniz yere taşıyabilme
- **Karışık Medya Desteği**: Resim (JPG, PNG) ve video (MP4) dosyaları
- **Gerçek Zamanlı Saat**: Çalışan görev çubuğu saati

### 🔧 Gelişmiş Özellikler

- **Dosya Yükleme**: Bilgisayarınızdan çoklu dosya seçimi
- **Sürükle-Bırak**: Masaüstüne dosyaları doğrudan bırakma
- **Demo Modu**: Hızlıca test etmek için örnek görseller
- **Oynatma Listesi**: Medya sıralamasını değiştirme
- **Zamanlama Kontrolü**: Pencere açılma sürelerini ayarlama
- **Maksimum Pencere Sınırı**: Açık pencere sayısını kontrol etme
- **Rastgele Tohum**: Tekrarlanabilir düzenler için
- **Ekran Kaydı**: Desktop documentary'nizi kaydetme
- **Yerel Depolama**: Medya listesini tarayıcıda saklama

## 🚀 Hızlı Başlangıç

1. **`index_test.html`** dosyasını modern bir web tarayıcısında açın
2. **"📥 Medya Ekle"** ile kendi dosyalarınızı yükleyin veya **"✨ Demo"** butonunu tıklayın
3. İsteğe bağlı ayarları yapın (süre, maksimum pencere, rastgele tohum)
4. **"▶ Başlat"** ile desktop documentary'nizi başlatın
5. **"⏺ Kayıt"** ile deneyimi kaydedin

## 🎮 Kontroller

### Ana Butonlar

- **📥 Medya Ekle**: Bilgisayarınızdan dosya seçme
- **✨ Demo**: 5 örnek görsel yükleme
- **▶ Başlat**: Otomatik pencere açma sekansını başlatma
- **🔄 Reset**: Tüm pencereleri kapatma ve sıfırlama
- **⏺ Kayıt**: Ekran kaydını başlatma/durdurma

### Ayarlar

- **Süre**: Pencereler arası bekleme süresi (1-8 saniye)
- **Maks Pencere**: Aynı anda açık olabilecek maksimum pencere sayısı (3-20)
- **Rastgele Tohum**: Tekrarlanabilir düzenler için sayı girişi

### Pencere Kontrolleri

- **Sürükleme**: Pencere başlık çubuğundan sürükleyerek taşıma
- **\_**: Pencereyi şeffaflaştırma (minimize)
- **□**: Pencereyi normale döndürme (restore)
- **×**: Pencereyi kapatma

## 📁 Dosya Desteği

### Desteklenen Formatlar

- **Resimler**: JPG, JPEG, PNG, GIF, WebP
- **Videolar**: MP4, WebM, MOV

### Dosya Ekleme Yöntemleri

1. **Dosya Seçici**: "Medya Ekle" butonu ile klasik seçim
2. **Sürükle-Bırak**: Dosyaları doğrudan masaüstüne bırakma
3. **Demo Modu**: Picsum.photos'tan örnek görseller

## ⚙️ Gelişmiş Ayarlar

### Zamanlama Sistemi

```javascript
// Her medya öğesi için ayrı süre ayarlama
const mediaItems = [
  { name: "görsel1.jpg", type: "image", duration: 3000 }, // 3 saniye
  { name: "video1.mp4", type: "video", duration: 5000 }, // 5 saniye
];
```

### Rastgele Tohum Kullanımı

- Boş bırakın: Her seferinde farklı düzen
- Sayı girin: Aynı tohum ile aynı düzen

### Pencere Boyutları

Sistem otomatik olarak 3 boyut sınıfı atar:

- **Small**: Maksimum 300px genişlik
- **Medium**: Maksimum 400px genişlik
- **Large**: Maksimum 500px genişlik

## 🎨 Özelleştirme

### CSS Değişkenleri

```css
:root {
  --teal: #008080; /* Ana arka plan rengi */
  --deep: #004444; /* Koyu arka plan tonu */
  --bar: #c0c0c0; /* Görev çubuğu rengi */
  --title1: #000080; /* Pencere başlık rengi 1 */
  --title2: #0000ff; /* Pencere başlık rengi 2 */
}
```

### Akıllı Yerleştirme Algoritması

```javascript
function generateSmartPosition(index, total) {
  // Grid tabanlı sistem + organik varyasyon
  const cols = Math.ceil(Math.sqrt(total * 1.5));
  // Rastgele pozisyon hesaplama
  // Ekran sınırları kontrolü
}
```

## 🖥️ Tarayıcı Uyumluluğu

### Tam Destek

- **Chrome/Edge**: Tüm özellikler + ekran kaydı
- **Firefox**: Tüm özellikler + ekran kaydı
- **Safari**: Temel özellikler (ekran kaydı sınırlı)

### Gerekli API'ler

- File API (dosya yükleme)
- Drag & Drop API (sürükle-bırak)
- MediaRecorder API (ekran kaydı)
- Display Media API (ekran yakalama)
- Local Storage API (veri saklama)

## 📱 Responsive Tasarım

- **Desktop**: Tam özellik desteği
- **Tablet**: Temel özellikler (sürükleme sınırlı)
- **Mobil**: Görüntüleme modu (etkileşim sınırlı)

## 🎯 Kullanım Senaryoları

### Sanat & Tasarım

- Dijital kolaj oluşturma
- Görsel kompozisyon deneyimleri
- Rastgele sanat üretimi

### Eğitim & Sunum

- Retro bilgisayar deneyimi gösterimi
- Nostalji projeleri
- İnteraktif sunumlar

### İçerik Üretimi

- Sosyal medya videoları
- Sanatsal kayıtlar
- Desktop documentary'ler

### Kurulum & Sergi

- Galeriler için interaktif kurulumlar
- Müze sergileri
- Dijital sanat enstalasyonları

## 🔧 Sorun Giderme

### Pencereler Açılmıyor

- Medya dosyalarının yüklendiğini kontrol edin
- Tarayıcı konsolunu açıp hata mesajlarını kontrol edin
- Dosya formatlarının desteklendiğinden emin olun

### Kayıt Çalışmıyor

- HTTPS bağlantısı gerekli (yerel dosyalar için sorun olmaz)
- Ekran paylaşım iznini verin
- Chrome tarayıcısı önerilir
- Diğer sekmeleri kapatarak bellek boşaltın

### Performans Sorunları

- Maksimum pencere sayısını azaltın
- Büyük video dosyalarını optimize edin
- Tarayıcı sekmelerini kapatın
- RAM kullanımını kontrol edin

### Dosya Yükleme Sorunları

- Dosya boyutunu kontrol edin (>100MB problemli olabilir)
- Desteklenen formatları kullanın
- Tarayıcıyı yeniden başlatın

## 💾 Veri Yönetimi

### Yerel Depolama

- Medya listesi tarayıcıda saklanır
- Blob URL'ler oturum bazlıdır
- Temizlemek için: `localStorage.clear()`

### Dosya Güvenliği

- Dosyalar sadece tarayıcı belleğinde
- Sunucuya yükleme yapılmaz
- Gizlilik odaklı tasarım

## 🚀 Gelişmiş Kullanım

### Toplu İşlemler

```javascript
// Çoklu dosya yükleme
document.getElementById("filePicker").multiple = true;

// Programatik başlatma
start();

// Medya listesi manipülasyonu
mediaItems.push({ name: "yeni.jpg", type: "image", url: blobUrl });
```

### Özel Entegrasyon

```javascript
// API'dan medya yükleme
async function loadFromAPI(urls) {
  for (const url of urls) {
    mediaItems.push({ name: getFileName(url), type: "image", url });
  }
  renderPlaylist();
}
```

## 🤝 Katkıda Bulunma

Geliştirme fikirleri:

- [ ] Daha fazla dosya formatı desteği
- [ ] Ses efektleri ve müzik
- [ ] Tema sistemi (Mac OS, Linux vb.)
- [ ] Bulut depolama entegrasyonu
- [ ] Sosyal medya paylaşımı
- [ ] AI destekli otomatik kolaj
- [ ] WebGL animasyonları
- [ ] Multi-monitor desteği

## 📊 Teknik Detaylar

### Mimari

- Vanilla JavaScript (framework yok)
- CSS Grid & Flexbox layout
- Modern Web APIs
- Event-driven architecture

### Performans

- Lazy loading için Intersection Observer
- Memory management için Object URLs
- 60fps animasyonlar
- Optimize edilmiş DOM manipülasyonu

### Güvenlik

- XSS koruması
- Safe file handling
- No server communication
- Privacy-first approach

## 📄 Lisans

Bu proje açık kaynak kodludur. İstediğiniz gibi kullanabilir, değiştirebilir ve dağıtabilirsiniz.

## 🙏 Teşekkürler

- Windows 95 tasarım ilhamı için Microsoft
- Demo görseller için Picsum.photos
- Modern web teknolojileri için W3C
- Açık kaynak topluluğu

---

**Desktop Documentary TR** - Retro bilgisayar estetiğini modern web deneyimine taşıyan gelişmiş uygulama.

### Son Güncelleme: Ekim 2025

### Versiyon: 2.0 (Gelişmiş Türkçe Sürüm)
