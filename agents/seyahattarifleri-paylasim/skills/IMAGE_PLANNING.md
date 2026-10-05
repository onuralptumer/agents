# Skill: Görsel Planı ve Promptları

## Purpose
Blog yazısı için gereken görsel sayısını belirlemek, her görselin yazıdaki tam yerini tarif etmek ve her görsel için kullanıma hazır üretim promptunu yazmak.

## Serves Goals
- Okunma (>500/hafta) — doğru yerde, farklı işlevli görseller uzun yazıda okuru devam ettirir
- Yayına hazır içerik

## Inputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-tr.md` — nihai Türkçe yazı
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-en.md` — İngilizce yazı (EN yerleşim cümleleri için)
- `data/imports/notlar/<slug>/` — kullanıcının gerçek fotoğrafları (varsa)
- `guides/fotograf-plan.md` — sayı, rol, oran, yerleşim ve plan kartı
- `guides/fotograf-uret.md` — prompt şablonu, ortak fotoğraf dili, gerçek mekân kuralları

## Process
1. Yazıyı çözümle: konu, tarih/mevsim, anlatı omurgası, gerçek mekânlar, yolculuğun niteliği, mevcut kullanıcı fotoğrafları (`fotograf-plan.md` §1).
2. Görsel sayısını belirle; uzunluk tablosunu başlangıç aralığı olarak kullan, kota olarak değil (`fotograf-plan.md` §2). Mevcut uygun kullanıcı fotoğraflarını sayıya dahil et, yalnızca eksikleri planla.
3. Görsel hikâyeyi kur: kapak + yazının gerektirdiği roller; geniş/orta/yakın kadraj çeşitliliği (`fotograf-plan.md` §3).
4. Tanınabilir gerçek mekânlar için güvenilir görsel referansları incele ve URL'lerini karta ekle. Referans yoksa temsili/dar kadraj veya `gerçek fotoğraf gerekli` seç (`fotograf-plan.md` §4).
5. Seri için baskın estetiği seç (Canon EOS 50D veya iPhone 15 hissi) ve oranları belirle (`fotograf-plan.md` §5–6).
6. Yerleşimi yaz: kapak = `Öne çıkan görsel`; diğerleri için **tam bölüm başlığı** + **metinden aynen alınmış kısa cümle** + önce/sonra. Aynı yerleşimi EN yazıdaki karşılık gelen başlık ve cümleyle de ver.
7. Her yeni görsel için `fotograf-plan.md` §7 üretim kartını ve `fotograf-uret.md` §4 şablonuyla **İngilizce, tek başına anlaşılır prompt** yaz. Yalnızca ilgili kısıtları tut.
8. Her görsel için Türkçe alt metin taslağı yaz; TRANSLATION_EN kurallarıyla İngilizce alt metnini ekle. Kaynak notu: "AI ile üretilmiş temsili görsel." / "AI-generated representative image."
9. Ortamda görsel üretim aracı varsa ve insan "Fotoğraf oluştur" dediyse `fotograf-uret.md` §5–7'ye göre üret ve kontrol et. Araç yoksa bunu açıkça belirt; üretilmemiş görseli hazır gibi sunma.

## Outputs
- `outputs/YYYY-MM-DD_seyahattarifleri-paylasim_<slug>-gorsel-plani.md`:
  - 2–3 cümlelik özet (toplam görsel, yeni üretilecek sayı, baskın estetik, gerekçe)
  - Plan tablosu: `ID | Rol / sahne | TR konum | EN konum | Cihaz hissi | Oran | Kaynak türü`
  - Her görsel için üretim kartı + İngilizce prompt
  - Önerilen dosya adları (küçük harf, ASCII, tireli)
  - TR ve EN alt metin taslakları, isteğe bağlı altyazılar
  - Kullanıcıdan istenecek gerçek fotoğraflar (varsa)

## Quality Bar
- Her görselin farklı bir editoryal işlevi var; tekrar eden manzara veya boşluk doldurucu kare yok.
- Her yerleşim, metinde aynen bulunan bir cümleye bağlı; "yazının ortasına" gibi belirsiz konum yok.
- Promptlar yazıda desteklenmeyen nesne, hava, etkinlik veya kişisel olay eklemiyor.
- Gerçek mekân ayrıntıları yalnızca incelenmiş referanslara dayanıyor; referans URL'leri kartta.
- İnsanlar kullanıcı veya ailesi gibi tanıtılmıyor; varsayılan kimliği belirsiz, arkadan veya insansız kadraj.

## Tools
- Web araması (görsel referans doğrulama)
- Görsel üretim aracı — yalnızca ortamda mevcutsa ve insan istediyse

## Integration
- Girdi: BLOG_WRITING_TR ve TRANSLATION_EN çıktıları.
- Yazı revize edilirse yerleşim cümleleri yeniden kontrol edilir.
