# EE 533 Information Theory - Çalışma Planı

**Ders:** EE 533 Information Theory, METU EEE
**Hoca:** Barış Nakiboğlu
**Midterm:** 9 Mayıs 2026, Cumartesi, 11:00-14:00, EA209
**Hazırlayan:** Kerem Recep Gür

---

## Sınav Kuralları

- 3 saat (11:00-14:00)
- 5 çift taraflı el yazısı cheat sheet serbest (= 10 yüzey)
- Hesap makinesi ve kitap yasak
- Kapsam: 30 Nisan dersine kadar olan her şey
- **Hariç:** W06 slaytları 4-8 (fixed-length source coding için error exponents)
- Sonunda çözümler ODTÜClass'a yüklenecek

## GÜNCELLEME (24 Nisan)

### Barış'ın Resmi Duyurusu

"Exam covers all material discussed up to and including the lecture on April 30th, except for the error exponents for the fixed-length source coding problem (i.e., slides 4-8 of Week 6). We will cover these error exponents in the make-up lecture at 10:30 on Thursday, April 30."

Yani:
- 30 Nisan'a kadar işlenen her şey sınavda
- 30 Nisan'daki make-up dersi (error exponents) **hariç**
- W06 slaytları 4-8 **hariç**

### Kapsam Değişikliği

W10 slaytı açıldı ve **tamamen Differential Entropy (Ch. 8)**. Hoca programı hızlandırmış. Yani sınav kapsamı:
- Chapter 2 (Measures of info)
- Chapter 3 (AEP)
- Chapter 5 (Source coding)
- Chapter 7 (Channel capacity)
- **Chapter 8 (Differential entropy)** ← YENİ, W10'da işlendi
- Muhtemelen W11 dersi (27 Nisan Pazartesi) de kapsamda olacak — o slaytı bekle

### Durum Tespiti

