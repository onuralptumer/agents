# Skill: Performans Analizi

## Purpose
Blogun haftalık okunma ve yorum verisini hedeflerle karşılaştırmak ve yazı türü, açılış, başlık ve görsel yaklaşımı seçimini iyileştirecek örüntüleri çıkarmak.

## Serves Goals
- Okunma (>500/hafta)
- Etkileşim (>10 yorum/hafta)

## Inputs
- `data/imports/blog-stats.csv` — haftalık ve yazı bazında veriler (format: `data/imports/HOW_TO_EXPORT.md`)
- `outputs/*-tr.md`, `outputs/*-en.md`, `outputs/*-gorsel-plani.md` — yayınlanan yazıların özellikleri
- `MEMORY.md`

## Process
1. CSV'den son haftanın satırlarını oku. Blog toplamını hesapla: toplam okunma, toplam yorum (TR + EN).
2. Hedeflerle karşılaştır: okunma >500, yorum >10. Durum: ✅ ikisi de / ⚠️ biri / ❌ hiçbiri.
3. Yazı bazında kır: hangi yazı, hangi dil, kaç okunma, kaç yorum, ortalama okuma süresi.
4. Yazıları etiketle: yazı türü (`plan.md` §6), açılış yöntemi (`stil.md` §5), başlık mantığı (`plan.md` §7), uzunluk, görsel sayısı, dil.
5. Geçmiş haftalarla karşılaştır: hedef üstü yazılarda hangi etiketler tekrar ediyor? TR ve EN performansı nasıl ayrışıyor?
6. Yorumlarda tekrar eden okur sorularını not et (veri girildiyse) — bunlar gelecek yazıların "okur sorusu" girdisidir.
7. 3+ tutarlı veri noktasıyla doğrulanan örüntüyü MEMORY.md'ye kanıtıyla yaz; zayıf sinyali "Patterns Noticed"a.
8. Escalation kurallarını kontrol et.

## Outputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_haftalik-rapor.md` — skor tablosu, yazı bazında kırılım, wins/misses, öneriler
- `MEMORY.md` güncellemeleri
- Journal'a haftalık özet

## Quality Bar
- Her sonuç gerçek veriye dayanıyor; veri yoksa "veri yok" yazılıyor.
- Tek veri noktasından MEMORY.md'ye kural yazılmıyor.
- Öneriler `guides/` kurallarıyla çelişmiyor (ör. yorum için yapay çağrı önerilmiyor); çelişen bir bulgu varsa rehber değişikliği olarak insana öneriliyor.

## Tools
- `data/imports/blog-stats.csv`

## Integration
- Bulgular BLOG_WRITING_TR'nin yazı türü, açılış ve başlık seçimlerini; IMAGE_PLANNING'in görsel sayısı ve estetik seçimini besler.
