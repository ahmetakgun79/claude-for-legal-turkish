# Claude for Legal - Türk Hukuku Adaptasyon Rehberi

Bu rehber, `Claude for Legal` içindeki `SKILL.md`, `CLAUDE.md`, agent ve referans dosyalarını Türk hukuku, Türk yargı sistemi ve Türk avukatlık uygulamasına uyarlamak için kullanılır.

Amaç, dosyaların teknik iskeletini koruyarak hukuki içeriği Türkiye uygulamasına taşımaktır. Gereksiz çeviri yapma; komut, klasör, YAML ve sistem davranışı ancak bilinçli bir yeniden adlandırma kararı varsa değiştirilmelidir.

---

## 1. Genel Kural

- `SKILL.md` dosyasinin frontmatter yapisini koru.
- YAML bloklarini, baslik siralamasini, karar agacini ve output formatlarini bozma.
- Hukuki kavramlari, kurumlari, mahkeme adlarini, sureleri, para birimini ve pratik is akisini Turkiye'ye uyarla.
- Komut ve klasor adlarini tek basina Turkcelestirme. Repo genelinde yeniden adlandirma yapilmadiysa `/commercial-legal:review` gibi mevcut komutlari koru.
- Dosya icinde ornek slug kullaniliyorsa Turk hukuk pratiklerine uygun yaz: `abc-alacak-2026`, `is-davasi-yilmaz-2026`, `nda-xyz-2026`.
- Para birimini TL yap.
- Kanun maddelerini kisa referansla yaz: `(HMK m.127)`, `(Av. K. m.36)`, `(KVKK m.11)`, `(TTK m.5/A)`.
- Nihai outputlarda "taslak / avukat incelemesine tabi / hukuki gorus yerine gecmez" sinirini acik tut.

---

## 2. Skill Dosyasi Format Kurali

Her skill dosyasi su frontmatter ile baslamalidir:

```yaml
---
name: skill-slug
description: >
  Kisa aciklama.
user-invocable: true | false
---
```

`YAML` kelimesini basliga veya frontmatter oncesine koyma. Markdown icinde ornek YAML gosterilecekse fenced code block kullan:

```yaml
uyap_no: "2026/123"
```

---

## 3. Türk Maddi Hukuku ve Usul Karşılıkları

ABD / Ingiltere hukukuna ait kavramlari asagidaki Turk hukuk karsiliklariyla degistir:

| Kaynak kavram | Turk hukuk uyarlamasi |
|---|---|
| `FRCP` | HMK (Hukuk Muhakemeleri Kanunu) |
| `complaint` | dava dilekcesi |
| `answer deadline` | cevap dilekcesi suresi (HMK m.127 - tebligattan itibaren 2 hafta; uzatma talep edilebilir) |
| `discovery` | delil ibrazi / belge ibrazi (HMK m.219-220) |
| `legal hold` | delillerin korunmasi / belge saklama talimati; gerekiyorsa delil tespiti (HMK m.400) |
| `subpoena` | celp / bilgi-belge isteme yazisi |
| `injunction` | ihtiyati tedbir (HMK m.389) |
| `attachment` | ihtiyati haciz (IIK m.257) |
| `statute of limitations` | zamanasimi / hak dusurucu sure |
| `consent decree` | sulh / feragat / kabul |
| `damages` | maddi / manevi tazminat |
| `filing` | dava acma / dilekce sunma |
| `motion` | talep / ara karar talebi |
| `brief` | dilekce / savunma / hukuki degerlendirme notu |
| `pleadings stage` | dilekceler asamasi |
| `discovery stage` | on inceleme / tahkikat asamasi |
| `trial` | yargilama / durusma |
| `judgment` | karar / hukum |
| `appeal` | istinaf (BAM) / temyiz (Yargitay veya Danistay) |
| `settlement` | sulh / uzlasma |
| `arbitration` | tahkim (ISTAC, MTO veya ad hoc) |
| `regulatory deadline` | idari basvuru veya itiraz suresi |
| `criminal procedure` | CMK (Ceza Muhakemesi Kanunu) |

---

## 4. Türk Yargı ve İdari Sistem

Mahkeme adlarini su formatta yaz:

```text
[Sehir] [Sira No]. [Tur] Mahkemesi
```

Ornekler:

- Istanbul 3. Asliye Ticaret Mahkemesi
- Ankara 12. Asliye Hukuk Mahkemesi
- Izmir 2. Is Mahkemesi
- Istanbul 1. Agir Ceza Mahkemesi
- Ankara 4. Idare Mahkemesi
- Istanbul 2. Sulh Hukuk Mahkemesi
- Bolge Adliye Mahkemesi / BAM
- Yargitay
- Danistay
- Anayasa Mahkemesi

Idari merciler:

- Rekabet Kurumu
- Kisisel Verileri Koruma Kurumu
- BDDK
- SPK
- EPDK
- BTK
- SGK
- ISKUR
- Ticaret Bakanligi

UYAP kullanilan dava ve icra dosyalarinda `uyap_no` alani ekle. UYAP esas numarasi ornegi:

```yaml
uyap_no: "2026/123 E."
```

---

## 5. Türk Avukatlık Pratiği

### Mesleki Sir ve Gizlilik

ABD'deki `privilege` mantigini birebir tasima. Turk hukukunda daha dogru cerceve:

- avukatin sir saklama yukumlulugu,
- avukatlik sirri / mesleki sir,
- gizli hukuki degerlendirme,
- kontrolsuz paylasim halinde gizlilik ve strateji riski.

Output hedefi sorulurken su mantigi kullan:

> Bu cikti avukatlik sirri veya gizli hukuki degerlendirme kapsaminda olabilir. Hukuk ekibi ve yetkili muvekkil temsilcileri disinda paylasilacaksa, gizli versiyon yerine arindirilmis bir versiyon hazirlayabilirim.

### Cikar Catismasi

- `conflicts check` -> cikar catismasi kontrolu (Av. K. m.38)
- `waived` -> yazili onay / yazili feragat gerekliligi
- Cikar catismasi varsa dosya acma veya devam etme karari avukat tarafindan verilmelidir.

### Vekalet ve Avukat Bilgileri

Gereken dosyalarda su alanlari kullan:

```yaml
muvekkil:
  ad:
  iletisim:
  vekalet_tarihi:
  vekalet_durumu: verildi | beklemede | yok
outside_counsel:
  buro:
  avukat:
  baro_sicil_no:
  email:
```

### Reklam Yasagi

Avukatlik burosu veya avukat icin:

- `business development`,
- `lead generation`,
- soguk arama,
- muvekkil edinmeye donuk otomatik pazarlama,
- teklif gonderme akislari

reklam yasagi ve meslek kurallari bakimindan kaldirilir veya acik bir uyariyla sinirlandirilir (Av. K. m.55).

### Ucret

`contingency fee` kavramini Turk hukukuna otomatik tasima. Avukatlik ucreti icin:

