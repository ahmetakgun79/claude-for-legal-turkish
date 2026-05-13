# Regulatory Legal - Legal Turkish

Turkiye regulasyon izleme ve politika gap takibi plugin'i. Komut adlari orijinal repo ile uyum icin Ingilizce kalir; hukuki icerik Resmi Gazete, Mevzuat Bilgi Sistemi, KVKK/Kurul, Rekabet Kurumu, SPK, BDDK, BTK, EPDK, TCMB, Ticaret Bakanligi ve sektor kurum duyurulari ekseninde yurutulur.

> Bu plugin hukuki danismanlik vermez. Her cikti hukukcu incelemesine tabi taslak, izleme notu veya karar destek ciktisidir. Resmi metin, yururluk tarihi, gorus son tarihi, idari para cezasi, kurum karari ve sektor yukumlulugu somut dosyada guncel resmi kaynaktan dogrulanmalidir.

## Kimler Icin

| Rol | Ana is akislar |
|---|---|
| Regülasyon / compliance hukukcusu | Watchlist, gap triage, politika guncelleme koordinasyonu |
| KVKK / urun / finans / telekom ekipleri | Kendi alanlarina dokunan gelismeleri filtrelenmis sekilde almak |
| GC / yonetim | Maddi gap, son tarih ve eskalasyon raporu |
| Ozel hukuk burosu | Muvekkil bazli regulasyon degisikligi ve gorus sureci takibi |

## Komutlar

| Komut | Ne yapar |
|---|---|
| `/regulatory-legal:cold-start-interview` | Izlenecek kurumlari, politika kutuphanesini ve materiality esigini kurar |
| `/regulatory-legal:reg-feed-watcher` | Izleme listesindeki resmi kaynaklari simdi kontrol eder |
| `/regulatory-legal:policy-diff [duzenleme]` | Duzenleme degisikligini politika kutuphanesiyle karsilastirir |
| `/regulatory-legal:gaps` | Acik gap tracker durumunu gosterir |
| `/regulatory-legal:comments` | Taslak duzenleme / kamuoyu gorusu / gorus bildirme son tarihlerini takip eder |
| `/regulatory-legal:policy-redraft` | Gap'i kapatacak politika degisikligi taslagi uretir |
| `/regulatory-legal:matter-workspace` | Cok muvekkilli kullanimda matter izolasyonu yonetir |

## Varsayilan Kaynak Omurgasi

- Resmi Gazete ve Mevzuat Bilgi Sistemi.
- KVKK/Kurul duyurulari, kararlar, rehberler, standart sozlesmeler.
- Rekabet Kurumu kararlar, duyurular, mevzuat calismalari.
- SPK bultenleri, duyurular, idari yaptirimlar.
- BDDK mevzuat duyurulari, duzenleme taslaklari, kurul kararlari.
- BTK duyurulari, kurul kararlari ve kamuoyu gorusune acilan taslaklar.
- EPDK, TCMB, MASAK, Ticaret Bakanligi, TİTCK, SGK/ISKUR gibi sektor kaynaklari.

## Ilk Kurulum

```text
/regulatory-legal:cold-start-interview
```

Kurulum; izlenecek kurumlari, sektorleri, kaynak URL'lerini, politika sahiplerini, materiality esigini, gap kapanis surecini ve gorus bildirme karar sahiplerini profil dosyasina yazar.

## Durum

Bu klasor Legal Turkish icin ilk tur regulatory uyarlamasidir. Ikinci turda gercek kurum duyurusu, Resmi Gazete metni, taslak duzenleme ve ic politika kutuphanesiyle smoke test onerilir.
