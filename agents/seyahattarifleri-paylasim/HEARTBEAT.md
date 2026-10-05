# Seyahat Tarifleri Paylaşım Agent Heartbeat

## Schedule
- **Tetikleyici (asıl döngü):** `data/imports/notlar/` klasörüne yeni bir not dosyası eklendiğinde ya da insan "yeni yazı" dediğinde.
- **Haftalık:** Her pazartesi sabahı — performans analizi ve bekleyen not kontrolü.

## Each Cycle

### 1. Read Context
- `journal/entries/` altındaki son girdiler (insan kararları, onaylar, düzeltmeler)
- `knowledge/STRATEGY.md` — öncelik değişikliği var mı?
- Kendi `MEMORY.md`
- `data/imports/notlar/` — işlenmemiş not seti var mı?
- `data/imports/blog-stats.csv` — analiz edilmemiş hafta var mı?

### 2. Assess State
- İşlenmemiş not seti var mı? (bir not setinin `outputs/` altında `-tr.md` dosyası yoksa işlenmemiştir)
- TR yazı hazır ama EN yazı veya görsel planı eksik mi?
- İnsandan onay veya düzeltme bekleyen paket var mı?
- Analiz edilmemiş performans verisi var mı?

### 3. Execute Skill
Karar ağacı (sırayla):
1. Pazartesi ve analiz edilmemiş hafta var mı? → **PERFORMANCE_REVIEW**
2. İşlenmemiş not seti var mı? → **BLOG_WRITING_TR** → **TRANSLATION_EN** → **IMAGE_PLANNING** (tek paket olarak zincir halinde)
3. Eksik paket parçası var mı? → yalnızca eksik skill'i çalıştır
4. İnsan bir yazıda düzeltme istedi mi? → ilgili TR yazıyı `-v2` olarak revize et, ardından EN yazı ve görsel planı yerleşimlerini güncelle
5. Hepsi tamam mı? → İnsana bekleyen onayları hatırlat; yeni içerik üretme (notsuz yazı yazılmaz)

Not: Bir not seti TR → EN → görsel planı zinciriyle tek döngüde işlenir; bu "tek skill / döngü" kuralının istisnasıdır, çünkü paket yalnızca üçü birlikte yayına hazırdır.

### 4. Log to Journal
`journal/entries/YYYY-MM-DD_HHMM.md` (`templates/JOURNAL_ENTRY.md` formatıyla):
- İşlenen not seti ve üretilen dosyalar
- Yazının ana fikri ve türü
- Doğrulanamayan bilgiler / insandan beklenen netleştirmeler
- Sonraki adım

## Weekly Review

### 1. Gather Data
`data/imports/blog-stats.csv` dosyasından geçen haftanın satırları.

### 2. Score Against Targets

| Metric | Target | This Week | Status |
|--------|--------|-----------|--------|
| Blog toplam okunma (TR + EN) | >500 | | |
| Blog toplam yorum (TR + EN) | >10 | | |
| Teslim edilen not seti / hazırlanan paket | 1:1 | | |
| TR okunma / EN okunma (takip) | — | | |

### 3. Analyze Wins and Misses
- **Wins:** Hangi yazı türü, açılış, başlık, görsel yaklaşımı ve dil iyi çalıştı?
- **Misses:** Hangi yazı beklentinin altında kaldı? Hipotezi yaz.

### 4. Update Memory
3+ veri noktasıyla doğrulanan örüntüleri MEMORY.md'ye ekle.

### 5. Log Weekly Summary to Journal
- İncelenen yazı sayısı, hedeflere göre performans, en önemli içgörü, gelecek hafta için öneri.

## Monthly Review
- Son 4 haftanın trendi (okunma, yorum, TR/EN dağılımı)
- Yazı türlerinin performans sıralaması
- Hedeflerin ayarlanması gerekiyorsa insana öner

## Escalation Rules
- Okunma veya yorum 2+ hafta üst üste hedefin altında
- 2 hafta üst üste yeni not seti gelmedi (KPI'ları besleyecek içerik yok)
- 2 hafta üst üste performans verisi girilmedi
- Notlarda yazının doğruluğunu belirleyen kritik bir eksik veya çelişki var
- Bir mekânın kapanmış olması gibi, rota önerisini değiştiren güncel bir bilgi bulundu
- Performans bulguları bir rehber kuralıyla çelişiyor (rehberi agent değiştirmez, insana önerir)

## Rules
- Harekete geçmeden önce journal'ı oku
- Notsuz yazı yazma; deneyim uydurma
- Emin değilsen doğrula; doğrulayamıyorsan editör notuna yaz
- AGENT.md'deki bir hedefe hizmet etmeyen skill'i çalıştırma
