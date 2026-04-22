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

## Ders Kapsamı (Hocanın Syllabus'una Göre)

| Hafta | Konu | Kitap |
|-------|------|-------|
| 1-2 | Measures of information | Ch. 2 |
| 3 | Asymptotic Equipartition Property (AEP) | Ch. 3 |
| 4-6 | Source Coding | Ch. 5 |
| 7-11 | Channel Coding and Capacity | Ch. 7 |
| 12 | Differential Entropy (sınavda yok) | Ch. 8 |
| 13-14 | Gaussian Channel (sınavda yok) | Ch. 9 |
| 16 | Rate-Distortion Theory (sınavda yok) | Ch. 10 |

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
| W10 | 24 Nisan'da açılacak | Henüz yok |

---

## Zaman Planı

**Bugün:** 20 Nisan | **Sınav:** 9 Mayıs | **Kalan:** 19 gün

### Şenlik Notu

6-9 Mayıs METU Şenliği. Planı şenliğe göre ayarlıyoruz: tüm ana çalışma 5 Mayıs'a kadar bitecek, şenliğe gönül rahatlığıyla gideceğiz.

### Takvim

| Tarih | Aktivite | Saat/gün |
|-------|----------|----------|
| 20-24 Nisan | Temeller: notasyon + W01-W03 + kitap Ch 2-3 | 1.5-2 saat |
| 24 Nisan | W10 slaytını dizine ekle, kapsamı güncelle | - |
| 25-27 Nisan (hafta sonu) | Source coding: W04-W06 + kitap Ch 5 + Slepian-Wolf | 3-4 saat |
| 28 Nisan - 2 Mayıs | Channel coding: W07-W09 + kitap Ch 7 (EN AĞIR BLOK) | 2-3 saat |
| 30 Nisan | Son ders (error exponents - sınavda yok ama dinle) | - |
| 3-5 Mayıs | Cheat sheet hazırlama + HW1-4 tekrarı + eksikler | 4-5 saat |
| 6-8 Mayıs | Şenlik. Sabah 1 saat cheat sheet review, akşam şenlik | 1 saat |
| 8 Mayıs akşamı | Erken dön, erken yat | - |
| 9 Mayıs 11:00 | Sınav | - |

**Toplam planlanmış çalışma: ~47 saat.** İhtiyaç ~26-30 saat, fazlası tampon.

---

## Cheat Sheet Stratejisi (5 çift taraflı sayfa = 10 yüzey)

| Sayfa | İçerik |
|-------|--------|
| 1 | Tüm temel tanımlar: H, H(X\|Y), I(X;Y), D(p\|\|q), H_α, D_α, typical set, jointly typical set. Tanımlar arası ilişkiler (Venn diyagramı). |
| 2 | Temel araçlar: Jensen, log-sum, Fano, DPI, KLD ≥ 0 / chain rule / convexity, conditioning reduces entropy, tüm chain rule formülleri |
| 3 | Source coding: Kraft, McMillan, Shannon code bounds, Huffman, fixed-length achievability/converse, Slepian-Wolf rate region |
| 4 | Channel coding: Capacity tanımı, symmetric/Gallager-symmetric capacity formülleri, BSC/BEC/noisy typewriter örnekleri, channel coding theorem key steps |
| 5 | Kritik ispatların iskeletleri: Achievability (random coding + typicality), weak converse (Fano → bound), strong converse (Chebyshev trick), source-channel separation |

---

## Faz 1: Temelleri Kurmak (20-24 Nisan)

### Hedef

Notasyona hakim olmak. Artık H(X), H(X|Y), I(X;Y), D(p||q), p_{Y|X}, p_{X_iota} gibi semboller görünce otomatik anlamak.

### Günlük Plan

