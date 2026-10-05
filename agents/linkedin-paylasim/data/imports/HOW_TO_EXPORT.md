# Veri Aktarımı: LinkedIn İstatistikleri

Agent'ın öğrenebilmesi için her makalenin performans verisini buraya eklemen gerekiyor.

## Ne zaman?
Makale yayınlandıktan **7 gün sonra** (KPI'lar 7 günlük ölçülür).

## Nereden?
1. LinkedIn'de yayınladığın makaleyi/gönderiyi aç.
2. Altındaki **"Analitiği görüntüle" / "View analytics"** linkine tıkla.
3. Gösterim (Impressions), Reaksiyon (Reactions), Yorum (Comments), Paylaşım (Reposts) değerlerini al.
   - Profil > Analitik > İçerik bölümünden toplu Excel dışa aktarımı da yapabilirsin; ilgili satırları aşağıdaki formata kopyala.

## Nereye?
`linkedin-stats.csv` dosyasına yeni bir satır ekle (eski satırları silme):

```
yayin_tarihi,makale_dosyasi,baslik,gosterim_7g,reaksiyon_7g,yorum_7g,paylasim_7g,yayin_saati,format,notlar
2026-10-07,2026-10-05_linkedin-paylasim_makale.md,"Örnek başlık",2450,118,23,9,08:30,makale+gonderi,"karusel kullanıldı"
```

- `format`: makale / gonderi / makale+gonderi / karusel / video
- `notlar`: dikkat çeken her şey (ör. yorumlarda sık sorulan soru, kim paylaştı)

## İsteğe bağlı
- Kişisel deneyim, saha hikayesi veya şirket örneği notlarını `YYYY-MM-DD_not.md` olarak buraya bırakabilirsin; agent bunları makalelere ekler (gizli bilgi içeriyorsa kullanılıp kullanılamayacağını belirt).
