# Skill: Konu Araştırması (Topic Research)

## Purpose
Bu hafta LinkedIn'de en çok gösterim ve reaksiyon alma potansiyeli olan makale konusunu bulmak ve puanlı aday listesiyle insana sunmak.

## Serves Goals
- Görünürlüğü artırmak (gösterim >2.000) — güncel ve aranan konular algoritmada daha geniş dağıtım alır
- Etkileşim almak (reaksiyon >100) — kitlenin gerçek sorununa dokunan, görüş bildirmeye davet eden konular

## Inputs
- `knowledge/AUDIENCE.md` — hedef kitlenin sorunları ve dili
- `knowledge/STRATEGY.md` — güncel öncelikler
- `MEMORY.md` — hangi konu sütunu / açı daha önce işe yaradı
- `data/imports/linkedin-stats.csv` — geçmiş makale performansı
- `data/imports/` — insanın bıraktığı notlar, saha hikayeleri
- `journal/` — son sinyaller
- Web araştırması

## Konu Sütunları
1. Dijital dönüşüm
2. Teknoloji
3. Yapay zeka
4. Üretim yönetimi
5. Verimlilik
6. Maliyet azaltma

En güçlü konular genellikle iki sütunun kesişimindedir (ör. "Yapay zeka ile üretimde fire maliyetini düşürmek"). Bu bir hipotezdir; doğrulanana kadar MEMORY.md'ye yazılmaz.

## Process
1. Context oku: AUDIENCE, STRATEGY, MEMORY, son journal girdileri, geçmiş performans.
2. Son 3 makalenin konu sütunlarını listele; aynı sütunu 2 haftadan fazla üst üste önerme.
3. Web'de son 7–14 günün gelişmelerini tara:
   - Sektör haberleri (yeni AI modelleri/araçları, Endüstri 4.0, regülasyonlar, enerji/hammadde maliyetleri)
   - Güvenilir raporlar (McKinsey, BCG, Deloitte, Gartner, WEF, OECD, TÜİK, sektör dernekleri)
   - LinkedIn'de ve sektör medyasında tartışılan başlıklar
   - Türkiye'deki üretim ve KOBİ gündemi
4. 5–7 aday konu oluştur. Her biri için: çalışma başlığı, tek cümlelik ana fikir, konu sütun(lar)ı, hedef kitle segmenti, dayanak veri/kaynak.
5. Her adayı 1–10 arası puanla:
   - **Güncellik:** Şu an konuşuluyor mu? Yeni bir gelişmeye dayanıyor mu?
   - **Kitle acısı:** Hedef kitlenin somut bir sorununa (maliyet, verim, kaynak, risk) dokunuyor mu?
   - **Tartışma potansiyeli:** Okuru yorum yazmaya/görüş bildirmeye davet ediyor mu? Net bir duruş var mı?
   - **Özgünlük:** Kişisel deneyim, saha gözlemi veya sıra dışı bir açı eklenebilir mi?
   - **Kanıt:** Güçlü, kaynaklı bir veri/istatistikle desteklenebilir mi?
   - **Geçmiş performans:** MEMORY.md ve CSV'ye göre bu sütun/açı nasıl performans gösterdi? (veri yoksa 5)
6. Toplam puana göre sırala. Puanlar eşitse kitle acısı yüksek olan önde.
7. İlk 3 konu için: 2 alternatif hook (ilk 2 satır), önerilen format (vaka / liste / karşıt görüş / veri hikayesi / adım adım rehber), insandan istenecek kişisel katkı.
8. Önerilen konuyu ve gerekçesini net yaz: "Neden bu, neden şimdi, neden biz?"

## Outputs
- `outputs/YYYY-MM-DD_linkedin-paylasim_konu-arastirmasi.md` — puan tablosu, ilk 3 konunun detayı, önerilen konu, kaynak linkleri

## Quality Bar
- Her aday konunun en az 1 güvenilir, tarihli kaynağı var (link ile).
- En az 1 aday "karşıt görüş / yaygın inanışa itiraz" açısında.
- En az 1 aday Türkiye üretim/KOBİ bağlamına özgü.
- En az 1 aday "kanıtlanmış format remiksi" (MEMORY.md'de işe yarayan bir şeyin yeni açıyla tekrarı) — MEMORY boşsa atlanabilir.
- Hiçbir konu genel/klişe değil ("AI geleceği değiştirecek" gibi başlıklar reddedilir).

## Tools
- Web araması ve web sayfası okuma
- `data/imports/linkedin-stats.csv`

## Integration
- Önerilen konu ARTICLE_WRITING skill'ine girdi olur.
- PERFORMANCE_REVIEW'den gelen bulgular puanlamadaki "Geçmiş performans" kriterini besler.
- Dikkat çekici trendler journal'a yazılır.