- Avukatlik Asgari Ucret Tarifesi altina inilmemesi,
- dava veya hukum altina alinacak degerin belirli bir yuzdesinin kararlastirilmasinda kanuni sinirlar,
- dava konusu para disindaki mal ve haklarin aynen avukata birakilamamasi,
- yazili ucret sozlesmesi ve ucret mutabakati

kontrol edilir (Av. K. m.164).

---

## 6. KVKK ve Veri Koruma

`GDPR` referanslarini otomatik ve mekanik olarak `KVKK` diye degistirme; konuya gore Turk KVKK rejimini uygula.

Temel karsiliklar:

| Kaynak kavram | Turk hukuk uyarlamasi |
|---|---|
| `GDPR` | KVKK ve ikincil mevzuat |
| `data controller` | veri sorumlusu |
| `data processor` | veri isleyen |
| `DPA` | veri isleme sozlesmesi |
| `DPIA` | Veri Koruma Etki Degerlendirmesi (VKED) |
| `data subject rights` | ilgili kisi haklari (KVKK m.11) |
| `breach notification` | ihlal bildirimi (KVKK m.12; Kurul uygulamasinda en kisa surede ve genel kural olarak 72 saat icinde) |
| `data retention` | saklama ve imha sureleri |

Yurt disina veri aktariminda guncel KVKK m.9 yapisini kullan:

1. Yeterlilik karari var mi?
2. Yeterlilik yoksa uygun guvenceler var mi?
3. Uygun guvence olarak standart sozlesme, baglayici sirket kurallari, taahhutname veya kanundaki diger yollar kullaniliyor mu?
4. Bunlar yoksa aktarim arizi ve istisnai hallerden birine giriyor mu?
5. Acik riza kullaniliyorsa riskler aciklandi mi ve bu surekli aktarim icin tek dayanak haline getiriliyor mu?

NDA, vendor review, DPA, PIA veya AI use-case skill'lerinde ayrica su kontrolu ekle:

```yaml
kvkk:
  kisisel_veri_var: true | false | belirsiz
  ozel_nitelikli_veri_var: true | false | belirsiz
  rol: veri_sorumlusu | veri_isleyen | ortak_sorumluluk | belirsiz
  veri_isleme_sozlesmesi_gerekli: true | false | belirsiz
  yurt_disina_aktarim: true | false | belirsiz
  aktarim_dayanaklari:
    - yeterlilik_karari
    - uygun_guvence
    - standart_sozlesme
    - baglayici_sirket_kurallari
    - taahhutname
    - arizi_istisna
    - acik_riza
```

---

## 7. Arabuluculuk Dava Sarti

Arabuluculuk dava sarti kontrolu eklenirken otomatik ve kesin deadline uretme.

Genel kural:

- Is hukuku uyusmazliklari, ticari davalar, tuketici uyusmazliklari, kira, ortakligin giderilmesi, kat mulkiyeti ve komsu hakki gibi alanlarda dava sartlari ayrica kontrol edilir.
- Dava sartina tabi dosyalarda son tutanak dava dilekcesine eklenmelidir.
- Arabuluculuga basvurudan son tutanaga kadar gecen sure, zamanasimi ve hak dusurucu sure hesabinda dikkate alinmaz veya islemez.
- "Son tutanaktan itibaren 2 hafta" kuralini her dosyaya otomatik yazma. Bu, ozellikle ise iade gibi bazi is hukuku senaryolarinda kullanilir; ticari ve tuketici dosyalarinda ilgili ozel sure ayrica kontrol edilir.

Kullanilacak sema:

```yaml
arabuluculuk:
  dava_sarti: true | false | belirsiz
  dayanak: "TTK m.5/A | 7036 s. Kanun | TKHK | HUAK m.18/A | diger"
  surec_isletildi: true | false | devam-ediyor | belirsiz
  son_tutanak_tarihi: YYYY-MM-DD
  dava_acma_son_tarihi: YYYY-MM-DD | "ozel sure kontrol edilmeli"
  sonuc: anlasmazlik | anlasma | devam-ediyor | belirsiz
  not: "Son tutanak ve ozel dava acma suresi kontrol edilmeden kesin deadline verme."
```

---

## 8. Deliller, Ihtiyati Tedbir ve Ihtiyati Haciz

`legal hold` kavramini tek basina `delil tespiti` diye daraltma.

Turk uygulamasinda uc ayri konu olabilir:

- Delillerin korunmasi ve belge saklama talimati: kurum ici saklama / imha durdurma / belge guvenligi.
- Delil tespiti: mahkemeden tespit talebi (HMK m.400).
- Belge ibrazi: yargilamada karsi taraf veya uc kisiden belge ibrazi (HMK m.219-220).

Uygun dosyalara su alanlari eklenebilir:

```yaml
deliller:
  belge_saklama_talimati: gerekli | verildi | gerek_yok | belirsiz
  delil_tespiti:
    talep_edildi: true | false
    tarih:
    kapsam:
  belge_ibrazi:
    gerekli: true | false | belirsiz
    hedef:
```

---

## 9. Türkçe Hukuki Terimler

### Taraf Sifatlari

| Kaynak kavram | Turkce |
|---|---|
| `plaintiff` | davaci |
| `defendant` | davali |
| `claimant` | talep sahibi / alacakli |
| `respondent` | karsi taraf / borclu |
| `creditor` | alacakli |
| `debtor` | borclu |
| `investigated` | sorusturulan / supheli |

### Kaynak Turu

| Kaynak kavram | Turkce |
|---|---|
| `demand-letter` | ihtarname |
| `complaint-served` | dava dilekcesi tebligi |
| `subpoena` | celp / bilgi-belge isteme yazisi |
| `regulator-inquiry` | idari inceleme / idari sorusturma |
| `internal-report` | ic bildirim |
| `pre-suit-threat` | dava oncesi ihtar / tehdit |
| `enforcement-action` | icra takibi / idari yaptirim sureci |

### Dava Stratejisi

| Kaynak kavram | Turkce |
|---|---|
| `fight` | mucadele / davayi takip |
| `settle` | sulh / uzlasma |
| `investigate` | inceleme / sorusturma |
| `wait` | bekle / izle |

---

## 10. Kaldirilacak veya Donusturulecek ABD'ye Ozgu Yapilar

Tamamen kaldir veya Turk karsiligina donustur:

- ABD mahkeme kisaltmalari (`N.D. Cal.`, `S.D.N.Y.` vb.)
- ABD kurumlari (`FTC`, `SEC`, `DOJ`, `EEOC` vb.)
- ABD burolari (`[ABD hukuk burosu]` vb.)
- `engagement letter` kavramini otomatik silme; gerekiyorsa `avukatlik sozlesmesi`, `is kabul/kapsam yazisi`, `vekaletname durumu` olarak donustur.
- `insurance tender` akisini Turk sigorta ve riziko bildirimi uygulamasi yoksa kaldir.
- `business development / client outreach` akislari avukatlik burosu baglaminda kaldirilir.

Turk ornekleri:

