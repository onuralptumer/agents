# Skill: Türkçe Blog Yazımı

## Purpose
Kullanıcının seyahat notlarından seyahattarifleri.com için yayına hazır, Türkçe bir blog yazısı üretmek.

## Serves Goals
- Okunma (>500/hafta) — okura hem gitme hissi hem de kendi planını kurma imkânı veren, sonuna kadar okunan yazı
- Etkileşim (>10 yorum/hafta) — görüş sahibi anlatıcı ve okurun kendi deneyimini ekleyebileceği gerçek sorular
- Yayına hazır içerik

## Inputs
- `data/imports/notlar/<not-dosyası>.md` — gerçek deneyim malzemesi
- `guides/plan.md` — ana fikir ve bölüm planı
- `guides/stil.md` — ses, hitap, mizah, doğruluk sınırları, yayın kontrolü
- `guides/editor.md` — dört geçişli editoryal düzenleme
- `MEMORY.md` — işe yarayan yazı türleri, açılışlar, başlıklar
- Web araştırması — notlardaki boşlukları doğrulanmış pratik bilgiyle tamamlamak için

## Process
1. Notları oku. Konu, tarih/süre, kimlerle seyahat edildiği, mutlaka yer alacaklar ve kaçınılacaklar net mi kontrol et. Yalnızca anlatının doğruluğunu belirleyen eksik varsa insana sor; diğer durumlarda ilerle (`plan.md` §3, §11).
2. Malzemeyi ayır: gerçek deneyim / doğrulanmış dış bilgi / editoryal öneri / eksik (`stil.md` §4). Her notu `plan.md` §3'teki işlevlerden biriyle eşle.
3. `plan.md` §2'deki beş soruyu cevapla ve ana fikri tek cümleyle yaz.
4. `plan.md` §9'daki çalışma planını doldur (yazı türüne göre sıra: `plan.md` §6, `stil.md` §10). Planı çalışma notu olarak tut; onay için durma.
5. Değişebilen bilgileri (ücret, açılış saati, kapalı gün, rezervasyon, ulaşım) resmî/güvenilir kaynaklardan doğrula; kaynak ve kontrol tarihini çalışma notlarına yaz (`stil.md` §11).
6. Taslağı `stil.md` sesinde yaz: varsayılan hitap "siz", tek H1, H2/H3 hiyerarşisi, karar değiştiren bilgi önerinin yanında.
7. `editor.md` §13'teki dört geçişi uygula: anlam ve gerçeklik → okurun bilgisi ve akış → cümle ve ritim → yayın kontrolü.
8. Son kontroller: `plan.md` §10 listesi, `stil.md` §16 yayın öncesi kontrol, `editor.md` §14 kabul ölçütleri. Sorun varsa düzelt.
9. Kapanışı kontrol et: girişteki düşünceyi tamamlıyor mu? Yorum çağrısı varsa yazıya özgü ve doğal mı, önceki yazılardakiyle aynı mı? (aynıysa değiştir veya çıkar)
10. Çıktıyı kaydet; yazının dışında kısa **Editör Notları** ekle (doğrulanamayan bilgiler, insandan beklenen netleştirmeler, kaynak listesi ve kontrol tarihleri).

## Outputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-tr.md`:
  - Yayına hazır Türkçe yazı (başlık + gövde)
  - `---` ile ayrılmış **Editör Notları** (yayınlanmaz)

## Quality Bar
- Kişisel deneyimlerin tamamı notlara dayanıyor; uydurma sahne, duygu, diyalog yok.
- Denenen, araştırılan ve önerilen seçenekler birbirine karışmıyor.
- İlk birkaç paragrafta konu, açı ve fayda anlaşılıyor; başlıktaki vaat karşılanıyor.
- Rota; süre, kapalı gün, rezervasyon ve mola ihtiyacıyla uyumlu.
- Geçmiş deneyim ile güncel bilgi ayrılmış.
- `stil.md`, `plan.md` ve `editor.md` kontrol listelerinin tamamı geçiyor. Kritik bilgi hatası veya uydurulmuş deneyim varsa yazı yayına hazır sayılmaz.

## Tools
- Web araması ve sayfa okuma (doğrulama için)

## Integration
- Çıktı, TRANSLATION_EN ve IMAGE_PLANNING skill'lerinin girdisidir.
- Görsel planı TR metindeki başlık ve cümlelere göre yerleşim verir; TR metin sonradan değişirse görsel planı da güncellenir.
