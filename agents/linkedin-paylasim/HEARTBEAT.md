# LinkedIn Paylaşım Agent Heartbeat

## Schedule
Haftalık döngü, her pazartesi sabahı.
- **Pazartesi:** Haftalık performans analizi → konu araştırması → makale taslağı → insan onayına sunum.
- **Salı–Perşembe:** İnsan makaleyi onaylar ve yayınlar (önerilen saat aralığı insan tarafından belirlenir; veri biriktikçe MEMORY.md'den öğrenilir).
- **Yayından 7 gün sonra:** İnsan LinkedIn istatistiklerini `data/imports/linkedin-stats.csv` dosyasına ekler.

## Each Cycle

### 1. Read Context
- `journal/entries/` altındaki son girdileri kontrol et (sinyaller, kararlar, insan notları)
- `knowledge/STRATEGY.md` — öncelik değişikliği var mı?
- `knowledge/AUDIENCE.md` ve `knowledge/BRAND.md` — kitle ve ses tonu
- Kendi `MEMORY.md` — hangi konu/hook/format işe yaradı, hangisi yaramadı
- `data/imports/` — yeni performans verisi veya insan notu var mı?

### 2. Assess State
- `data/imports/linkedin-stats.csv` içinde henüz analiz edilmemiş satır var mı?
- Bu hafta için onaylanmış bir konu var mı?
- Bu hafta için yayına hazır makale var mı?
- Son yayınlanan makale hangi konu sütunundaydı? (aynı sütunu art arda tekrarlama)

### 3. Execute Skill
Karar ağacı (sırayla):
1. Analiz edilmemiş performans verisi var mı? → **PERFORMANCE_REVIEW** (önce bu)
2. Bu hafta için konu araştırması yok mu? → **TOPIC_RESEARCH**
3. Konu var ama makale yok mu? → **ARTICLE_WRITING** (en yüksek puanlı konu ile)
4. Makale hazır ve onay bekliyor mu? → İnsana hatırlat, yeni bir şey üretme.
5. Hepsi tamam mı? → Gelecek hafta için yedek konu listesini güncelle (TOPIC_RESEARCH, hafif mod).

Not: Haftalık döngüde PERFORMANCE_REVIEW → TOPIC_RESEARCH → ARTICLE_WRITING zincir halinde çalışabilir; bu bir hafta = bir makale hedefine hizmet ettiği için kural istisnasıdır.

### 4. Log to Journal
`journal/entries/YYYY-MM-DD_HHMM.md` dosyasına (`templates/JOURNAL_ENTRY.md` formatıyla):
- Bu döngüde ne yapıldı
- Seçilen konu ve neden seçildiği
- Dikkat çekici bulgular (ör. "AI + maliyet açılı başlıklar 2 kat reaksiyon aldı")
- Sonraki adım ve insandan beklenen aksiyon

## Weekly Review

### 1. Gather Data
`data/imports/linkedin-stats.csv` dosyasından son yayınlanan makalenin 7 günlük verilerini oku (format: `data/imports/HOW_TO_EXPORT.md`).

### 2. Score Against Targets

| Metric | Target | This Week | Status |
|--------|--------|-----------|--------|
| Gösterim (7 gün) | >2.000 | | |
| Reaksiyon (7 gün) | >100 | | |
| Yayına hazır makale | 1 | | |
| Yorum (7 gün, takip metriği) | — | | |
| Etkileşim oranı (reaksiyon+yorum+paylaşım / gösterim) | — | | |

### 3. Analyze Wins and Misses
- **Wins:** Ne işe yaradı? (konu sütunu, hook tipi, format, uzunluk, görsel, yayın günü/saati)
- **Misses:** Ne yaramadı? Hipotezi yaz.
- Tek veri noktası → journal'a; 3+ tutarlı veri noktası → MEMORY.md'ye.

### 4. Update Memory
Doğrulanmış örüntüleri MEMORY.md'deki ilgili bölümlere ekle.

### 5. Log Weekly Summary to Journal
- İncelenen makale sayısı
- Hedeflere göre performans
- Bu haftanın en önemli içgörüsü
- Gelecek hafta için öneriler

## Monthly Review
- Son 4 haftalık analizi karşılaştır (gösterim ve reaksiyon trendi)
- Konu sütunlarının performans sıralamasını çıkar
- Hedeflerin ayarlanması gerekiyorsa insana öner (2.000 / 100 eşikleri sürekli aşılıyorsa yükseltme önerisi)

## Escalation Rules
- Gösterim veya reaksiyon 2+ hafta üst üste hedefin altında
- Bir makale 1.000 gösterimin altında kaldı
- 2 hafta üst üste performans verisi girilmedi (agent öğrenemiyor)
- Önerilen konu hassas/riskli (şirket bilgisi, rakip adı, tartışmalı iddia)
- Makale onay bekliyor ve çarşamba sonuna kadar onaylanmadı

## Rules
- Harekete geçmeden önce her zaman journal'ı oku
- Haftada bir makale; kaliteyi sayıya feda etme
- Emin değilsen araştırma yap
- AGENT.md'deki bir hedefe hizmet etmeyen skill'i çalıştırma
