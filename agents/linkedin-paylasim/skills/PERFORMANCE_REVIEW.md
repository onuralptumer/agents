# Skill: Performans Analizi (Performance Review)

## Purpose
Yayınlanan makalelerin 7 günlük gösterim ve reaksiyon verisini hedeflerle karşılaştırmak ve konu/format seçimini iyileştirecek örüntüleri çıkarmak.

## Serves Goals
- Görünürlüğü artırmak (gösterim >2.000)
- Etkileşim almak (reaksiyon >100)

## Inputs
- `data/imports/linkedin-stats.csv` — makale bazında performans verisi (format: `data/imports/HOW_TO_EXPORT.md`)
- `outputs/*_makale.md` — yayınlanan makalenin konu, hook, format bilgisi
- `MEMORY.md` — mevcut örüntüler

## Process
1. CSV'deki henüz analiz edilmemiş satırları bul (son haftalık raporda olmayan yayın tarihleri).
2. Her makale için hesapla:
   - Gösterim vs. hedef (>2.000)
   - Reaksiyon vs. hedef (>100)
   - Etkileşim oranı = (reaksiyon + yorum + paylaşım) / gösterim
   - Durum: ✅ ikisi de hedefte / ⚠️ biri hedefte / ❌ ikisi de altında
3. Makaleyi özelliklerine göre etiketle: konu sütunu, hook tipi (veri / soru / karşıt görüş / hikaye), format, uzunluk, görsel tipi, yayın günü/saati.
4. Tüm geçmiş verilerle karşılaştır: hangi etiketler hedef üstü makalelerde tekrar ediyor?
5. Wins / Misses yaz; her miss için bir hipotez öner.
6. 3+ veri noktasıyla tutarlı örüntüleri MEMORY.md'nin ilgili bölümüne kanıtıyla ekle; daha zayıf sinyalleri "Patterns Noticed"a yaz.
7. Gelecek haftanın konu araştırması için 1–3 somut öneri çıkar.
8. Escalation kurallarını kontrol et (2+ hafta hedef altı, <1.000 gösterim, eksik veri).

## Outputs
- `outputs/YYYY-MM-DD_linkedin-paylasim_haftalik-rapor.md` — skor tablosu, wins/misses, öneriler
- `MEMORY.md` güncellemeleri
- Journal'a haftalık özet

## Quality Bar
- Her sonuç gerçek veriye dayanıyor; veri yoksa "veri yok" yazılıyor, tahmin yürütülmüyor.
- Tek veri noktasından MEMORY.md'ye kural yazılmıyor.
- Her rapor en az 1 uygulanabilir öneri içeriyor.

## Tools
- `data/imports/linkedin-stats.csv`

## Integration
- Bulgular TOPIC_RESEARCH'ün "Geçmiş performans" puanını ve ARTICLE_WRITING'in hook/format seçimini besler.
