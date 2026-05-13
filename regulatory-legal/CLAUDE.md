<!--
CONFIGURATION LOCATION

User-specific configuration for this plugin lives at:

  ~/.claude/plugins/config/claude-for-legal/regulatory-legal/CLAUDE.md

Rules:
1. Skills read configuration from that path, not from this template.
2. If the user config is missing or still contains [PLACEHOLDER], stop before substantive work and ask the user to run /regulatory-legal:cold-start-interview.
3. Setup and cold-start-interview write to that path.
4. This file is the shipped template and may be replaced by plugin updates.
-->

# Regulatory Legal Practice Profile - Legal Turkish Template

Bu profil, regulatory-legal skill'lerinin Turkiye regulasyon izleme ve politika gap takibi icin calismasini saglar. Komut adlari Ingilizce kalir; hukuki cerceve Resmi Gazete, Mevzuat Bilgi Sistemi, KVKK, Rekabet, SPK, BDDK, BTK, EPDK, TCMB, MASAK, Ticaret Bakanligi, TİTCK ve diger sektor kurumlari esas alinarak yurutulur.

## Kurum / Muvekkil Profili

**Kurum / muvekkil:** [PLACEHOLDER]
**Sektor:** [PLACEHOLDER - finans / e-ticaret / telekom / enerji / saglik / teknoloji / uretim / kamu yuklenicisi / diger]
**Faaliyet modeli:** [PLACEHOLDER]
**Hedef pazarlar:** [PLACEHOLDER - Turkiye / AB / ABD / diger]
**Regulasyon sahibi ekip:** [PLACEHOLDER]
**Politika sahipleri:** [PLACEHOLDER]
**Eskalasyon:** [PLACEHOLDER - hukuk, compliance, KVKK, risk, ic denetim, yonetim, dis hukuk]

## Izlenen Kurumlar

| Kurum / kaynak | Alan | Neden izleniyor | Kaynak / izleme yöntemi | Onem |
|---|---|---|---|---|
| Resmi Gazete / Mevzuat Bilgi Sistemi | Genel mevzuat | [PLACEHOLDER] | https://www.resmigazete.gov.tr / https://www.mevzuat.gov.tr | Ana |
| KVKK / Kurul | Kisisel veri | [PLACEHOLDER] | https://www.kvkk.gov.tr | [PLACEHOLDER] |
| Rekabet Kurumu | Rekabet / platform / M&A | [PLACEHOLDER] | https://www.rekabet.gov.tr | [PLACEHOLDER] |
| SPK | Sermaye piyasasi / kripto | [PLACEHOLDER] | https://www.spk.gov.tr | [PLACEHOLDER] |
| BDDK | Bankacilik / finans | [PLACEHOLDER] | https://www.bddk.gov.tr | [PLACEHOLDER] |
| BTK | Telekom / elektronik haberlesme | [PLACEHOLDER] | https://www.btk.gov.tr | [PLACEHOLDER] |
| EPDK | Enerji | [PLACEHOLDER] | https://www.epdk.gov.tr | [PLACEHOLDER] |
| TCMB | Odeme / elektronik para | [PLACEHOLDER] | https://www.tcmb.gov.tr | [PLACEHOLDER] |

## Kullanici Rolu

**Rol:** [PLACEHOLDER - Avukat / hukuk musaviri / compliance / KVKK sorumlusu / risk / non-lawyer]
**Sorumlu hukukcu:** [PLACEHOLDER]

Non-lawyer kullanici icin ciktilar nihai uyum beyanı, kurum gorusu, resmi basvuru veya politika onayi degildir. Hukukcu incelemesi ve gerekli hallerde sektor uzmanı/dış hukuk kontrolu gerekir.

## Entegrasyonlar

| Entegrasyon | Durum | Fallback |
|---|---|---|
| Dokuman deposu / policy library | [PLACEHOLDER] | Kullanici dosya yolu veya metin yapistirir |
| Slack / Teams / e-posta | [PLACEHOLDER] | Digest dosya veya sohbet ciktisi |
| Kurum kaynağı / RSS / web izleme | [PLACEHOLDER] | Manuel kaynak kontrolu ve paste-in |
| Hukuk arastirma araci | [PLACEHOLDER] | Resmi kaynak + kullanici sagladi + dogrula etiketi |

## Politika Kutuphanesi

| Politika / prosedur | Dosya / kaynak | Son guncelleme | Sahip | Ilgili kurum |
|---|---|---|---|---|
| [PLACEHOLDER] | | | | |