- `Av. [Ad Soyad]`
- `[Buro Adi] Avukatlik Burosu`
- `Istanbul 3. Asliye Ticaret Mahkemesi`
- `Kisisel Verileri Koruma Kurumu`
- `Rekabet Kurumu`

---

## 11. Standart Türk Dosya Alanları

Uygun dava, uyusmazlik veya sozlesme inceleme skill'lerine su alanlari eklenebilir:

```yaml
uyap_no: "2026/123 E. (varsa)"
muvekkil:
  ad:
  iletisim:
  vekalet_tarihi:
  vekalet_durumu: verildi | beklemede | yok
outside_counsel:
  buro:
  avukat:
  baro_sicil_no:
  email:
deliller:
  belge_saklama_talimati: gerekli | verildi | gerek_yok | belirsiz
  delil_tespiti:
    talep_edildi: true | false
    tarih:
    kapsam:
zamanasimi_tarihi:
ihtiyati_tedbir:
  gerekli: true | false | belirsiz
  dayanak: "HMK m.389"
ihtiyati_haciz:
  gerekli: true | false | belirsiz
  dayanak: "IIK m.257"
```

---

## 12. Gizlilik Sozlesmesi (NDA) Skill Ek Kurallari

`commercial-legal/skills/nda-review/SKILL.md` Turk hukukuna uyarlanirken su ek kontroller bulunmalidir.

### Komut ve Klasor Adlari

Repo genelinde plugin yeniden adlandirilmadiysa:

- `/commercial-legal:review` korunur.
- `commercial-legal/CLAUDE.md` korunur.
- Skill adi Turkcelestirilecekse dosya ve marketplace etkisi ayrica kontrol edilir.

Tam Turkcelestirme yapilacaksa bu bir repo-geneli refactor sayilir:

- `commercial-legal` -> `ticari-hukuk`
- `/commercial-legal:review` -> `ticari-hukuk:incele` (varsayımsal hedef ad; canlı komut değildir)
- marketplace kayitlari
- README tablolarindaki komutlar
- hook ve agent referanslari

birlikte guncellenmelidir.

### NDA Kontrol Listesi

Her NDA incelemesinde asagidaki kalemler kontrol edilir:

- gizli bilgi tanimi,
- isaretleme / sozlu aciklama teyidi,
- bilgi kullanma amaci,
- istisnalar,
- iade / imha yukumlulugu,
- yedekleme ve arsiv kopyalari,
- mahkeme veya idari merci talebiyle aciklama,
- sure ve gizlilik yukumlulugunun devam suresi,
- cezai sart ve fahiş cezai sart riski,
- fikri mulkiyet devri veya lisans tuzagi,
- calisan / musteri ayartmama,
- rekabet etmeme veya munhasirlik,
- uygulanacak hukuk ve yetkili mahkeme,
- tahkim sarti,
- KVKK ve veri aktarimi,
- rekabet hukuku hassas bilgi paylasimi,
- imza ve temsil yetkisi.

### KVKK Kontrolu

NDA kapsaminda kisisel veri paylasimi varsa KVKK bolumu ekle:

```yaml
kvkk:
  kisisel_veri_paylasimi: true | false | belirsiz
  ozel_nitelikli_veri: true | false | belirsiz
  veri_isleme_sozlesmesi_gerekli: true | false | belirsiz
  yurt_disina_aktarim: true | false | belirsiz
  not: "KVKK m.9 ve ilgili ikincil mevzuat ayrica kontrol edilmeli."
```

### Rekabet Hukuku Kontrolu

Taraflar rakip veya potansiyel rakipse su kontrolu ekle:

```yaml
rekabet_hukuku:
  rakipler_arasi_paylasim: true | false | belirsiz
  hassas_bilgi:
    fiyat: true | false | belirsiz
    musteri: true | false | belirsiz
    maliyet: true | false | belirsiz
    strateji: true | false | belirsiz
    kapasite: true | false | belirsiz
  not: "Rekabete hassas bilgi paylasimi varsa Rekabet Kurumu uygulamasi acisindan hukukcu incelemesine yonlendir."
```

### Imza ve Temsil Yetkisi

NDA temiz olsa bile imza icin ayri kontrol gerekir:

```yaml
imza:
  imza_yetkilisi_kontrol_edildi: true | false | belirsiz
  imza_sirkuleri_gerekli: true | false | belirsiz
  e_imza_veya_fiziki_imza: e-imza | fiziki | KEP | belirsiz
```

Kapanis aksiyonu NDA icin UYAP'a yonlendirme yapmamalidir. Uygun kapanis ornekleri:

- `CLM uzerinden standart NDA onay akisini baslatin.`
- `Yetkili imzaci ve imza sirkuleri kontrolunden sonra e-imza surecine alin.`
- `Hukuk ekibinin SARI bayraklari onaylamasi halinde imzaya yonlendirin.`

### NDA Output Sinirlari

`What this skill does not do` bolumune sunlari ekle:

- Imza yetkisi vermez.
- Hukuki gorus veya mutalaa yerine gecmez.
- SARI ve KIRMIZI maddelerde nihai karari vermez.
- Yabanci hukuk secimi varsa Turk hukuku varsayimiyla kesin sonuc vermez.
- Karsi tarafa gonderilecek nihai metni avukat onayi olmadan kesinlestirmez.

---

## 13. Sözleşme Tadil Geçmişi Skill Ek Kuralları

`commercial-legal/skills/amendment-history/SKILL.md` Türk hukukuna uyarlanırken amaç, ana sözleşme ile ek protokol, zeyilname ve tadil metinleri arasındaki değişiklik zincirini doğru kurmaktır. Bu skill sözleşmenin tarihçesini çıkarır; nihai yorum, geçerlilik veya üstünlük görüşü vermez.

### Komut ve Klasör Adları

Repo genelinde plugin yeniden adlandırılmadıysa:

- `/commercial-legal:amendment-history` korunur.
- `commercial-legal/CLAUDE.md` korunur.
- `vendor-agreement-review` veya `stakeholder-summary` gibi yönlendirmeler mevcut repo adlarıyla bırakılır.

Tam Türkçeleştirme yapılacaksa bu bir repo-geneli refactor sayılır:

- `amendment-history` -> `sozlesme-tadil-gecmisi`
- `/commercial-legal:amendment-history` -> `ticari-hukuk:sozlesme-tadil-gecmisi` (varsayımsal hedef ad; canlı komut değildir)
- README komut tabloları, marketplace kayıtları ve skill yönlendirmeleri birlikte güncellenmelidir.

### Belge Kaynakları

UYAP bir sözleşme yönetim sistemi değildir. Bu skill'de `uyap_no` yalnızca sözleşme tarihçesi bir dava, icra takibi veya mahkeme dosyasıyla bağlantılıysa kullanılmalıdır.

Varsayılan belge kaynakları:

