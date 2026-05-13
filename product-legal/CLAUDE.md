<!--
CONFIGURATION LOCATION

User-specific configuration for this plugin lives at:

  ~/.claude/plugins/config/claude-for-legal/product-legal/CLAUDE.md

Rules:
1. Skills read configuration from that path, not from this template.
2. If the user config is missing or still contains [PLACEHOLDER], stop before substantive work and ask the user to run /product-legal:cold-start-interview.
3. Setup and cold-start-interview write to that path.
4. This file is the shipped template and may be replaced by plugin updates.
-->

# Product Legal Practice Profile - Legal Turkish Template

Bu profil, product-legal skill'lerinin Turkiye urun hukuku ve uygulamasina gore calismasi icin varsayilan cercevedir. Komut adlari geriye donuk uyumluluk icin Ingilizce kalir; hukuki icerik Turk tuketici hukuku, ticari reklam, e-ticaret, KVKK, urun guvenligi, sektor regulasyonu ve AI yonetisimi ekseninde yurutulur.

## Sirket ve Urun Profili

**Sirket / muvekkil:** [PLACEHOLDER]
**Urun / hizmet:** [PLACEHOLDER]
**Model:** [PLACEHOLDER - B2C / B2B / B2B2C / pazaryeri / abonelik / fintech / saglik / oyun / egitim / diger]
**Hedef pazarlar:** [PLACEHOLDER - Turkiye / AB / ABD / diger]
**Kullanicilar:** [PLACEHOLDER - tuketici / tacir / calisan / hasta / finansal tuketici / ogrenci / cocuk]
**Regulasyon ayak izi:** [PLACEHOLDER - Ticaret Bakanligi, Reklam Kurulu, KVKK/Kurul, BTK, BDDK/TCMB, SPK, TİTCK, EPDK, Rekabet, belediye/yerel izin, AB/ABD varsa ayrica]
**Risk istahi:** [PLACEHOLDER - muhafazakar / dengeli / hizli-deneysel; kategori bazli sapmalar]
**Lansman gate sahibi:** [PLACEHOLDER]
**Eskalasyon:** [PLACEHOLDER - hukuk, KVKK, guvenlik, compliance, GC, urun lideri, pazarlama lideri]

## Kullanici Rolu

**Rol:** [PLACEHOLDER - Avukat/hukuk musaviri / hukuk operasyonu / PM / pazarlama / kurucu / non-lawyer]
**Sorumlu hukukcu:** [PLACEHOLDER]

Non-lawyer kullanicilar icin ciktilar nihai izin veya "ship" onayi degildir; hukukcuya goturulecek karar destek notu uretir. Reklam yayini, abonelik/checkout degisikligi, KVKK aksiyonu, resmi bildirim, app store/platform uyumu veya lansman onayi once hukukcu tarafindan gozden gecirilir.

## Cikti Kurallari

Dahili lansman incelemesi, ozellik risk analizi, reklam iddia incelemesi ve hizli triage ciktilarinda su baslik kullanilir:

```text
GIZLI HUKUKI / URUN HUKUKU CALISMA TASLAGI - HUKUKCU INCELEMESINE TABIDIR
Bu cikti hukuki gorus, reklam onayi, KVKK karari veya lansman izni yerine gecmez.
```

Disarida yayinlanacak pazarlama metni, musteri FAQ'i, app store aciklamasi, ticket yorumu veya PM'e gidecek sade ozet icin bu dahili baslik kullanilmaz. Dahili analiz ile paylasilabilir ozet ayri tutulur.

Her kritik ciktidan once tek reviewer note ver:

```markdown
Reviewer note
- Kaynaklar: [okunan PRD/reklam metni/sozlesme/politika/resmi kaynak/kullanici beyani]
- Okuma kapsami: [tamami / secili kisim / yalnizca ticket ozeti]
- Dogrulanmasi gerekenler: [6502, 6563, reklam yonetmeligi, KVKK, IYS, sektor mevzuati, platform politikasi, tutar/tarih]
- Aksiyon oncesi: [hukukcu onayi / KVKK triage / Reklam Kurulu riski / sektor uzmani / guvenlik / urun lideri]
```

Kaynak etiketi gercegi yansitir:

- `[Ticaret Bakanligi]` yalnizca Bakanlik sayfasi, kilavuz veya mevzuat linki bu oturumda kontrol edildiyse.
- `[KVKK/Kurul]` yalnizca Kurum/Kurul sayfasi, rehber, karar veya duyuru bu oturumda kontrol edildiyse.
- `[Mevzuat.gov.tr]` veya `[Resmi Gazete]` yalnizca resmi metin kontrol edildiyse.
- `[platform politikasi - canli dogrula]` app store, sosyal medya, arama/reklam agi, kart agi veya marketplace kurali canli sayfadan dogrulanmadiginda kullanilir.
- `[kullanici sagladi]` kullanici PRD, reklam metni, ekran goruntusu, policy, ticket veya sozlesme verdiyse.
- `[model bilgisi - dogrula]` kaynak cekilmeden kullanilan genel bilgi icindir.

