# Product Legal - Legal Turkish

Turkiye urun hukuku, pazarlama ve lansman inceleme plugin'i. Komut adlari orijinal repo ile uyum icin Ingilizce kalir; hukuki cerceve Turk tuketici hukuku, ticari reklam, e-ticaret, KVKK, urun guvenligi, erisilebilirlik, sektor regulasyonlari ve AI yonetisimi ekseninde uygulanir.

> Bu plugin hukuki danismanlik vermez. Her cikti avukat/hukukcu incelemesine tabi taslak ve karar destek notudur. Kanun, yonetmelik, Kurul/Reklam Kurulu karari, platform politikasi, sektor duzenlemesi, tutar ve tarih bilgileri somut dosyada guncel kaynaktan dogrulanmalidir.

## Kimler Icin

| Rol | Ana is akislar |
|---|---|
| Urun hukukcusu / hukuk musaviri | Lansman incelemesi, ozellik risk analizi, eskalasyon |
| Urun yoneticisi | Hizli "bu sorun olur mu?" triyaji |
| Pazarlama / growth | Reklam, iddia, indirim, influencer ve kampanya kontrolu |
| KVKK / uyum / guvenlik | Veri, tedarikci, guvenlik, sektor regulasyonu kapilari |

## Komutlar

| Komut | Ne yapar |
|---|---|
| `/product-legal:cold-start-interview` | Turk urun hukuku profilini, risk kalibrasyonunu ve lansman surecini kurar |
| `/product-legal:launch-review [PRD/ticket]` | Lansmani kategori kategori inceler |
| `/product-legal:marketing-claims-review [metin]` | Reklam ve pazarlama iddialarini inceler |
| `/product-legal:is-this-a-problem [soru]` | Hizli PM/growth sorusuna kalibre triage verir |
| `/product-legal:feature-risk-assessment [ozellik]` | Tek bir ozellik/riske derin karar notu hazirlar |
| `/product-legal:matter-workspace` | Cok muvekkilli kullanimda matter izolasyonu yonetir |

## Turk Hukuku Kontrol Omurgasi

Varsayilan inceleme basliklari:

1. Sozlesme ve kullanici taahhutleri: kullanim sartlari, SLA, abonelik, cayma/iptal, garanti, ayipli hizmet, B2B/B2C ayrimi.
2. KVKK ve veri: yeni veri, yeni amac, acik riza, aydinlatma, cerez, IYS, yurt disina aktarim, tedarikci/alt isleyen.
3. Reklam ve haksiz ticari uygulamalar: dogruluk, durustluk, karsilastirmali reklam, indirim, ortulu reklam, influencer, saglik/gida/finans iddialari.
4. E-ticaret ve abonelik: 6563, ticari elektronik ileti, siparis akisi, mesafeli sozlesme, on bilgilendirme, iade/cayma, elektronik pazar yeri rolleri.
5. Urun guvenligi, erisilebilirlik ve sektor: guvensiz urun, teknik mevzuat, BTK, BDDK/TCMB, SPK, TİTCK, EPDK, Rekabet, yerel izinler.
6. Fikri haklar ve icerik: lisans, marka/telif, kullanici icerigi, veri seti/egitim verisi, acik kaynak, takedown sureci.
7. Guvenlik ve ucuncu taraflar: yeni vendor, entegrasyon, siber risk, veri akisi, sozlesme ve DPA/VK sozlesmesi.
8. AI / otomasyon: AI kullanim kaydi, otomatik karar, insan denetimi, sentetik icerik, model egitimi, AI vendor sarti.

## Ilk Kurulum

```text
/product-legal:cold-start-interview
```

Kurulum; sirketin urun yuzeyini, Turkiye ve diger hedef pazarlarini, regulasyon ayak izini, lansman gate'lerini, reklam iddia politikasini, KVKK/AI eskalasyonlarini ve ornek gecmis lansman kararlarini profil dosyasina yazar.

## Entegrasyonlar

`.mcp.json` icinde Jira/Linear/Asana, dokuman depolama ve Slack benzeri araclar tanimli olabilir. Bunlar yoksa plugin dosya yukleme, ticket metni yapistirma ve manuel workflow ile calisir.

## Durum

Bu klasor Legal Turkish icin ilk tur Turk urun hukuku uyarlamasidir. Gercek PRD, reklam metni, abonelik akisi, cerez/banner, mobil uygulama ekranlari ve e-ticaret checkout ornekleriyle ikinci tur smoke test onerilir.