- doğrudan dosya yükleme,
- CLM / sözleşme yönetim sistemi,
- kurumsal doküman arşivi,
- e-imza platformu,
- KEP yazışmaları,
- fiziki imza nüshaları ve taramaları.

Kaynak alanı için şu yapı kullanılabilir:

```yaml
belge_kaynaklari:
  clm_id:
  arsiv_linki:
  kep_kaydi:
  e_imza_kaydi:
  uyap_no: "yalnızca dava/icra bağlantısı varsa"
```

### Belge Türleri

ABD'deki `amendment`, `addendum`, `side letter` gibi kavramları Türk uygulamasında belge adına göre ayır:

- Ana Sözleşme
- Ek Protokol
- Zeyilname
- Tadil Sözleşmesi
- Devir Sözleşmesi
- Temlik Sözleşmesi
- Fesih Protokolü
- Mutabakat Tutanağı
- Yan Yazı / ek anlaşma

Belge türü belirsizse kesin sınıflandırma yapma; başlık, giriş hükümleri ve imza bloğuna göre "muhtemel belge türü" olarak işaretle.

### Kronoloji ve Geçerlilik Kontrolü

Kronoloji kurulurken şu sırayı izle:

1. İmza tarihi.
2. Yürürlük tarihi.
3. Metin içi "tarihinden itibaren geçerli olmak üzere" ifadeleri.
4. KEP / e-imza zaman damgası.
5. Dosya adı veya arşiv tarihi.

İmza tarihi ile yürürlük tarihi farklıysa ikisini ayrı göster:

```yaml
belge:
  tur: Ek Protokol
  imza_tarihi:
  yururluk_tarihi:
  kaynak:
  siralama_guveni: yuksek | orta | dusuk
```

Sıralama güveni düşükse output başında kullanıcıdan teyit iste:

> Belge sırasını başlık ve dosya tarihlerinden çıkardım; `[belge adı]` için emin değilim. Bu sıralama doğru mu?

### Taraf, Unvan ve Yetki Kontrolü

Her belge için tarafları ve imza bloklarını karşılaştır:

- taraf unvanı değişmiş mi?
- birleşme, devir, bölünme veya ticaret unvanı değişikliği var mı?
- sözleşmenin devri veya alacağın temliki yapılmış mı?
- imza yetkilisi ve temsil yetkisi tutarlı mı?
- kaşe / e-imza / KEP kaydı metinle uyumlu mu?

Uygun çıktı alanı:

```yaml
taraf_kontrolu:
  taraflar_tutarlı: true | false | belirsiz
  unvan_degisikligi: true | false | belirsiz
  devir_veya_temlik: true | false | belirsiz
  imza_yetkisi_kontrol_edildi: true | false | belirsiz
```

### Madde Takibi

Madde takibinde sadece ilgili hükme temas eden belgeleri göster. İlgili hükme dokunmayan ek protokol veya zeyilnameleri listeye doldurma.

Her bulguda kaynak ver:

```text
Fesih (m. 12.3 ana sözleşme; 2 No'lu Ek Protokol m. 4 ile değişik)
```

Madde numarası kaymışsa bunu açıkça belirt:

> Ana sözleşmede m. 9 olan sorumluluk hükmü, 3 No'lu Ek Protokol'de m. 8.2 olarak yeniden numaralandırılmış görünüyor.

### Çelişki ve Üstünlük

Ana sözleşme ile zeyilname arasında çelişki varsa skill kesin hukuki mütalaa vermemelidir. Bunun yerine:

- çelişkiyi tarif et,
- hangi belgelerin hangi maddeleri arasında olduğunu göster,
- sözleşmede "öncelik sırası / üstünlük" hükmü var mı kontrol et,
- yoksa hukukçu incelemesine yönlendir.

Kullanılacak ifade:

> Bu iki hüküm arasında potansiyel çelişki var. Hangi hükmün üstün geleceği sözleşmenin yorumuna ve varsa öncelik sırası maddesine bağlıdır; hukukçu incelemesine yönlendirilmelidir.

### Türkiye'ye Özgü Risk Başlıkları

Tadil geçmişi çıkarılırken şu başlıklar ayrıca izlenmelidir:

- cezai şart ve fahiş cezai şart riski,
- temerrüt faizi ve ticari faiz,
- ödeme vadeleri ve kur farkı,
- damga vergisi etkisi,
- KDV ve stopaj etkisi,
- süre uzatımı ve otomatik yenileme,
- fesih ve ihbar süreleri,
- yetkili mahkeme / icra dairesi,
- tahkim şartı,
- KVKK ve veri işleme hükümleri,
- fikri mülkiyet lisansı veya devir hükümleri,
- rekabet yasağı / münhasırlık / müşteri veya çalışan ayartmama,
- teminat, kefalet, garanti ve teminat mektubu değişiklikleri.

### Output Sınırları

`What this skill does not do` bölümüne şunları ekle:

- Hangi belgenin kesin olarak üstün geleceğine dair hukuki mütalaa vermez.
- Yeni ek protokol veya zeyilname taslağı hazırlamaz.
- Sözleşmenin güncel halinin tam risk incelemesini yapmaz; bunun için sözleşme inceleme skill'ine yönlendirir.
- Damga vergisi, vergi, muhasebe veya finansal etki hesabını kesinleştirmez; yalnızca kontrol edilmesi gereken alanları işaretler.
- Eksik veya imzasız belgeye dayanarak kesin güncel metin oluşturmaz.

---

## 14. Profil Özelleştirme Skill Ek Kuralları

`commercial-legal/skills/customize/SKILL.md` Türk hukukuna uyarlanırken amaç, kullanıcının tüm başlangıç mülakatını tekrar yapmadan ticari hukuk profilindeki tekil ayarları güvenli şekilde değiştirmesidir.

### Komut ve Klasör Adları

Repo genelinde plugin yeniden adlandırılmadıysa:

- `/commercial-legal:customize` korunur.
- `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` korunur.
- `company-profile.md` yerine `sirket-profili.md` gibi adlar ancak repo genelinde karşılığı güncellenmişse kullanılmalıdır.

Tam Türkçeleştirme yapılacaksa:

- `customize` -> `ozellestir`
- `/commercial-legal:customize` -> `ticari-hukuk:ozellestir` (varsayımsal hedef ad; canlı komut değildir)
- README, marketplace, hook ve skill yönlendirmeleri birlikte değiştirilmelidir.

### Özelleştirilebilir Alanlar

Türk hukuk pratiği için gösterilecek profil haritası şu alanları kapsamalıdır:

- şirket / müvekkil kimliği,
- hukuk müşavirliği mi hukuk bürosu mu olduğu,
- yetki alanları ve çalışma şehirleri,
- risk tutumu,
- onay ve imza yetkisi matrisi,
- ticari sözleşme playbook pozisyonları,
- GS / NDA tasnif tercihleri,
- KVKK ve veri aktarımı tercihleri,
- cezai şart, sorumluluk sınırı, fesih, yenileme ve fiyat revizyonu pozisyonları,
- yetkili mahkeme / tahkim tercihleri,
- çıktı dili ve üslubu,
- KEP, e-imza, CLM, arşiv ve belge depolama entegrasyonları.

