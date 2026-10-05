# Skill: İngilizce Çeviri

## Purpose
Onaylanmaya hazır Türkçe yazıyı anlamını, yazarın sesini ve ayrıntılarını koruyarak doğal okunan, yayına hazır İngilizce yazıya çevirmek.

## Serves Goals
- Okunma (>500/hafta) — İngilizce sürüm, uluslararası okura ikinci bir okunma kanalı açar
- Yayına hazır içerik

## Inputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-tr.md` — editoryal kontrolden geçmiş Türkçe yazı
- `guides/translation.md` — çeviri kuralları ve kontrol listesi
- `MEMORY.md` — tutarlı kullanılacak terimler (varsa)

## Process
1. Türkçe yazının yalnızca yayınlanacak bölümünü al; Editör Notları'nı çevirme.
2. Metnin samimiyetini, ritmini, mizahını ve okurla kurduğu ilişkiyi belirle (`translation.md` §4). Bu incelemeyi çıktıya yazma.
3. Varsayılanlarla çevir: doğal Amerikan İngilizcesi, kaynak metnin okuru, kaynak ton (`translation.md` §2).
4. Yer adları, marka adları, tarihler, sayılar, para birimleri ve çocuk yaşı için `translation.md` §6 kurallarını uygula. "Seyahat Tarifleri" marka adını çevirme.
5. Başlık hiyerarşisini, listeleri, tabloları, bağlantıları ve görsel yer tutucularını koru (`translation.md` §7).
6. İki ayrı okuma yap (`translation.md` §9):
   - **Sadakat:** Türkçe kaynakla karşılaştır — her bölüm, sayı, olumsuzluk, kesinlik düzeyi, ben/biz/siz ayrımı.
   - **Doğallık:** Yalnızca İngilizceyi oku — klişe ("hidden gem", "nestled", "breathtaking"), çeviri kokan yapı, tutarsız terim.
7. Kaydet. Anlamı etkileyen çözülemeyen belirsizlik varsa metnin dışına kısa Türkçe editör notu ekle; sorun yoksa not ekleme.

## Outputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-en.md` — yayına hazır İngilizce yazı (+ gerekiyorsa ayrı, kısa Türkçe editör notu)

## Quality Bar
- Kaynakta olmayan hiçbir deneyim, iddia, süperlatif veya pazarlama dili eklenmemiş.
- İsimler, sayılar, tarihler, fiyatlar ve süreler birebir doğru.
- Metin, İngilizce yazan bir blog yazarının kaleminden çıkmış gibi okunuyor.
- Amerikan ve İngiliz yazımı karışmamış; tekrar eden terimler tutarlı.

## Tools
- Yok (yalnızca kaynak metin ve rehber)

## Integration
- Girdi: BLOG_WRITING_TR çıktısı.
- IMAGE_PLANNING'in ürettiği Türkçe alt metinler bu skill ile İngilizceye çevrilir (`translation.md` §7: alt metin ve açıklamalar çevrilir).
