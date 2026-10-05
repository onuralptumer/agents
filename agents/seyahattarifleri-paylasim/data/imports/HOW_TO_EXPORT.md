# Veri Aktarımı: Seyahat Tarifleri

## 1. Seyahat notları (her yeni yazı için)

`notlar/YYYY-MM-DD_<slug>.md` adıyla bir dosya oluştur (`<slug>`: küçük harf, ASCII, tireli; ör. `2026-10-05_sakiz-adasi.md`). Gerçek fotoğrafların varsa `notlar/<slug>/` klasörüne koy.

```text
Konu / destinasyon:
Yazı türü (biliniyorsa): şehir rehberi / çocukla seyahat / yemek / kişisel hikâye / hazırlık rehberi / hafta sonu rotası
Seyahat tarihi ve süresi:
Kimlerle seyahat edildi ve ilgili ihtiyaçlar (ör. 16 aylık çocuk, bebek arabası):
Varsa özel hedef okur:
Gerçek deneyim notlarım:
Mutlaka yer almasını istediklerim:
Kaçınılacak konular:
Varsa mevcut iç bağlantılar (seyahattarifleri.com yazıları):
İstenen yaklaşık uzunluk:
Görsel tercihi (isteğe bağlı): görsel sayısı, Canon / iPhone estetiği, kendi fotoğraflarım var/yok
```

Agent yalnızca bu notlarda yazdıklarını kişisel deneyim olarak kullanır. Kritik bir eksik olursa sorar; küçük eksiklerde eldeki malzemeyle ilerler.

## 2. Performans verisi (her pazartesi)

Kaynak: blog analitiği (ör. WordPress istatistikleri, Jetpack, Google Analytics) ve WordPress yorum paneli.

`blog-stats.csv` dosyasına geçen haftanın her yazısı için bir satır ekle (eski satırları silme):

```
hafta_baslangici,yazi_slug,dil,yayin_tarihi,okunma_7g,yorum_7g,ortalama_okuma_suresi,notlar
2026-10-05,sakiz-adasi,tr,2026-10-06,320,7,04:10,"yorumlarda feribot soruldu"
2026-10-05,sakiz-adasi,en,2026-10-06,140,2,03:05,
2026-10-05,_toplam,tr+en,,610,12,,"blog geneli haftalık toplam"
```

- `dil`: `tr`, `en` veya toplam satırında `tr+en`
- `_toplam` satırı: o haftanın blog geneli toplamı (KPI bu satırla ölçülür: okunma >500, yorum >10)
- `okunma_7g` / `yorum_7g`: o hafta içinde ilgili yazının aldığı okunma/yorum
- `notlar`: yorumlarda tekrar eden sorular, öne çıkan trafik kaynağı vb.