`baro bölgesi` yalnızca avukat veya hukuk bürosu profillerinde anlamlıdır. Şirket içi hukuk müşavirliği profillerinde `baro` yerine şirket merkezi, yetki alanı ve faaliyet şehirleri sorulmalıdır.

### Guardrail Değişiklikleri

Kullanıcı şu korumaları kapatmak isterse doğrudan kapatma:

- avukat incelemesi uyarısı,
- mesleki sır / gizli hukuki değerlendirme başlığı,
- kaynak ve kanun maddesi doğrulama notları,
- `[verify]`, `[incele]`, `[avukat onayı gerekir]` gibi güvenlik etiketleri,
- çıkar çatışması ve yetki kontrolü hatırlatmaları.

Bunun yerine değişikliğin neyi zayıflatacağını açıkla ve daha dar bir alternatif öner:

> Bu koruma hukuki riskleri görünür tutmak için kullanılıyor. Tamamen kaldırmak yerine yalnızca iç ekip özetlerinde daha kısa bir uyarı formatı kullanabilirim.

### Değişiklik Kaydı

Profil değişiklikleri ileride hangi playbook'un uygulandığını anlamak için kayda bağlanmalıdır:

```yaml
profil_degisiklik_kaydi:
  tarih:
  degistiren:
  degisen_alan:
  onceki_deger:
  yeni_deger:
  etkilenen_skilller:
  not:
```

### Bu Skill Ne Yapmaz

- Yeni hukuki pozisyonu kendisi icat etmez; kullanıcıdan veya yetkili hukukçudan alır.
- Avukatlık meslek kurallarını zayıflatan bir ayarı sessizce kabul etmez.
- Tüm başlangıç mülakatını yeniden çalıştırmaz.
- Birden fazla köklü değişikliği tek onayla yazmaz.

---

## 15. Eskalasyon ve Onay Skill Ek Kuralları

`commercial-legal/skills/escalation-flagger/SKILL.md` Türk hukukuna uyarlanırken amaç, sözleşme veya işlem riskini doğru onay makamına yönlendirmek ve gönderilmeye hazır fakat otomatik gönderilmeyen bir talep taslağı üretmektir.

### Onay Matrisi

Tutarlar TL cinsinden yazılmalı, eşikler açık olmalıdır:

```yaml
eskalasyon_matrisi:
  - onay_yetkisi: "Sözleşme Avukatı"
    esik: "standart maddeler / 1.000.000 TL altı"
    eskalasyon_makami: "Kıdemli Avukat"
    kanal: "Teams / e-posta"
  - onay_yetkisi: "Hukuk Müşaviri"
    esik: "standart dışı maddeler / 10.000.000 TL altı"
    eskalasyon_makami: "Genel Müdür veya Yönetim Kurulu"
    kanal: "resmi onay notu"
```

Onay makamı belirsizse "hukuk yönetimi" gibi genel ifadelerle yetinme; isim veya rol sor.

### Otomatik Eskalasyon Tetikleyicileri

Türk ticari uygulamasında şu başlıklar otomatik eskalasyon adayıdır:

- sınırsız sorumluluk,
- cezai şart veya fahiş cezai şart riski,
- FSEK / fikri mülkiyet devri,
- KVKK veya yurt dışına veri aktarımı riski,
- rekabet yasağı, münhasırlık veya müşteri/çalışan ayartmama,
- tahkim veya yabancı hukuk seçimi,
- yetkili mahkeme dışı forum,
- teminat, kefalet, garanti veya teminat mektubu,
- ödeme, kur farkı, fiyat artışı veya ticari faiz riski,
- imza yetkisini veya şirket içi temsil sınırını aşan işlem.

### Karar ve Gönderim Sınırı

Bu skill:

- hiçbir şeyi kendi başına onaylamaz,
- talebi otomatik göndermez,
- onaylayıcı yerine karar vermez,
- yalnızca tavsiye ve seçenek hazırlar.

Onay taslağı profesyonel ve kayda geçirilebilir olmalıdır. Hukuk bürosu bağlamında karşı tarafa doğrudan gönderilecek metin üretilecekse avukat onayı ayrıca aranmalıdır.

### Kayıt ve İzlenebilirlik

Eskalasyon yapıldıysa inceleme notuna veya dosya tarihçesine şu kayıt önerilir:

```yaml
eskalasyon:
  konu:
  onay_makami:
  kanal:
  karar_beklenen_tarih:
  durum: taslak | gonderildi | onaylandi | reddedildi | revizyon_istendi
  karar:
  tarih:
```

### Bu Skill Ne Yapmaz

- Onay makamı yerine karar vermez.
- İmza yetkisi yaratmaz.
- Yönetim kurulu, genel kurul veya şirket içi imza sirküleri gerekliliklerini ortadan kaldırmaz.
- Mesajı otomatik göndermez.

---

## 16. Dosya Çalışma Alanı Skill Ek Kuralları

`commercial-legal/skills/matter-workspace/SKILL.md` Türk hukukuna uyarlanırken amaç, birden fazla müvekkil veya dosya ile çalışan kullanıcılarda bağlam sızıntısını önlemektir.

### Komut ve Klasör Adları

Repo genelinde plugin yeniden adlandırılmadıysa:

- `/commercial-legal:matter-workspace` korunur.
- `matters/`, `matter.md`, `history.md`, `notes.md` korunur.

Tam Türkçeleştirme yapılacaksa:

- `matter-workspace` -> `dosya-alani`
- `matters/` -> `dosyalar/`
- `matter.md` -> `dosya.md`
- `history.md` -> `tarihce.md`
- bu değişiklik tüm skill referanslarıyla birlikte yapılmalıdır.

### Dosya Açılış Alanları

Yeni dosya açarken şu alanlar Türk pratiğine göre eklenebilir:

```yaml
dosya:
  slug:
  muvekkil:
  karsi_taraf:
  dosya_turu:
  uyap_no: "varsa"
  vekalet_durumu: verildi | beklemede | yok
  cikar_catismasi_kontrolu: yapildi | beklemede | kapsam_disi
  arabuluculuk:
    dava_sarti: true | false | belirsiz
    surec_isletildi: true | false | devam-ediyor | belirsiz
  gizlilik: standart | yüksek | mesleki_sir_kisitli
  zamanasimi_tarihi:
  hak_dusurucu_sure:
```

`uyap_no` her dosyada zorunlu değildir. Sözleşme, danışmanlık, KVKK, ürün veya ticari işlem dosyalarında UYAP dosyası yoksa `yok` veya `dava bağlantısı yok` yazılmalıdır.

### Çıkar Çatışması ve Vekalet

Bu skill çıkar çatışması kontrolünü yapmaz; yalnızca durumunu kaydeder. Hukuk bürosu bağlamında:

