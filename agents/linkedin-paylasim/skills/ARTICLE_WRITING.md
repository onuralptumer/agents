# Skill: Makale Yazımı (Article Writing)

## Purpose
Seçilen konuyla LinkedIn'de yayına hazır makaleyi ve onu duyuracak/taşıyacak gönderi metnini yazmak.

## Serves Goals
- Görünürlüğü artırmak (gösterim >2.000) — güçlü hook ve okunabilir format ile "daha fazlasını gör" tıklaması ve dağıtım
- Etkileşim almak (reaksiyon >100) — net bir duruş, kanıt ve yorum davet eden kapanış
- Düzenli yayın (haftada 1)

## Inputs
- `outputs/YYYY-MM-DD_linkedin-paylasim_konu-arastirmasi.md` — önerilen konu, hook'lar, kaynaklar
- `knowledge/BRAND.md` — ses tonu
- `knowledge/AUDIENCE.md` — üç okur segmenti (üst düzey yönetici, orta kademe yönetici, mühendis)
- `MEMORY.md` — işe yarayan hook, format, uzunluk
- `data/imports/` — insanın kişisel notları / saha hikayesi (varsa)

## Process
1. Konu araştırmasındaki önerilen konuyu al (insan farklı konu seçtiyse onu kullan).
2. Tek cümlelik ana mesajı yaz: "Okur bu yazıdan sonra neyi farklı düşünecek / yapacak?"
3. Kaynakları tekrar doğrula; her rakamın kaynağı ve tarihi elinde olsun.
4. Makaleyi şu yapıda yaz:
   - **Başlık:** Somut, fayda veya gerilim içeren (ör. rakam, karşıtlık, soru). 60–80 karakter.
   - **Açılış (ilk 2–3 satır):** Çarpıcı veri, cesur iddia veya kısa sahne. Giriş cümlesi yok, doğrudan konuya.
   - **Problem:** Kitlenin bildiği acıyı kendi diliyle tarif et.
   - **İçgörü / Çerçeve:** 3–5 maddelik net bir çerçeve, model veya adım listesi.
   - **Kanıt:** Kaynaklı veri + somut örnek (tercihen Türkiye/üretim bağlamı; insanın deneyimi varsa ona yer aç: `[KİŞİSEL DENEYİM: ...]`).
   - **Uygulanabilir çıktı:** Okurun yarın yapabileceği 1–3 adım.
   - **Kapanış:** Net bir görüş + yorum davet eden açık uçlu, spesifik bir soru.
   - **Kaynaklar:** Liste halinde.
   - Uzunluk: 600–1.000 kelime (MEMORY.md'de farklı bir bulgu varsa onu uygula).
5. LinkedIn gönderi metnini yaz (makaleyi paylaşırken veya tek başına uzun gönderi olarak kullanılabilir):
   - İlk 2 satır = hook (≈200 karakter içinde "...daha fazlasını gör" öncesi merak uyandırmalı)
   - Kısa paragraflar, bol boşluk, en fazla 1–2 emoji
   - 3–5 maddelik özet
   - Kapanışta tek, spesifik soru
   - 3–5 hashtag (geniş + niş karışık, ör. #DijitalDönüşüm #YapayZeka #ÜretimYönetimi #Verimlilik #Yalınüretim)
   - Dış link varsa gönderide değil ilk yorumda paylaşılmasını öner (hipotez — MEMORY.md ile doğrula)
6. 2 alternatif başlık ve 2 alternatif hook ver (A/B seçimi insana).
7. Görsel brief'i yaz: kapak görseli fikri veya 5–7 sayfalık karusel/PDF taslağı (sayfa başlıkları).
8. Taslağı kaydet ve **EDITORIAL_REVIEW** skill'ini çalıştır (dört geçişli düzenleme). Nihai metni insan onayına sun (journal'a "onay bekliyor" girdisi).

## Outputs
- `outputs/YYYY-MM-DD_linkedin-paylasim_makale.md` şu bölümlerle:
  - Seçilen konu ve ana mesaj
  - Makale (başlık + gövde + kaynaklar)
  - LinkedIn gönderi metni
  - Alternatif başlıklar ve hook'lar
  - Görsel / karusel brief'i
  - Hashtag'ler ve önerilen yayın günü/saati
  - İnsandan beklenenler (kişisel deneyim ekleme, onay)

## Quality Bar
- Hook ilk 2 satırda tek başına okunduğunda "devamını okumak istiyorum" dedirtiyor.
- En az 1 kaynaklı, güncel (son 12 ay) veri var; uydurma rakam yok.
- Net bir görüş/duruş var; "hem öyle hem böyle" yazısı değil.
- Okur için en az 1 uygulanabilir adım var.
- Kapanış sorusu spesifik ("Siz ne düşünüyorsunuz?" değil; "Sizin hattınızda en çok fire hangi adımda oluşuyor?" gibi).
- Engagement bait, abartılı vaat, jargon yığını yok; BRAND.md tonuna uygun.
- Yazım ve dilbilgisi kontrol edilmiş Türkçe.

## Tools
- Web araması (kaynak doğrulama)

## Integration
- Girdi: TOPIC_RESEARCH çıktısı.
- Çıktı: EDITORIAL_REVIEW'e taslak olarak gider; insana yalnızca editoryal kontrolden geçmiş metin sunulur.
- Çıktı insan onayından sonra yayınlanır; yayın tarihi ve performansı `data/imports/linkedin-stats.csv`'ye girilir ve PERFORMANCE_REVIEW tarafından analiz edilir.
