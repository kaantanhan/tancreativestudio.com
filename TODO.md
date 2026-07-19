# TAN Creative — Yapılacaklar

> Çalışma dosyası. Canlı siteye **gitmez** (deploy `exclude` listesinde).
> Madde tamamlandıkça `- [ ]` → `- [x]`. **Güncel: 2026-07-18** (kod taranarak doğrulandı)

---

## 🔴 0. ACİL — canlıda kırık
- [ ] **press.html'de 3 kırık link**: `press-02.html`, `press-03.html`, `press-04.html` dosyaları **yok** ama press.html (satır 304/309/314) onlara link veriyor → tıklayan kullanıcı **404** alıyor.
      Seçenekler: (a) 3 sayfayı press-01 şablonundan üret, (b) gerçek içerik gelene kadar o kartların linkini kaldır.
- [ ] Kök dizindeki `orks"#` (kazara oluşmuş) ve `.DS_Store` dosyalarını sil; `.gitignore`'a `.DS_Store` ekle.

## 🟠 1. İçerik — en yüksek etki (site "hazır" görünmesini bu belirliyor)
Şu an sitenin büyük kısmı placeholder. Öncelik: metinler → görseller.

**Proje sayfaları (work-03…08 tamamen placeholder — her birinde 7 adet "Görsel Yakında")**
- [ ] work-03 — Allianz / Point Cloud
- [ ] work-04 — Emaar Artbox
- [ ] work-05 — "Eşik" Exhibition
- [ ] work-06 — Les Benjamins New Year
- [ ] work-07 — Borusan Contemporary / Edward Burtynsky
- [ ] work-08 — Borusan Sanat / 2025 Visual Identity

**Metinler (8 work sayfasının hepsinde "hazırlanıyor" placeholder'ı var — work-01 ve 02 dahil)**
- [ ] work-01 (Akbank) ve work-02 (Paribuart): Overview + Approach + spread özeti
- [ ] work-03…08: tüm gövde metinleri
- [ ] Tüm projelerde **Credits** (Creative Direction / Design / Development / Motion / Photography) — şu an "—"

**Press**
- [ ] press-01 + press.html kartlarındaki **Lorem ipsum** → gerçek içerik
- [ ] Press görselleri (boş gri `.ph` kutuları)
- [ ] index.html'deki press kartları da lorem — gerçek başlık/kaynak/özet

**Kart kapakları**
- [ ] work-03…08 kartları (index'te 3, works.html'de 6 adet "Görsel Yakında") → kapak görseli/videosu

## 🟡 2. SEO / paylaşım — hızlı kazanç
- [ ] **og etiketleri sadece index.html'de var** (6 adet); diğer **14 sayfada hiç yok** → WhatsApp/LinkedIn/X'te paylaşılınca önizleme çıkmıyor. En azından og:title + og:description + og:image ekle.
- [ ] **Favicon yok** (hiçbir sayfada referans yok) → sekmede boş ikon.
- [ ] og:image için paylaşım görseli üret (1200×630).
- [ ] `sitemap.xml` + `robots.txt` (opsiyonel ama faydalı)

## 🟡 3. Performans
- [ ] `images/akbank-kapak.mp4` **6.2 MB** — ana sayfa hero'su, ilk açılışı yavaşlatıyor. Daha agresif sıkıştır (hedef ~2–3 MB) veya daha kısa kes.
- [ ] Diğer büyük videolar: akbank-3 (2.3 MB), akbank-2 (1.9 MB), paribuart-4 (1.2 MB)
- [ ] Kullanılmayan dosyaları sil: `images/hero.mp4` (936 KB), `images/hero.jpg` — artık hero videosu akbank-kapak
- [ ] Videolarda `poster` + `preload` gözden geçir (mobil veri tüketimi)

## 🟢 4. İçerik/bölüm geliştirme
- [ ] **Capabilities** sayfası: içerik genişletme (şu an 3 kısa madde)
- [ ] **Clients**: eksik marka logoları / sıralama gözden geçir
- [ ] **404 sayfası** yok — siteyle uyumlu bir 404 ekle
- [ ] "Görsel Yakında" placeholder'ı için daha zarif bir tasarım (boş gri kutu yerine)

## 🔵 5. Bilinen küçük sorunlar
- [ ] **Borusan Sanat logosu** SVG'si bozuk (üst üste binen tekrarlı yazılar) — temiz SVG ile değiştir *(daha önce "sonra" demiştiniz)*
- [ ] Aksan rengi sistemi (opsiyonel)

## ⚪ 6. Test / doğrulama
- [ ] Gerçek iPad'de nav renk uyumu (son düzeltme sonrası) — deploy sonrası kontrol
- [ ] Gerçek cihazda yumuşak scroll hissi (Lenis tarzı lerp) — çok ağır/hafif mi?
- [ ] Safari + Firefox'ta genel kontrol (şu ana kadarki testler Chromium)
- [ ] Klavye ile gezinme + odak halkaları (erişilebilirlik)

---

## ✅ Tamamlananlar (referans)
- [x] Giriş intro'sunun bazen takılması → 4 katmanlı fail-safe (font timeout, try/catch, arka plan sekmesi, 6sn backstop)
- [x] iPad/tablette nav renk uyumu çalışmıyordu → imleçten ayrıştırıldı, her cihazda çalışıyor
- [x] Locomotive/Lenis tarzı yumuşak scroll (3 katmanlı güvenlik ağıyla)
- [x] Mobil clients: 3 sütun grid, optik normalizasyon (oran-bazlı ol-* sınıfları), per-logo ince ayarlar
- [x] Services → **Capabilities** (tüm sayfalar + dosya adı + anchor)
- [x] Ana sayfa Selected Works 8 → 5 kart
- [x] İmleç yazıları (PLAY/EXPLORE/READ) her zeminde parlaklığa göre siyah/beyaz
- [x] Masaüstü TAN logosu %20 büyütüldü + banda dikey ortalandı
- [x] Kurum logoları: Emaar / Sinopale / Demir Tasarım / Base / Unrig yenilendi, İRHM kaldırıldı
- [x] Logo boyut ve sıralama ince ayarları (birçok tur)
- [x] about.html zenginleştirildi (manifesto + Approach + Expertise + Clients + Contact)
- [x] capabilities.html + press.html toplu sayfaları
- [x] Footer linkleri (LinkedIn, Instagram, Privacy), X kaldırıldı
- [x] 8 proje ayrı sayfada (work-01…08); work-01 ve 02 görselleri dolu
- [x] Mobil sticky header, iç sayfa geçiş animasyonu, intro atlama, i/İ locale düzeltmesi
- [x] Ana sayfa hero videosu = Akbank / Niyetler 2
- [x] FTP deploy timeout (büyük video yükü) düzeltmesi