- karşı taraf,
- ilişkili taraflar,
- grup şirketleri,
- önceki müvekkiller,
- aynı olayla bağlantılı kişiler

ayrı kontrol gerektirir (Av. K. m.38).

### Cross-Matter Gizlilik

`Cross-matter context` kapalıysa başka dosya klasörü okunmaz. Açık olsa bile başka dosya bilgisi yalnızca kullanıcı açıkça karşılaştırma istediğinde okunmalıdır.

Dosya kapatma silme değildir. Arşivlenen dosyalar saklama, çıkar çatışması ve mesleki sorumluluk sebepleriyle okunabilir kalır; imha politikası ayrıca belirlenmelidir.

### Bu Skill Ne Yapmaz

- Çıkar çatışması kontrolü yerine geçmez.
- Saklama veya imha politikası uygulamaz.
- Başka dosya bağlamını kendiliğinden kullanmaz.
- Hukuki strateji belirlemez; sadece dosya bağlamını izole eder.

---

## 17. Sözleşme Yenileme ve Fesih Takibi Skill Ek Kuralları

`commercial-legal/skills/renewal-tracker/SKILL.md` ve `renewal-register.yaml` Türk hukukuna uyarlanırken amaç, otomatik yenileme ve fesih ihbar sürelerinin kaçırılmasını önlemektir.

### Kayıt Defteri Alanları

Kayıt defteri TL ve Türk bildirim yöntemleriyle tutulmalıdır:

```yaml
renewals:
  - karsi_taraf:
    sozlesme:
    imza_tarihi:
    ilk_donem_bitis:
    mevcut_donem_bitis:
    yenileme_mekanizmasi:
    ihbar_suresi_gun:
    ihbar_yontemi: noter | kep | iadeli_taahhutlu_posta | e-posta | sozlesmede_belirtilen
    gonderim_tampon_gun:
    ihbar_son_takvim_tarihi:
    ihbar_son_is_gunu:
    en_gec_gonderim_tarihi:
    hesaplama_notu:
    fiyat_artisi:
    yillik_deger_tl:
    is_birimi_sahibi:
    clm_id:
    uyap_no: "yalnızca dava/icra bağlantısı varsa"
    durum: aktif | feshedildi | yenilendi | suresi_gecti
    notlar:
```

### Bildirim Yöntemi

Tacirler arasındaki temerrüt, fesih ve sözleşmeden dönme ihbarlarında TTK m.18/3 ayrıca kontrol edilmelidir. Türk uygulamasında tipik yöntemler:

- noter,
- taahhütlü / iadeli taahhütlü posta,
- telgraf,
- güvenli elektronik imzalı KEP,
- sözleşmede geçerli kabul edilen e-posta veya portal bildirimi.

Sözleşme bildirim maddesi, TTK m.18/3 ve uygulamadaki ispat ihtiyacı birlikte değerlendirilmelidir. E-posta tek başına ancak sözleşme ve olay özelinde güvenli kabul ediliyorsa not düşülmelidir.

### Tarih Hesabı

Yenileme takibi iki tarih ayrımı yapmalıdır:

- `ihbar_son_takvim_tarihi`: ham matematiksel tarih.
- `en_gec_gonderim_tarihi`: bildirim yöntemine göre güvenli gönderim tarihi.

Hafta sonu ve resmi tatil hesabında otomatik kesin hüküm verme. TBK m.93 genel olarak son gün tatile rastlarsa izleyen ilk iş gününe geçeceğini söyler; ancak yenilemeyi kaçırmamak için tracker risk azaltıcı şekilde daha erken gönderim uyarısı verebilir. Bu fark outputta açıkça yazılmalıdır:

> Hukuki son gün hesabı ile risk azaltıcı gönderim tarihi farklı olabilir. Sözleşmedeki bildirim maddesi ve uygulanacak hukuk kontrol edilmeden kesin son tarih olarak kullanılmamalıdır.

### Uyarı Mantığı

Uyarılar `en_gec_gonderim_tarihi` üzerinden çalışmalıdır:

- Kırmızı: 0-13 gün
- Turuncu: 14-44 gün
- Sarı: 45-89 gün

Sınır günleri tek bir gruba dahil edilmelidir. Aynı sözleşme iki grupta görünmemelidir.

### Avukat Onayı ve İş Birimi Kararı

Yenileme takibi araştırmadır; fesih ihbarı göndermek, göndermemek veya yenilemeyi kabul etmek hukuki sonuç doğurur. Kullanıcı avukat değilse şu kapı korunmalıdır:

> Bu işlem sözleşmeyi sona erdirebilir veya şirketi yeni bir dönem için borç altına sokabilir. Şirket avukatı veya yetkili hukukçu ile görüştünüz mü?

### Bu Skill Ne Yapmaz

- Sözleşmeyi kendisi feshetmez.
- Yenilemeye karar vermez.
- Fesih ihbarını otomatik göndermez.
- Sözleşme bildirim maddesini okumadan kesin deadline üretmez.
- Vergi, muhasebe veya bütçe etkisini kesin hesaplamaz.

---

## 18. Sözleşme İnceleme Router Skill Ek Kuralları

`commercial-legal/skills/review/SKILL.md` Türk hukukuna uyarlanırken bu skill'in esas görevi, gelen belgeyi doğru alt inceleme skill'ine yönlendirmek ve çıktıları tek raporda birleştirmektir.

### Router Mantığı

Belge başlıkları, içerik ve taraf ilişkisine göre şu alt skill'lere yönlendirme yapılır:

- Gizlilik Sözleşmesi / NDA -> `nda-review`
- Tedarikçi sözleşmesi / hizmet sözleşmesi / MSA -> `vendor-agreement-review`
- SaaS / abonelik / bulut hizmeti -> `saas-msa-review`
- Ek protokol / zeyilname / tadil metni -> `amendment-history`
- Yenileme veya fesih ihbar tarihi -> `renewal-tracker`

Belge birden fazla kategoriye giriyorsa kullanıcıya kısa yönlendirme onayı sor. `confirm_routing` varsayılanı `true` olmalıdır.

### UYAP ve Belge Kaynağı

`UYAP No` sözleşme inceleme için varsayılan kaynak değildir. Yalnızca sözleşme bir dava, icra takibi veya mahkeme dosyasıyla bağlantılıysa kullanılır. Aksi halde belge kaynakları CLM, e-imza, KEP, kurumsal arşiv, Drive/SharePoint veya doğrudan yüklemedir.

### Birleşik Rapor

Birden fazla alt skill çalıştıysa birleşik raporda:

- hangi alt skill'in çalıştığı,
- hangi hukuk varsayımının uygulandığı,
- hangi konuların avukat incelemesine kaldığı,
- hangi outputların kaynak alındığı

açıkça belirtilmelidir.

---

## 19. SaaS ve Abonelik Sözleşmesi Skill Ek Kuralları

`commercial-legal/skills/saas-msa-review/SKILL.md` Türk hukukuna uyarlanırken SaaS ve abonelik sözleşmelerinin yenileme, fiyat artışı, veri, çıkış ve hizmet seviyesi riskleri ayrı katman olarak incelenmelidir.