- Bugün: 24 Nisan (başlangıç planı 20 Nisan'dı → 4 gün kayıp)
- Sınav: 9 Mayıs
- Kalan: 15 gün
- Şenlik: 6-9 Mayıs
- **Etkin çalışma süresi: 24 Nisan - 5 Mayıs = 12 gün**

## Ders Kapsamı (Güncel)

| Hafta | Konu | Kitap | Sınavda? |
|-------|------|-------|----------|
| 1-3 | Measures of info + AEP | Ch. 2, 3 | Evet |
| 4-6 | Source Coding | Ch. 5 | Evet (W06 s4-8 hariç) |
| 7-9 | Channel Coding | Ch. 7 | Evet |
| 10 | Differential Entropy | Ch. 8 | **Evet** (önce dışındaydı, içeri girdi) |
| 13-14 | Gaussian Channel | Ch. 9 | Hayır |
| 16 | Rate-Distortion | Ch. 10 | Hayır |

**Kitap versiyonu:** Cover & Thomas, Elements of Information Theory, **2. baskı (2006)**. Dizinde `Elements of Information Theory - 2005 - Cover.pdf`.

1. baskı (1991) kullanma - bölüm numaraları farklı. Slepian-Wolf 1. baskıda Ch. 14, 2. baskıda Ch. 15. Syllabus 2. baskıya göre.

---

## 7 Çekirdek Araç

Tüm slaytlardaki ispatların büyük çoğunluğu bu 7 aracın kombinasyonu:

| # | Araç | Nerede kullanılıyor |
|---|------|---------------------|
| 1 | Jensen's inequality | KLD non-negativity, joint convexity, monotonicity, H ≤ log\|supp\|, conditioning reduces entropy |
| 2 | Chain rules (entropy, MI, KLD) | Neredeyse her ispatın temeli |
| 3 | Conditioning reduces entropy / CMI ≥ 0 | DPI, her converse, product channel capacity |
| 4 | Fano's inequality | Tüm converse ispatlarında |
| 5 | KLD ≥ 0 | L ≥ H, DPI for KLD, excess redundancy |
| 6 | Typicality counting | Her achievability ispatında + strong converse (source coding) |
| 7 | Chebyshev / concentration | WLLN → AEP, tüm strong converse'ler |

### Destekleyici Araçlar

| # | Araç |
|---|------|
| 8 | DPI (Data Processing Inequality) — #2 + #3'ten türetilir |
| 9 | WLLN / AEP — #7'den türetilir |
| 10 | Random coding + Markov existence argument |
| 11 | Union bound |

---

## Haftalık Slayt İçeriği

| Slayt | Konu | Temel İspatlar |
|-------|------|----------------|
| W01 | σ-algebra, probability, convex functions, Jensen, entropy, joint/conditional entropy, MI, chain rules | Jensen, chain rule for entropy, conditioning reduces entropy |
| W02 | Markov chains, DPI, Fano, Rényi, convergence, WLLN, SLLN, CLT, Berry-Esseen, AEP, typical sets | DPI, Fano, WLLN (Chebyshev), AEP, joint typicality |
| W03 | KL divergence properties (chain rules, DPI, joint convexity, monotonicity), Rényi divergence, variational characterizations | KLD ≥ 0, joint convexity, monotonicity, variational char. of MI |
| W04 | Source coding: Kraft, Shannon code, Huffman, McMillan, Shannon radius/center | Kraft, L ≥ H, McMillan |
| W05 | Shannon-Fano-Elias, competitive optimality, coin flip generation, fixed length coding converse | Huffman optimality, fixed length converse, strong converse |
| W06 | Fixed length source coding (s4-8 HARİÇ: error exponents), randomized achievability, Slepian-Wolf | Slepian-Wolf achievability + converse |
| W07 | Channel coding setup, DMC, Shannon capacity/radius, symmetric channels, channel coding theorem achievability | Achievability (random coding + typicality) |
| W08 | Weak converse (Fano), strong converse (Chebyshev), feedback channels | Weak converse, strong converse, feedback versions |
| W09 | Source-channel separation theorem | Achievability + converse + strong converse |
| W10 | Differential entropy (Ch 8): CDF review, h(X) tanımı, uniform/exp/Gaussian örnekleri, AEP for continuous r.v., h(X) vs H(X), multivariate normal, Hadamard, MI for continuous | Concavity of h, conditioning reduces h, AEP for continuous, multivariate normal entropy, Hadamard's inequality |
| W11 | 28 Nisan Pazartesi dersi (bekleniyor) | Slayt gelince eklenecek |

---

## Zaman Planı (24 NİSAN BAŞLANGIÇLI)

**Bugün:** 24 Nisan | **Sınav:** 9 Mayıs | **Kalan:** 15 gün

Önceki planda 20 Nisan'da başlayacaktın, 4 gün kaybedildi. Plan şenliğe göre ayarlı: **5 Mayıs'a kadar ana çalışma bitecek.**

### Etkin Çalışma Süresi

- **24 Nisan - 5 Mayıs:** Ana çalışma = 12 gün
- **6-8 Mayıs:** Şenlik + hafif tekrar
- **9 Mayıs:** Sınav

### Kompakt Takvim

| Tarih | Gün | Aktivite | Saat |
|-------|-----|----------|------|
| 24 Nisan Per | Bugün | **BAŞLA:** W01 + Kitap Ch 2.1-2.7 (entropy, MI, Jensen, chain rules) | 3 |
| 25 Nisan Cum | | W02 + Kitap Ch 2.8-2.10, Ch 3 (Fano, DPI, AEP) | 3 |
| 26 Nisan Cts | | W03 (KL divergence full) + kitap Ch 2 tekrar | 3 |
| 27 Nisan Paz | | W04 + W05 + Kitap Ch 5.1-5.9 (source coding) | 4 |
| 28 Nisan Pzt | W11 dersi | W06 (s4-8 hariç) + Slepian-Wolf + Kitap Ch 15.4. **W11 slaytını al.** | 4 |
| 29 Nisan Sal | | W07 + Kitap Ch 7.1-7.7 (channel coding, capacity, achievability) | 4 |
| 30 Nisan Çar | Make-up ders | W08 (converse + feedback). **10:30 make-up dersine git** (error exponents) | 3 |
| 1 Mayıs Per | | W09 (source-channel separation) + W10 yarısı (differential entropy giriş) | 3 |
| 2 Mayıs Cum | | W10 tam bitir (differential entropy, multivariate normal, MI for continuous) + W11 | 4 |
| 3 Mayıs Cts | | **Cheat sheet sayfa 1-2** + HW1-2 tekrar | 5 |
| 4 Mayıs Paz | | **Cheat sheet sayfa 3-4** + HW3-4 tekrar | 5 |
| 5 Mayıs Pzt | | **Cheat sheet sayfa 5** (ispat iskeletleri) + son tekrar. Plan bitti. | 4 |
| 6 May Sal | Şenlik | Sabah 1 saat cheat sheet review, akşam şenlik | 1 |
| 7 May Çar | Şenlik | Sabah 1 saat cheat sheet review, akşam şenlik | 1 |
| 8 May Per | Şenlik | Sabah 1 saat review, akşam şenlik ama erken dön | 1 |
| 9 Mayıs Cum | **SINAV** | 11:00-14:00 EA209 | - |

**Ana çalışma (24 Nis - 5 May): ~45 saat**
**Şenlik dönemi (6-8 May): ~3 saat**
**Toplam: ~48 saat**

### Gerçekçi Değerlendirme

Önceki plan 47 saatle rahattı. Bu plan 48 saat ama **daha sıkıştırılmış** (12 günde tüm ana iş). Günlük ortalama 3.5-4 saat. Olimpiyatçı altyapınla bu sürdürülebilir ama:

- ⚠️ **27 Nisan Pazar günü 4 saat** kritik — source coding bitirmek lazım
- ⚠️ **2 Mayıs Cuma 4 saat** kritik — differential entropy hem tanımları hem W11'i toparla
- ⚠️ **3-5 Mayıs** cheat sheet günleri 5 saat — bu çok ama cheat sheet hazırlarken zaten tekrar yapmış oluyorsun

Eğer bir gün bir şey çıkar da çalışamazsan, ertesi güne öteleme — **aynı gün gece telafi et**. 12 günlük plan tampon bırakmıyor.

---

## Cheat Sheet Stratejisi (5 çift taraflı sayfa = 10 yüzey)

Differential entropy (W10) eklenmesiyle düzenleme yapıldı:

| Sayfa | İçerik |
|-------|--------|
| 1 | Tüm temel tanımlar: H, H(X\|Y), I(X;Y), D(p\|\|q), H_α, D_α, typical set, jointly typical set. Tanımlar arası ilişkiler (Venn diyagramı). |
| 2 | Temel araçlar: Jensen, log-sum, Fano, DPI, KLD ≥ 0 / chain rule / convexity, conditioning reduces entropy, tüm chain rule formülleri |
| 3 | Source coding: Kraft, McMillan, Shannon code bounds, Huffman, fixed-length achievability/converse, Slepian-Wolf rate region |
| 4 | Channel coding + Differential entropy: Capacity tanımı, symmetric/Gallager-symmetric capacity formülleri, BSC/BEC/noisy typewriter örnekleri, channel coding theorem key steps. **h(X) tanımı, uniform/exp/Gaussian için h değerleri, multivariate normal h = (1/2)log((2πe)^n det(K))** |
| 5 | Kritik ispatların iskeletleri: Achievability (random coding + typicality), weak converse (Fano → bound), strong converse (Chebyshev trick), source-channel separation, **AEP for continuous, Hadamard's inequality** |

---

## Faz 1: Temeller (24-26 Nisan, 3 gün)

### Hedef

Notasyona hakim olmak. H(X), H(X|Y), I(X;Y), D(p||q), p_{Y|X}, p_{X_iota} gibi semboller görünce otomatik anlamak. 7 çekirdek aracın her birinin ne işe yaradığını bilmek.

### Günlük Plan

- **24 Nisan (Per) — 3 saat:** Kitap Ch 2.1-2.7 (entropy, MI, Jensen, chain rules). W01 tüm.
- **25 Nisan (Cum) — 3 saat:** Kitap Ch 2.8-2.10 + Ch 3 (DPI, sufficient stats, Fano, AEP). W02 tüm.
- **26 Nisan (Cts) — 3 saat:** W03 tüm (KL divergence derinlemesine). Ch 2 kritik yerleri tekrar.

### Kontrol Soruları

- H, H(X|Y), I(X;Y), D(p||q) tanımlarını yazabiliyor musun?
- I(X;Y) = H(X) - H(X|Y) = H(Y) - H(Y|X) neden ikisi de?
- Jensen eşitsizliği nasıl uygulanır? Hangi function convex, hangi concave?
- KLD neden non-negatif? İspatı?
- AEP ne diyor? Typical set tanımı?
- Fano's inequality ifadesi?

---

## Faz 2: Source Coding (27-28 Nisan, 2 gün)

### Hedef

Source coding'in tüm araçlarına hakim olmak. Slepian-Wolf'un achievability + converse ispatlarını anlamak.

### Günlük Plan

- **27 Nisan (Paz) — 4 saat:** Kitap Ch 5.1-5.9. W04 + W05 tüm (codes, Kraft, Shannon code, Huffman, Shannon-Fano-Elias, fixed length coding).
- **28 Nisan (Pzt) — 4 saat:** W06 (s4-8 HARİÇ). Slepian-Wolf full ispat. Kitap Ch 15.4. **W11 slaytını dizine al** (dersin sonra).

### Kontrol Soruları

- Kraft inequality ifadesi + ispat fikri?
- Huffman code neden optimal?
- Fixed length source coding converse Fano ile nasıl?
- Slepian-Wolf rate region?
- Achievability'de typicality counting nasıl işliyor?

---

## Faz 3: Channel Coding (29-30 Nisan, 2 gün)

### Hedef

Dersin ağırlık merkezi. Capacity, coding theorem, achievability, weak/strong converse, feedback.

### Günlük Plan

- **29 Nisan (Sal) — 4 saat:** Kitap Ch 7.1-7.7. W07 tüm (DMC, capacity, symmetric channels, achievability proof).
- **30 Nisan (Çar) — 3 saat + make-up dersi:** W08 tüm (weak + strong converse + feedback). **10:30 make-up dersine git** (error exponents - sınavda yok ama dinle).

### Kontrol Soruları

- Shannon capacity tanımı, Shannon center nedir?
- Channel coding theorem achievability nasıl? (Random coding + typicality + Markov existence)
- Weak converse nasıl? (Fano → I ≤ nC → Pe ≥ (R-C)/R)
- Strong converse? (Chebyshev trick)
- Feedback capacity artırıyor mu?
- BSC, BEC, noisy typewriter capacity formülleri?

---

## Faz 4: Joint Source-Channel + Differential Entropy (1-2 Mayıs, 2 gün)

### Hedef

W09 (source-channel separation) ve W10 (differential entropy) konularını bitirmek. Bu faz çok önemli çünkü W10 sonradan girdi ve çoğu öğrenci buraya yeterince çalışmamış olacak — **senin avantajın olabilir**.

### Günlük Plan

- **1 Mayıs (Per) — 3 saat:** W09 tüm (source-channel separation: achievability + converse + strong converse). W10 s1-10 (CDF review, h(X) tanımı, examples, AEP for continuous).
- **2 Mayıs (Cum) — 4 saat:** W10 s11-18 tamamla (multivariate normal, Hadamard, MI for continuous). W11 slaytını bitir. HW4 sorularını tekrar çöz.

### Kontrol Soruları

- Source-channel separation theorem ifadesi, hangi koşullarla?
- Differential entropy h(X) ile H(X) arasında ne fark?
- h(X) negatif olabilir mi? Hangi örneklerde?
- Gaussian için h(X) formülü? Uniform için?
- Multivariate normal'ın differential entropy'si?
- Hadamard's inequality?
- I(X;Y) continuous r.v. için nasıl tanımlı?

---

## Faz 5: Cheat Sheet + Pratik (3-5 Mayıs, 3 gün)

### Hedef

Cheat sheet'i finalize et. HW'leri tekrar gez. Eksik yerleri kapat. Bu günler **tekrar + pekiştirme**, yeni öğrenme değil.

### Günlük Plan

- **3 Mayıs (Cts) — 5 saat:** Cheat sheet sayfa 1-2 (tanımlar + temel araçlar). HW1-2 sorularını hızlıca gez.
- **4 Mayıs (Paz) — 5 saat:** Cheat sheet sayfa 3-4 (source/channel coding + differential entropy). HW3-4 sorularını gez.
- **5 Mayıs (Pzt) — 4 saat:** Cheat sheet sayfa 5 (ispat iskeletleri). Slaytlardaki H.W. işaretli soruları çöz. Son tekrar.

### 5 Mayıs akşamı hazır olmalısın

Çalışma bitti demek. Şenliğe gönül rahatlığıyla giriyorsun.

---

## Faz 6: Şenlik + Final Review (6-8 Mayıs)

- **6-8 Mayıs sabahları (1 saat):** Kahvaltı sırasında cheat sheet'e göz at, güvenini tazele.
- **6-8 Mayıs akşamları:** Şenlik. Rahat ol.
- **8 Mayıs akşamı:** Erken dön, cheat sheet yanında, erken yat.

---

## Sınav Günü (9 Mayıs)

- 10:00: Kalk, hafif kahvaltı
- 10:30: EA209'a doğru yola çık
- 10:50: Sınıfta ol
- 11:00-14:00: Sınav
- Sonrası: Çözümleri ODTÜClass'a yükle

---

## Önemli Kavramlar Listesi

### Temel Ölçüler
- H(X), H(X|Y), H(X,Y): entropy
- I(X;Y), I(X;Y|Z): mutual information
- D(p||q): KL divergence
- H_alpha, D_alpha: Rényi versiyonları

### Eşitsizlikler
- Jensen: f(E[X]) ≤ E[f(X)] for convex f
- Log-sum inequality
- Fano: H(X|Y) ≤ h(P_e) + P_e log(|X|-1)
- KLD ≥ 0

### Chain Rules
- H(X,Y) = H(X) + H(Y|X)
- I(X,Y;Z) = I(X;Z) + I(Y;Z|X)
- D(p_{X,Y}||q_{X,Y}) = D(p_X||q_X) + D(p_{Y|X}||q_{Y|X} | p_X)

### AEP ve Typical Sets
- AEP: -(1/n) log p(X_1^n) → H(X)
- A_epsilon^(n): typical set
- |A_epsilon^(n)| ≈ 2^(nH(X))

### Source Coding
- Kraft: sum D^(-l_i) ≤ 1
- Shannon code: l(x) = ceil(log 1/p(x))
- Huffman code: optimal prefix code
- Slepian-Wolf rate region: R_1 ≥ H(X|Y), R_2 ≥ H(Y|X), R_1+R_2 ≥ H(X,Y)

### Channel Coding
- Shannon capacity: C = sup_{p_X} I(X;Y)
- BSC capacity: 1 - h(p)
- BEC capacity: 1-alpha
- Channel coding theorem: R < C achievable, R > C not
- Feedback capacity = capacity (for memoryless)

### Differential Entropy (YENİ - W10)
- h(X) = integral f_X(x) log(1/f_X(x)) dx (continuous analog of H)
- h(X) negatif olabilir, sonsuz olabilir, tanımsız olabilir
- Uniform on [0, l]: h = log l
- Exponential with rate lambda: h = log(e/lambda)
- Gaussian N(mu, sigma^2): h = (1/2) log(2 pi e sigma^2)
- Multivariate normal N(mu, K): h = (1/2) log((2 pi e)^n det(K))
- AEP for continuous: (1/n) log(1/f(X_1^n)) → h(X)
- Hadamard: det(K) ≤ prod K_{i,i} for positive definite K
- Chain rule for h: h(X,Y) = h(X|Y) + h(Y) = h(X) + h(Y|X)
- Independence bound: h(X_1^n) ≤ sum h(X_i)
- h(X|Y) ≤ h(X) (conditioning reduces h, eşitlik iff independent)
- I(X;Y) = h(X) - h(X|Y) = h(Y) - h(Y|X) (aynı yapı)
- If Y = aX + b: h(Y) = h(X) + log|a|

---

## Hedefler

- Minimum: BB (standart çalışma, cheat sheet)
- Gerçekçi: BA-AA (bu plana uyarsan)
- Stretch: AA (+bonus soru çözebilirsen)

Olimpiyat geçmişi (JBMO silver + 2 Türkiye ulusal bronz + JNO silver) matematiksel altyapı bakımından avantaj. Ama bu ders olimpiyat matematiği değil, analiz matematiği. Farklı kas, çalışmayı gerektirir.

---

## Notlar

- Cheat sheet için 10 yüzey çok cömert. İyi kullanılırsa ciddi avantaj.
- Hoca ispat-ağırlıklı soruyor. "Show that", "Prove that" formatında soru bekle.
- Slaytlardaki H.W. işaretli sorular sınav adayı.
- Her strong converse ispatı aynı Chebyshev trick'i kullanıyor - bir kere öğren, yeter.
- Her weak converse Fano + chain rule + conditioning reduces entropy pattern'ında - bir kere öğren, yeter.
- Her achievability random coding + typicality counting + Markov existence - bir kere öğren, yeter.

---

## Dizin Yapısı

```
EE533/
├── README.md                                    (bu dosya)
├── Elements of Information Theory - 2005 - Cover.pdf  (kitap, 2. baskı)
├── assignment1/
├── assignment2/
├── assignment3/
├── assignment4/
│   ├── Assignment04.pdf
│   ├── p1.png - p5.png  (soruların screenshot'ları)
└── lecture-notes/
    ├── 533slidesW01.pdf - 533slidesW09.pdf
    └── (W10 yakında)
```
