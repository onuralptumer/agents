# Skill: Editoryal Kalite Kontrolü (Editorial Review)

## Purpose
ARTICLE_WRITING'in ürettiği taslağı yayından önce açıklık, bilgi sırası, tutarlılık, doğruluk ve dil kalitesi açısından düzenleyip nihai metne dönüştürmek.

Temel yaklaşım: Okura bir sorunu, fikri veya kararı göstermek; düşünceleri onun takip edebileceği sırada anlatmak; anlamı ve yazarın sesini koruyarak gereksiz zihinsel yükü azaltmak.

> Kaynak: Kullanıcının `editor.md` rehberi (Steven Pinker'ın *The Sense of Style* özetinden uyarlanmış). Orijinali seyahat yazıları içindi; buradaki kurallar aynı ilkelerin LinkedIn iş/teknoloji makalelerine uyarlamasıdır.

## Serves Goals
- Etkileşim almak (reaksiyon >100) — okuru yormayan, net duruşlu metin daha çok okunur ve tepki alır
- Görünürlüğü artırmak (gösterim >2.000) — ilk satırlarda konuya doğrudan giren metin "daha fazlasını gör" tıklaması alır
- Düzenli yayın — her hafta aynı kalite çıtasından geçen metin

## Inputs
- `outputs/YYYY-MM-DD_linkedin-paylasim_makale.md` — ARTICLE_WRITING taslağı
- `knowledge/AUDIENCE.md` — üç okur segmenti
- `knowledge/BRAND.md` — ses tonu
- İnsanın kişisel notları (`data/imports/`)

## Okur: Üç segment, tek metin
Makale aynı anda üç okura hitap eder (bkz. `knowledge/AUDIENCE.md`):

| Segment | Metinden ne arar? | Editörün kontrol sorusu |
|---|---|---|
| Üst düzey yönetici | Stratejik etki, maliyet/kâr, risk, karar | İlk 3 satırda "bu benim işime/bilançoma ne yapar?" sorusunun cevabı var mı? |
| Orta kademe yönetici | Uygulama, ekip, süreç, ölçüm | Yarın ekibiyle konuşabileceği somut bir adım veya çerçeve var mı? |
| Mühendis | Doğruluk, mekanizma, teknik derinlik | Teknik iddia doğru ve yeterince kesin mi? Pazarlama diline kaçmış mı? |

Yönetici için teknik ayrıntıyı gömme, mühendis için de basitleştirip yanlışlama. Teknik terimi ilk kullanımda bir cümleyle açıkla; mekanizmayı doğru anlat; ardından iş etkisine bağla.

## Kurallar

### 1. Klasik üslup: Okurla aynı yere bak
Yazarı kürsüye, okuru öğrenci konumuna koyma. Okurun aklını ve merakını varsay, konu bilgisini varsayma. Metin yazma süreci hakkında değil, konunun kendisi hakkında konuşsun.

### 2. Soyut iddia yerine belirleyici ayrıntı
"Yapay zeka verimliliği ciddi şekilde artırıyor" okura az şey gösterir. Kaynaklı bir rakam, somut bir süreç adımı veya gerçek bir vaka kullan: hangi hatta, hangi metrik, ne kadar, ne sürede.
Canlılık için ayrıntı icat edilmez. Kişisel deneyim yalnızca insanın notlarında varsa kullanılır; yoksa `[KİŞİSEL DENEYİM: ...]` yer tutucusu kalır.

### 3. Bilgi lanetini önle
Yazarın bildiği kavram okurun zihninde hazır değildir.
- Kısaltmaları (OEE, MES, ERP, TPM, LLM, RAG vb.) ilk kullanımda aç; tek kullanım için kısaltma yaratma.
- Bir yönetim çerçevesini veya teknolojiyi ilk geçtiği yerde somut parçalarıyla tanıt.
- "Bu yaklaşım", "o sistem" gibi göndermelerin neyi işaret ettiğini kontrol et.
- "Hızla", "ciddi oranda", "kolayca" yerine doğrulanmış süre, oran veya koşul ver.
- Okurun ihtiyaç duyduğu bağlamı, ilgili iddiadan önce koy.

### 4. Bilgi sırasını okura göre düzenle
Okurun bildiği noktadan başla, yeni bilgiyi onun üzerine kur. Her cümle öncekinin kurduğu tabloya bağlansın. Karar değiştiren bilgiyi (ön koşul, risk, maliyet, sınırlama) yan ayrıntıların arasında kaybetme; ilgili önerinin hemen yanına koy.
Bağlantı bağlaç sayısından değil, düşüncelerin birbirini hazırlamasından gelir. Kaynakta neden-sonuç yoksa "bu sayede" ile ilişki üretme.

### 5. Türkçe cümlede zihinsel yükü azalt
Türkçede yüklem sondadır; amaç okurun çok sayıda tamamlanmamış ilişkiyi aklında tutmasını önlemek. Şunları ara:
- Ana yükleme ulaşmadan biriken yan cümlecikler
- Birbirine gömülmüş sıfat-fiil ve isim tamlamaları
- Bir cümlede birkaç ayrı karar veya zaman dilimi

Her uzun cümleyi bölme; kısa cümleleri de peş peşe dizerek metni rapor maddelerine çevirme. Ölçüt kelime sayısı değil, ilk okumada anlaşılmadır.

### 6. Fiili isimlerin arkasına saklama
Kurumsal metinlerin en yaygın sorunu "zombi isimler"dir.

| Ağır | Doğrudan |
|---|---|
| Dijital dönüşümün gerçekleştirilmesi sağlanmalıdır. | Dönüşümü üretim hattından başlatın. |
| Maliyetlerin azaltılmasına yönelik çalışmalar yapıldı. | Fire oranını %4'ten %2,5'e indirdik. *(yalnızca gerçek veriyse)* |
| Verimlilik artışının elde edilmesi hedeflenmektedir. | Hedef: OEE'yi 6 ayda 8 puan artırmak. *(yalnızca gerçek hedefse)* |

Etken anlatımı tercih et ama edilgeni yasaklama. Edilgeni, bilinen sorumluluğu gizlemek veya zayıf bir iddiaya nesnellik görüntüsü vermek için kullanma.

### 7. Tutarlılığı kelime çeşitliliğine feda etme
Aynı kavramı sırf tekrar olmasın diye farklı adlarla anma ("dijital dönüşüm", "dijitalleşme", "teknolojik transformasyon" farklı şeyler sanılabilir). Bir terimi seç, tutarlı kullan.
Karşılaştırılan seçenekleri aynı ölçütlerle anlat (maliyet, süre, risk, gereken yetkinlik). Liste maddelerini dilbilgisel olarak paralel kur.

### 8. Bağlaçları ve olumsuzlamayı anlam için kullan
"Bu yüzden" gerçek sonuç, "ancak" gerçek karşıtlık getirsin. Çifte olumsuzluğu sadeleştir ("Yapay zekaya yatırım yapmamanın yanlış olmadığı söylenemez" → net bir görüş). Bir sınırlamayı belirten olumsuz cümle ("Bu yöntem kesikli üretimde işe yaramıyor") en açık ifade olabilir; koru.

### 9. Gereksiz çekinceleri azalt, anlamlı belirsizliği koru

| İfade türü | İşlem |
|---|---|
| "Bir bakıma denebilir ki…" gibi işlevsiz çekince | Cümleyi doğrudan kur. |
| "Sektöre göre %10–25 arasında değişiyor" gibi kaynaklı aralık | Koru. |
| "Bunu kendi tesisimizde denemedik" gibi deneyim sınırı | Koru. |
| "Bence" ile belirtilen kişisel görüş | Nesnel gerçek izlenimi doğacaksa koru. |

Akıcı görünmek için kesinlik üretme. Alay veya sözde vurgu için gelişigüzel tırnak kullanma.

### 10. Canlılığı ve yazarın sesini koru
Okurun zihninde görüntü oluşturan ayrıntıyı kısaltma uğruna çıkarma. İyi bir benzetme bilinmeyeni anlaşılır kılar; yanlış beklenti yaratan veya klişe benzetme ("veri yeni petroldür") yüktür. Özgün gözlem, zoraki espriden değerlidir. Gündelik Türkçe yanlış Türkçe değildir; "Ama" ile başlayan cümle veya yerinde devrik cümle otomatik hata sayılmaz.

### 11. LinkedIn'e özgü kontroller
- Hook (ilk 2 satır, ≈200 karakter) tek başına okunduğunda anlaşılır ve merak uyandırıcı mı?
- Gönderi metninde paragraflar mobilde rahat okunacak kadar kısa mı?
- Kapanış sorusu spesifik mi ve üç segmentten en az biri kolayca cevap verebilir mi?
- Hashtag'ler konuyla gerçekten ilgili mi?

## Process (Dört geçişli düzenleme)

1. **Anlam ve gerçeklik:** Ana mesajı ve verilen vaatleri kontrol et. Her rakamın kaynağını ve tarihini doğrula. Her kişisel deneyim insanın notuna dayanıyor mu? Şüpheli bilgiyi daha kesin söylemek yerine doğrula veya kapsamını daralt.
2. **Okurun bilgisi ve akış:** Metni sırayla üç segmentin gözüyle oku (yukarıdaki tablo). Açıklanmamış kavramları, kısaltmaları, konu atlamalarını ve muğlak göndermeleri düzelt. Her paragrafın öncekiyle ilişkisini kontrol et.
3. **Cümle ve ritim:** Zombi isimleri, gömülü yapıları, işlevsiz çekinceleri ve tekrar eden cümle başlangıçlarını sadeleştir. Yazarın sesini taşıyan gerçek ayrıntıları koru.
4. **Yayın kontrolü:** Başlık, hook, kaynak linkleri, rakam tutarlılığı (makale ve gönderi metninde aynı rakamlar), noktalama, hashtag'ler. Metin hâlâ seçilen konunun ana mesajına ve BRAND.md sesine uyuyor mu?

Sorunları tespit etmekle yetinme; nihai metinde düzelt. Somut sorunlar çözüldüğünde yeni fayda üretmeyen düzenleme turlarına devam etme. Kendi ikinci okumanı gerçek okur testi gibi sunma.

## Outputs
- Aynı `outputs/YYYY-MM-DD_linkedin-paylasim_makale.md` dosyasının nihai hali (henüz insana sunulmadıysa) veya `..._makale-v2.md`
- Dosyanın sonunda kısa **Editör Notu**: anlamı etkileyen düzeltmeler, doğrulanamayan bilgiler, insandan beklenen eklemeler

## Quality Bar (Kabul ölçütleri)
- [ ] Üst düzey yönetici ilk 3 satırda iş etkisini görüyor.
- [ ] Orta kademe yönetici en az bir uygulanabilir adım/çerçeve buluyor.
- [ ] Mühendis açısından teknik iddialar doğru ve yeterince kesin.
- [ ] Teknik terimler ve kısaltmalar ilk kullanımda açıklanmış.
- [ ] Yeni bilgi yeterli bağlamdan sonra geliyor; karar değiştiren bilgi önerinin yanında.
- [ ] Her rakam kaynaklı ve doğrulanmış; uydurma deneyim veya veri yok.
- [ ] Cümlelerde ana düşünce ve eylem kolay bulunuyor; zombi isim zinciri yok.
- [ ] Bağlaçlar gerçek mantıksal ilişkileri gösteriyor.
- [ ] Aynı kavramlar tutarlı adlarla anılıyor.
- [ ] Anlamlı belirsizlik ve kişisel görüş işaretleri korunmuş.
- [ ] Sadeleştirme anlamı, önemli ayrıntıları veya yazarın sesini silmemiş.
- [ ] Makale ve gönderi metni birbiriyle tutarlı.

Bu liste bir puanlama oyunu değildir. Uydurulmuş deneyim, anlam kayması veya okuru yanlış karara götürecek çelişki varsa metin yayına hazır sayılmaz.

## Tools
- Web araması (kaynak ve rakam doğrulama)

## Integration
- Girdi: ARTICLE_WRITING taslağı. Çıktı: insan onayına sunulan nihai metin.
- Yapısal bir sorun bulunursa (yanlış konu açısı, zayıf ana mesaj) ARTICLE_WRITING'e geri dönülür.
- Sık tekrar eden editoryal sorunlar journal'a; 3+ kez doğrulananlar MEMORY.md "Process Improvements" bölümüne yazılır.