### Türk Hukuku Kontrol Katmanı

SaaS incelemesinde şu alanlar ayrıca kontrol edilir:

- otomatik yenileme ve fesih ihbar süresi,
- fiyat artışı, kur farkı, TÜFE/ÜFE ve tek taraflı fiyat değişikliği,
- KDV, stopaj veya fatura düzeni etkisi,
- hizmet seviyesi, kesinti, bakım penceresi ve kredi mekanizması,
- veri taşınabilirliği ve çıkış yardımı,
- KVKK rol ayrımı: veri sorumlusu / veri işleyen,
- alt veri işleyenler ve yurt dışına aktarım,
- veri lokasyonu ve erişim yetkileri,
- yapay zeka / makine öğrenmesi için veri kullanımı,
- fikri mülkiyet ve kullanım verisi hakları,
- denetim, log, güvenlik ve ihlal bildirimi,
- uygulanacak hukuk, yetki ve tahkim.

### Renewal Handoff

Otomatik yenileme veya fesih ihbar süresi tespit edilirse `renewal-tracker` için kayıt üret:

```yaml
yenileme_handoff:
  karsi_taraf:
  sozlesme:
  mevcut_donem_bitis:
  ihbar_suresi_gun:
  ihbar_yontemi:
  fiyat_artisi:
  yillik_deger_tl:
  not:
```

### AI ve Veri Kullanımı

SaaS sağlayıcısının müşteri verilerini model eğitimi, ürün iyileştirme, analitik veya benchmark için kullanıp kullanmadığı açıkça işaretlenmelidir. Belirsizlik varsa SARI veya eskalasyon adayıdır.

---

## 20. Tedarikçi Sözleşmesi İnceleme Skill Ek Kuralları

`commercial-legal/skills/vendor-agreement-review/SKILL.md` Türk hukukuna uyarlanırken amaç, tedarikçi sözleşmesini playbook'a göre incelemek, sapmaları işaretlemek ve gerekiyorsa redline metni üretmektir.

### Ön Kontroller

İnceleme başlamadan önce:

- taraf ve rol: alıcı / müşteri mi, tedarikçi / satıcı mı?
- sözleşme türü,
- sözleşme bedeli ve TL karşılığı,
- imza ve temsil yetkisi,
- uygulanacak hukuk ve yetki,
- KVKK ve veri aktarımı,
- rekabet hukuku hassasiyeti,
- otomatik yenileme ve fesih,
- cezai şart, teminat, kefalet, garanti,
- damga vergisi veya vergi kontrol ihtiyacı

çıkarılmalıdır.

### Deal-Breaker Adayları

Türk uygulamasında tipik kırmızı bayraklar:

- sınırsız veya kontrolsüz sorumluluk,
- tek taraflı ve fahiş cezai şart,
- fikri mülkiyet devri veya geniş lisans,
- KVKK m.9 kontrolü yapılmadan yurt dışı aktarım,
- belirsiz fiyat artışı veya tek taraflı ücret değişikliği,
- ağır ve belirsiz hizmet seviyesi yaptırımları,
- münhasırlık / rekabet yasağı,
- yabancı hukuk ve yabancı yetki seçimi,
- tahkim hükmü ama kurum, yer veya dil belirsizliği,
- teminat mektubu, kefalet veya garanti kapsamının belirsizliği.

### Redline Sınırı

Revizyon önerileri küçük ve uygulanabilir olmalıdır. Yeni hukuki yapı kuran geniş değişikliklerde:

> Bu madde sözleşmenin risk dağılımını değiştirdiği için hukukçu tarafından yeniden kaleme alınmalıdır.

---

## 21. İş Birimi Özet Raporu Skill Ek Kuralları

`commercial-legal/skills/stakeholder-summary/SKILL.md` Türk hukukuna uyarlanırken amaç, avukat incelemesini hukukçu olmayan iş birimi için okunabilir bir karar özetine çevirmektir.

### Hedef ve Gizlilik

Raporun hedef kitlesi sorulmalıdır:

- satın alma,
- satış,
- finans,
- ürün,
- yönetim,
- karşı tarafla paylaşılacak arındırılmış metin.

Mesleki sır veya gizli hukuki değerlendirme içeren kısımlar hukuk dışı geniş dağıtıma çıkarılmamalıdır. Gerekirse iki versiyon hazırlanır:

- hukuk ekibi için tam versiyon,
- iş birimi için arındırılmış aksiyon versiyonu.

### Format

İş birimi özeti kısa olmalıdır:

- karar cümlesi,
- en önemli 3 risk,
- yapılacaklar,
- onay gereken kişi,
- son tarih,
- "imzalanabilir mi?" cevabı.

Hukuki mütalaa dili kullanılmamalı; ancak hukuki risk görünmez hale getirilmemelidir.

---

## 22. Litigation Başlangıç Mülakatı Skill Ek Kuralları

`litigation-legal/skills/cold-start-interview/SKILL.md` Türk hukukuna uyarlanırken mülakat rol, taraf ve yargı yolu bazlı dallanmalıdır.

### Rol Dallanması

Temel roller:

- hukuk müşaviri,
- hukuk bürosu avukatı,
- serbest avukat,
- stajyer avukat / yardımcı hukuk personeli,
- klinik veya eğitim kullanıcısı.

### Taraf ve Yargı Yolu

Taraf:

- davacı,
- davalı,
- alacaklı,
- borçlu,
- üçüncü kişi,
- şikayetçi / mağdur,
- şüpheli / sanık.

Yargı yolu:

- hukuk,
- ticaret,
- iş,
- tüketici,
- idare,
- icra,
- ceza,
- tahkim,
- arabuluculuk.

### Türkiye Entegrasyonları

Mülakat şu kaynak ve araçların durumunu kaydetmelidir:

- UYAP,
- e-tebligat / UETS,
- KEP,
- e-imza,
- Yargıtay / Danıştay / Anayasa Mahkemesi karar kaynakları,
- mevzuat kaynağı,
- ofis belge arşivi.

---

## 23. Dilekçe Bölümü Hazırlayıcı Skill Ek Kuralları

`litigation-legal/skills/brief-section-drafter/SKILL.md` Türk hukukuna uyarlanırken output "brief" değil, dilekçe bölümü veya savunma bölümü taslağıdır.

### Bölüm Türleri

Tipik bölümler:

- maddi vakıalar,
- usuli itirazlar,
- hukuki nedenler,
- deliller,
- açıklamalar,
- talep ve sonuç,
- ihtiyati tedbir / ihtiyati haciz talebi,
- istinaf / temyiz nedeni.

### Delil Sadakati

Her vakıa somut delile bağlanmalıdır. Tanık beyanları için tanık adına yapay anlatı üretilmemeli; tanık delili HMK m.240 vd. çerçevesinde dikkatli işaretlenmelidir.

### Zayıf Argümanlar