Tutar, idari para cezasi, basvuru/esik degeri, Kurul/Reklam Kurulu karari, platform politikasi, sektor izni veya guncel yururluk tarihi icin canli resmi kaynak kontrol edilmeden kesin ifade kurma.

## Varsayilan Lansman Inceleme Cercevesi

1. **Sozlesme ve kullanici taahhutleri:** ToS, abonelik, iptal/cayma, garanti, SLA, mesafeli satis, ayipli mal/hizmet, B2B/B2C ayrimi.
2. **KVKK ve veri:** yeni veri, yeni amac, profil/cerez, acik riza, aydinlatma, IYS, yurt disina aktarim, tedarikci/alt isleyen.
3. **Reklam ve haksiz ticari uygulamalar:** dogru-durust reklam, karsilastirma, indirim, ortulu reklam, influencer, saglik/gida/finans iddialari.
4. **E-ticaret ve checkout:** 6563, ETHS/ETAHS rolleri, ticari elektronik ileti, on bilgilendirme, siparis onayi, iade/cayma, abonelik yenileme.
5. **Urun guvenligi, erisilebilirlik ve sektor:** guvensiz urun, teknik mevzuat, BTK/BDDK/SPK/TCMB/TİTCK/EPDK/Rekabet, kamu veya yerel izinler.
6. **Fikri haklar ve icerik:** marka/telif, ucuncu taraf icerik, UGC, acik kaynak, veri seti, model egitimi, takedown.
7. **Guvenlik ve ucuncu taraflar:** yeni vendor, API, bulut, veri akisi, SLA, guvenlik review, sozlesme/DPA.
8. **AI / otomasyon:** AI use-case, otomatik karar, insan denetimi, sentetik icerik, model egitimi, AI vendor sarti.

## Risk Kalibrasyonu

| Pattern | Varsayilan cagri | Tipik aksiyon |
|---|---|---|
| Saf UI/icerik duzeltmesi, yeni veri veya iddia yok | Dusuk | Kisa FYI |
| Yeni analitik/cerez/veri amaci | Orta/Yuksek | KVKK triage, aydinlatma/cerez kontrolu |
| Tuketici checkout, fiyat, indirim, abonelik, otomatik yenileme | Yuksek | 6502/mesafeli sozlesme/abonelik kontrolu |
| Karsilastirmali, mutlak veya sayisal reklam iddiasi | Yuksek | Kanit dosyasi ve reklam incelemesi |
| Influencer, yorum, testimonial veya ortulu reklam riski | Yuksek | Acik ifsa ve mecra kontrolu |
| Cocuk, saglik, finans, egitim, telekom, enerji, kamu | Yuksek/Bloke | Sektor uzmani ve resmi kaynak kontrolu |
| Yurt disina veri aktarimi veya AI/model egitimi | Yuksek/Bloke | KVKK/AI governance triage |
| Yeni vendor veya entegrasyon veri aliyorsa | Orta/Yuksek | Vendor/DPA/guvenlik review |

## Pazarlama Iddialari

**Reviewer:** [PLACEHOLDER]
**Karsilastirmali reklam politikasi:** [PLACEHOLDER - yasak / sadece kanitla / sektor uzmani onayi ile]
**Kanit standardi:** [PLACEHOLDER - yayin oncesi yazili kanit / veri ekibi onayi / harici rapor / test metodolojisi]
**Yasakli veya hassas ifadeler:** [PLACEHOLDER - en iyi, tek, garantili, risksiz, tamamen guvenli, 100%, ucretsiz, sinirsiz, doktor onayli, yatirim getirisi]
**Indirim/fiyat kurali:** [PLACEHOLDER]
**Influencer/testimonial kurali:** [PLACEHOLDER]

## E-ticaret / Abonelik Kapilari

- on bilgilendirme,
- mesafeli sozlesme,
- cayma/istisna,
- abonelik feshi ve yenileme,
- fiyat/indirim gosterimi,
- siparis ozeti ve onay,
- ticari elektronik ileti/IYS,
- elektronik pazar yeri rolleri,
- musteri hizmetleri ve sikayet akisi.

## KVKK / AI / Guvenlik Kapilari

KVKK iceren her lansmanda `/privacy-legal:use-case-triage` onerilir. AI, otomatik karar, model egitimi, sentetik icerik veya AI vendor varsa `/ai-governance-legal:use-case-triage` ve gerekirse vendor incelemesi tetiklenir. Guvenlik ve tedarikci riskleri hukuk degerlendirmesine yazilir ama teknik onay varsayilmaz.

## Matter Workspaces

**Enabled:** [PLACEHOLDER - evet/hayir]
**Active matter:** none - practice-level context only
**Cross-matter context:** off
**Matters path:** `~/.claude/plugins/config/claude-for-legal/product-legal/matters/`

## Bu Profil Ne Yapmaz

- Lansman, reklam, abonelik akisi veya app store gonderimi icin nihai onay vermez.
- Kurum, platform, UYAP, IYS, VERBIS, ETBIS veya resmi sisteme islem yapmaz.
- Tutar, esik, ceza, platform kurali veya sektor yukumlulugunu guncel kaynak kontrolu olmadan kesinlestirmez.
- Teknik guvenlik, urun guvenligi veya performans iddiasini belge olmadan dogru varsaymaz.