- **20 Nisan:** Kitap Ch 2.1-2.4 oku (entropy tanımları). W01 s15-26 paralel oku.
- **21 Nisan:** Kitap Ch 2.5-2.7 (chain rules, Jensen, log-sum). W01'in geri kalanı.
- **22 Nisan:** Kitap Ch 2.8-2.10 (DPI, sufficient stats, Fano). W02 s1-7.
- **23 Nisan:** Kitap Ch 3 (AEP). W02 s18-24 (AEP, typical sets).
- **24 Nisan:** W03 tüm (KL divergence derinlemesine). W10 slaytı geldi mi bak.

### Kontrol Soruları (Faz 1 sonunda cevaplayabilmen lazım)

- H(X), H(X|Y), I(X;Y), D(p||q) tanımlarını hatırlayabiliyor musun?
- I(X;Y) = H(X) - H(X|Y) = H(Y) - H(Y|X) neden?
- Jensen eşitsizliğini ne zaman uygulanır?
- KLD neden non-negatif? İspatı?
- AEP ne diyor?

---

## Faz 2: Source Coding (25-27 Nisan)

### Hedef

Source coding'in tüm araçlarına hakim olmak. Slepian-Wolf'un hem achievability hem converse ispatını anlamak.

### Günlük Plan

- **25 Nisan:** Kitap Ch 5.1-5.5. W04 tüm (codes, Kraft, Shannon code).
- **26 Nisan:** Kitap Ch 5.6-5.9. W05 tüm (Huffman, Shannon-Fano-Elias, fixed length coding).
- **27 Nisan:** W06 (error exponents HARİÇ s4-8). Slepian-Wolf full ispat. Kitap Ch 15.4.

### Kontrol Soruları

- Kraft inequality nedir, ispatı?
- Huffman code neden optimal?
- Fixed length source coding converse (Fano ile) nasıl ispatlanıyor?
- Slepian-Wolf rate region?
- Slepian-Wolf achievability'de typicality counting nerede kullanılıyor?

---

## Faz 3: Channel Coding (28 Nisan - 2 Mayıs)

### Hedef

Dersin ağırlık merkezi. Channel capacity, coding theorem, achievability, weak/strong converse, feedback, source-channel separation.

### Günlük Plan

- **28 Nisan:** Kitap Ch 7.1-7.5. W07 s1-12 (DMC, capacity, symmetric channels).
- **29 Nisan:** Kitap Ch 7.6-7.7. W07 s13-19 (achievability proof).
- **30 Nisan:** W08 s1-7 (weak + strong converse). Ders akşamı: error exponents (sınavda yok).
- **1 Mayıs:** W08 s8-13 (feedback).
- **2 Mayıs:** W09 (source-channel separation). W10 varsa oku. HW4 sorularını çöz.

### Kontrol Soruları

- Shannon capacity tanımı, Shannon center nedir?
- Channel coding theorem achievability nasıl kanıtlanıyor? (Random coding + typicality + Markov existence)
- Weak converse nasıl? (Fano → I ≤ nC → Pe ≥ (R-C)/R)
- Strong converse? (Chebyshev trick)
- Feedback capacity'yi artırıyor mu?
- BSC, BEC kapasiteleri ezber hazır mı?

---

## Faz 4: Cheat Sheet + Pratik (3-5 Mayıs)

### Hedef

Cheat sheet'i finalize et. HW'leri tekrar gez. Eksik yerleri kapat.

### Günlük Plan

- **3 Mayıs:** Cheat sheet sayfa 1-2 (tanımlar + araçlar). HW1-2 sorularını hızlıca gez.
- **4 Mayıs:** Cheat sheet sayfa 3-4 (source + channel coding). HW3-4 sorularını gez.
- **5 Mayıs:** Cheat sheet sayfa 5 (ispat iskeletleri). Slaytlardaki H.W. işaretli soruları çöz. Son tekrar.

---

## Faz 5: Şenlik + Final Review (6-8 Mayıs)

- 6-8 Mayıs sabahları: 1 saat cheat sheet'e göz at, güvenini tazele.
- 6-8 Mayıs akşamları: Şenlik.
- 8 Mayıs akşamı: Erken dön, cheat sheet'i yanına al, erken yat.

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