## Materiality Esigi

**Her zaman maddi / aksiyon gerekir:**
- Yururluge girmis kanun, yonetmelik, teblig, kurul karari veya baglayici karar.
- Son tarih, bildirim, lisans, raporlama, tutar, ceza veya uygulama degisikligi iceren gelisme.
- Sirketin ana faaliyet sektorunde yeni yukumluluk veya yasak.
- Kurum incelemesi, yaptirim, veri ihlali, rekabet sorusturmasi veya sektor uyarisi.

**Incelemeye deger:**
- Taslak duzenleme, kamuoyu gorusu, ilke karar taslagi, rehber, duyuru.
- Rakip/sektor hakkinda yaptirim veya karar.
- Kurum bulteni, sektor raporu veya uygulama beklentisi.

**FYI / izleme:**
- Genel konusma, etkinlik, akademik yayin, istatistik bulteni, dogrudan aksiyon dogurmayan haber.

## Gap Yaniti

**Triager:** [PLACEHOLDER]
**Politika update sahibi:** [PLACEHOLDER]
**Tracker:** [PLACEHOLDER - YAML / spreadsheet / ticket]
**Eskalasyon:** [PLACEHOLDER]
**Risk kabul yetkilisi:** [PLACEHOLDER]

## Gorus Bildirme / Taslak Takibi

**Takip edilen taslak kaynaklari:** [PLACEHOLDER]
**Karar sahibi:** [PLACEHOLDER]
**Gorus hazirlama sahibi:** [PLACEHOLDER]
**Ic son tarih standardi:** [PLACEHOLDER - resmi son tarihten kac is gunu once]

## Cikti Kurallari

Dahili analiz, gap raporu, politika diff'i, izleme digest'i ve politika redraft taslaklarinin basina su baslik konur:

```text
GIZLI HUKUKI / REGULASYON IZLEME CALISMA TASLAGI - HUKUKCU INCELEMESINE TABIDIR
Bu cikti hukuki gorus, uyum beyanı, resmi kurum gorusu veya politika onayi yerine gecmez.
```

Disari gidecek kurum gorusu, musteri notu, yonetim ozeti veya public comment metninde bu dahili baslik kullanilmaz; ic analiz ile dis metin ayri tutulur.

Her onemli ciktidan once tek reviewer note ver:

```markdown
Reviewer note
- Kaynaklar: [Resmi Gazete / Mevzuat.gov.tr / kurum sitesi / policy library / kullanici sagladi / dogrulanamadi]
- Okuma kapsami: [tam metin / ozet / secili madde / yalnizca duyuru]
- Dogrulanmasi gerekenler: [yururluk, son tarih, kapsam, yaptirim, kurum yorumu, policy versiyonu]
- Aksiyon oncesi: [hukukcu onayi / dis hukuk / sektor uzmanı / yonetim / risk kabul]
```

Kaynak etiketi:

- `[Resmi Gazete]`, `[Mevzuat.gov.tr]`, `[KVKK/Kurul]`, `[Rekabet Kurumu]`, `[SPK]`, `[BDDK]`, `[BTK]`, `[EPDK]`, `[TCMB]`, `[Ticaret Bakanligi]` yalnizca bu oturumda ilgili resmi kaynak kontrol edildiyse.
- `[kullanici sagladi]` kullanici duyuru, metin, politika veya ekran verdiğinde.
- `[ikincil kaynak - resmi kaynaktan dogrula]` hukuk burosu bulteni, haber, aggregator veya yorum icin.
- `[model bilgisi - dogrula]` kaynak cekilmeden kullanilan genel bilgi icin.

## Matter Workspaces

**Enabled:** [PLACEHOLDER - evet/hayir]
**Active matter:** none - practice-level context only
**Cross-matter context:** off
**Matters path:** `~/.claude/plugins/config/claude-for-legal/regulatory-legal/matters/`

## Bu Profil Ne Yapmaz

- Resmi Gazete, kurum sistemi, UYAP, VERBIS, ETBIS, SPK/BDDK/BTK/EPDK portali veya baska resmi sisteme basvuru yapmaz.
- Uyum sertifikasyonu veya nihai hukuki gorus vermez.
- Politika kaynagini dogrudan degistirmez; yalnizca redraft teklifi uretir.
- Guncel tarih/tutar/yururluk/son tarih bilgilerini resmi kaynak kontrolu olmadan kesin kabul etmez.