Zayıf veya doğrulanmamış argümanlar gizlenmemeli; taslak notlarında "doğrulanmalı", "riskli", "içtihat kontrolü gerekli" olarak işaretlenmelidir.

---

## 24. Kronoloji ve Vaka Takibi Skill Ek Kuralları

`litigation-legal/skills/chronology/SKILL.md` Türk hukukuna uyarlanırken amaç, delillerden tarihli olayları çıkarıp dava teorisine göre önemlendirmektir.

### Kaynak ve KVKK

Kronoloji kaynakları:

- dilekçeler,
- ihtarnameler,
- sözleşmeler,
- e-posta / KEP,
- tutanaklar,
- UYAP evrakı,
- tanık notları,
- bilirkişi raporu,
- ödeme ve fatura kayıtları.

Kişisel veri ve özel nitelikli veri varsa KVKK uyarısı eklenmelidir. Gereksiz kişisel veri işlenmemeli, hassas bilgiler sınırlı erişimle tutulmalıdır.

### Output Türleri

- çalışma kronolojisi,
- maddi vakıa listesi,
- tanık hazırlık kronolojisi,
- dava teorisi için kritik olaylar,
- eksik delil ve doğrulama listesi.

Her olayda tarih, kaynak, güven seviyesi ve önem etiketi bulunmalıdır.

---

## 25. İstem ve Unsur Tablosu Skill Ek Kuralları

`litigation-legal/skills/claim-chart/SKILL.md` Türk hukukuna uyarlanırken "claim chart" iki farklı modda ele alınmalıdır: patent istem tablosu ve hukuk davası unsur tablosu.

### Patent Modu

Patent modunda:

- istem numarası,
- teknik unsur,
- karşı ürün / yöntem karşılığı,
- delil,
- eksik veya tartışmalı unsur,
- tecavüz veya hükümsüzlük modu

ayrılır. Teknik ve hukuki kanaat nihai görüş gibi sunulmaz.

### Hukuk Davası Modu

Hukuk modunda kanuni unsurlar delillerle eşleştirilir:

- sözleşmeye aykırılık,
- haksız fiil,
- sebepsiz zenginleşme,
- işçilik alacağı,
- ticari alacak,
- marka / telif / haksız rekabet.

Her unsur için delil, kaynak, ispat boşluğu ve karşı taraf savunması ayrı gösterilir.

### CSV / Excel Güvenliği

Tablo CSV veya Excel'e aktarılıyorsa formül enjeksiyonu riski için `=`, `+`, `-`, `@` ile başlayan hücreler güvenli hale getirilmelidir.

---

## 26. İhtarname Ön Hazırlık Skill Ek Kuralları

`litigation-legal/skills/demand-intake/SKILL.md` Türk hukukuna uyarlanırken amaç, ihtarname taslağı öncesi stratejik ve maddi vakıa bilgilerini toplamaktır.

### Hazırlık Soruları

Her zaman sorulacak temel alanlar:

- gönderen / muhatap,
- ilişki ve hukuki dayanak,
- tetikleyici olay,
- talep,
- süre,
- deliller,
- daha önceki yazışmalar,
- hedeflenen duruş: mücadele / uzlaşma / soruşturma / bekle.

Önemli dosyalarda ayrıca:

- ikrar riski,
- ibra / feragat riski,
- arabuluculuk veya sulh görüşmeleri,
- zamanaşımı / hak düşürücü süre,
- gönderim yöntemi: noter / KEP / iadeli taahhütlü,
- ihtardan sonra açılabilecek dava veya icra yolu

sorulmalıdır.

---

## 27. İhtarname Taslaklama Skill Ek Kuralları

`litigation-legal/skills/demand-draft/SKILL.md` Türk hukukuna uyarlanırken output noter veya KEP ile gönderilebilecek ihtarname taslağına uygun olmalıdır.

### Taslak Öncesi Kapı

Taslaklamadan önce kullanıcı şu riskleri onaylamalıdır:

- mesleki sır,
- ikrar riski,
- feragat / ibra riski,
- zamanaşımı veya hak düşürücü süre,
- arabuluculuk ve sulh görüşmeleri gizliliği,
- üslup ve maddi vaka doğruluğu,
- gönderim yöntemi.

### Türk Noter / KEP Yapısı

Tipik yapı:

- ihtar eden,
- muhatap,
- konu,
- açıklamalar,
- hukuki dayanak,
- talep ve verilen süre,
- aksi halde başvurulacak yollar,
- delil ve ekler,
- tarih ve imza.

Taslak `.docx` üretilecekse belge ayrıca görsel/biçimsel kontrole tabi tutulmalıdır.

---

## 28. Gelen İhtarname Analizi Skill Ek Kuralları

`litigation-legal/skills/demand-received/SKILL.md` Türk hukukuna uyarlanırken amaç, gelen ihtarı okumak, süre ve riskleri çıkarmak, cevap seçeneklerini hazırlamak ve gerekiyorsa yeni dosya açmaktır.

### Analiz Adımları

1. İhtarnameyi oku ve tarafları çıkar.
2. Tebliğ veya öğrenme tarihini tespit et.
3. Verilen süreyi ve son günü hesapla.
4. Portföyde ilişkili dosya var mı kontrol et.
5. İddia edilen vakıaları ve hukuki dayanakları ayır.
6. Delil ve ispat boşluklarını işaretle.
7. Cevap seçeneklerini hazırla: esaslı cevap, karşı ihtar, uzlaşma, sessiz kalma, dava/icra hazırlığı.

### Süre Uyarısı

Tebliğ tarihi belirsizse kesin deadline üretme. "Tebliğ tarihi doğrulanmalı" uyarısı ver. Sürenin noter, KEP veya posta kaydına göre başladığı ayrıca kontrol edilmelidir.

---

## 29. Output Kurallari

- "What this skill does NOT do" bolumunu Turkce yaz.
- Onay ve confirm mesajlarini Turkce yaz.
- Temiz dosyalarda gereksiz uzun rapor uretme.
- Hukuki risk derecelendirmesinde renkleri sadece yardimci sinyal olarak kullan; gerekceyi mutlaka yaz.
- Alinti yapiliyorsa kisa alinti kullan ve madde numarasi belirt.
- Eksik bilgi varsa kesin hukuki sonuc verme; `belirsiz`, `kontrol edilmeli`, `avukat incelemesine yonlendir` ifadelerini kullan.
- Dava veya idari basvuru deadline'i uretmeden once dayanak, teblig tarihi, son tutanak, ozel kanun ve tatil/hafta sonu etkisini kontrol et.

---

## 30. Kaynak Notlari

Bu rehber operasyonel bir uyarlama standardidir. Hukuki kaynaklar degisebilir. Ozellikle KVKK yurt disina aktarim, arabuluculuk dava sarti, avukatlik ucreti, reklam yasagi, dava sureleri ve idari basvuru sureleri uygulanmadan once guncel mevzuat ve resmi kaynaklardan kontrol edilmelidir.
