# Claude Legal Turkish

Claude Legal Turkish, Anthropic'in açık kaynaklı **Claude for Legal** yapısını temel alan Türkiye uyarlamasıdır. Amaç, aynı plugin/skill iskeletini koruyarak hukuki içerikleri Türk hukuku, Türkiye yargı sistemi ve yerel regülasyonlar ekseninde çalışır hale getirmektir.

Bu repo; hukuk departmanları, avukatlar, uyum ekipleri ve hukuk operasyonları için sözleşme inceleme, dava/uyuşmazlık takibi, KVKK, iş hukuku, ürün hukuku, şirketler hukuku ve regülasyon izleme iş akışlarına yönelik Claude Code plugin'leri içerir.

> Önemli: Bu proje hukuki danışmanlık vermez. Üretilen her çıktı avukat/hukukçu incelemesine tabi taslak, araştırma notu veya karar destek çıktısıdır. Kanun, içtihat, süre, tebliğ, yetki, imza ve resmi kaynak kontrolleri somut dosya için ayrıca doğrulanmalıdır.

## Tasarım Kararı

Operasyonel adlar orijinal repo ile uyumlu tutulur:

- Plugin klasörleri: `commercial-legal`, `litigation-legal`, `privacy-legal` vb.
- Komutlar: `/commercial-legal:review`, `/regulatory-legal:reg-feed-watcher` vb.
- Dosya adları: `SKILL.md`, `CLAUDE.md`, `.mcp.json`, `.claude-plugin/plugin.json`

Türkçeleştirme; hukuki içerikte, kontrol listelerinde, çıktı şablonlarında, örneklerde ve kaynak/kavram katmanında yapılır. Komut adlarını `/ticari-hukuk:*` gibi Türkçeleştirmek ayrı bir repo-geneli refactor işidir.

## Durum Özeti

| Alan | Durum | Not |
|---|---|---|
| `commercial-legal` | İlk tur tamamlandı | NDA, tedarikçi, SaaS/abonelik, yenileme, tadil, eskalasyon ve dosya çalışma alanı Türk ticari sözleşme pratiğine uyarlandı. |
| `corporate-legal` | İlk tur tamamlandı | TTK, SPK/KAP/MKK, MERSİS, Ticaret Sicili, M&A diligence ve kapanış iş akışları işlendi; bazı yardımcı dosyalarda ikinci tur polish yapılabilir. |
| `litigation-legal` | İlk tur tamamlandı / kararlı | HMK, CMK, UYAP/UETS, noter/KEP ihtarname, delil tespiti, müzekkere, istinaf/temyiz ve Av.K. m.36 gizlilik akışları işlendi. |
| `privacy-legal` | İlk tur tamamlandı | KVKK, Kurul kararları, VERBİS, aydınlatma/açık rıza, yurt dışına aktarım, veri ihlali ve ilgili kişi başvuruları merkeze alındı. |
| `employment-legal` | İlk tur tamamlandı | İş Kanunu, SGK, İŞKUR, İSG, fesih, işçilik alacakları, zorunlu arabuluculuk, izin ve iç soruşturma akışları işlendi. |
| `product-legal` | İlk tur tamamlandı | 6502, 6563, Reklam Kurulu, KVKK, İYS/çerez, ürün güvenliği, sektör regülatörleri ve AI/otomasyon kapıları işlendi. |
| `regulatory-legal` | İlk tur tamamlandı | Resmi Gazete, Mevzuat Bilgi Sistemi, KVKK, Rekabet, SPK, BDDK, BTK, EPDK, TCMB, Ticaret Bakanlığı, MASAK ve sektör kaynakları işlendi. |
| `managed-agent-cookbooks` | İlk tur tamamlandı | Reg monitor, docket watcher, launch radar, renewal watcher ve diligence grid cookbook'ları Türk kaynak mantığına göre güncellendi. |
| `legal-builder-hub` | Kısmen uyarlanmış meta araç | Skill kurulum/QA yapısı korunur; Legal Turkish isim/path stabilitesi kontrolü eklendi. |
| `ip-legal` | Kısmen uyarlanmış | README/CLAUDE ve bazı skill'ler FSEK, SMK, TÜRKPATENT, WIPO, uyar-kaldır ve tecavüzün men'i eksenine çekildi; bazı skill'lerde US/DMCA/USPTO kalıntıları temizlenecek. |
| `ai-governance-legal` | Kısmen uyarlanmış | Vendor AI review ve use-case triage KVKK/FSEK/TTK ticari sır katmanı aldı; AIA/reg-gap/policy çekirdeğinde EU/US kalıntıları temizlenecek. |
| `law-student` | Kapsam dışı | ABD hukuk eğitimi/bar prep modeli Türk sistemle doğrudan uyumlu olmadığı için uyarlanmayacak. |
| `legal-clinic` | Ayrık / kapsam dışı | US law school clinic modeli Türkiye'de doğrudan karşılığı olmayan ayrı bir yapı olduğu için Legal Turkish çekirdeğine çevrilmeyecek. |
| `cocounsel-legal` | Harici | Westlaw/Practical Law odaklı üçüncü taraf plugin; Türk hukuku çıktısı gibi kabul edilmemelidir. |

Ayrıntılı takip için: [TURKISH_ADAPTATION_STATUS.md](TURKISH_ADAPTATION_STATUS.md)

## Kurulum

Claude Code içinde bu klasörü yerel marketplace olarak ekleyin:

```text
/plugin marketplace add C:\path\to\legal-turkish-master
```

Bir plugin kurun:

```text
/plugin install commercial-legal@legal-turkish
```

Claude Code'u yeniden başlatın. Ardından ilgili plugin'in başlangıç mülakatını çalıştırın:

```text
/commercial-legal:cold-start-interview
```

İlk kullanım örneği:

```text
/commercial-legal:review "C:\sozlesmeler\tedarikci-taslak.docx"
```

Diğer örnekler:

```text
/litigation-legal:demand-intake
/privacy-legal:pia-generation
/employment-legal:termination-review
/regulatory-legal:reg-feed-watcher
```

Kısa kurulum akışı için: [QUICKSTART.md](QUICKSTART.md)

## Bağlantılar ve MCP

Plugin'lerde Slack, Google Drive, Box, Linear, Asana gibi operasyonel bağlayıcılar opsiyonel olarak korunmuştur. Türk hukuk kaynaklarına yönelik yerel araştırma omurgası için `.mcp.json` dosyalarında **Yargı MCP** önerilir.

Yargı MCP; Yargıtay, Danıştay, Anayasa Mahkemesi, KVKK, Rekabet Kurumu ve benzeri Türkiye kaynaklarına erişim için kullanılır. Bağlantı çalışmıyorsa veya bağlı değilse çıktılardaki kaynak/citation etiketleri doğrulama uyarısı taşır.

## Repo Yapısı

```text
legal-turkish-master/
├── .claude-plugin/
│   └── marketplace.json
├── commercial-legal/
├── corporate-legal/
├── litigation-legal/
├── privacy-legal/
├── employment-legal/
├── product-legal/
├── regulatory-legal/
├── ip-legal/
├── ai-governance-legal/
├── managed-agent-cookbooks/
├── legal-builder-hub/
├── references/
└── scripts/
```

## Doğrulama

Bu çalışma kopyasında yapılan son yapısal kontroller:

- Marketplace `source` yolları ve plugin manifestleri çözümleniyor.
- Tüm JSON dosyaları parse ediliyor.
- Somut plugin komut atıfları mevcut skill klasörlerine gidiyor.
- Managed-agent `manifest`, `file` ve `from_plugin` referansları çözümleniyor.
- Ana `claude-for-legal-main` iskeletine göre eksik dosya yok.
- Türkçeye çevrilmiş operasyonel identifier kalıntıları temizlendi (`reg-feed-watcher`, `feed-reader` korunur).

Windows ortamında `bash` ve `pyyaml` yoksa repo'nun `scripts/test-cookbooks.sh` harness'i birebir çalışmayabilir; bu durumda eşdeğer statik kontroller PowerShell/Node ile yapılabilir.

## Yayın Notu

Bu repo bir Türkiye uyarlama çalışmasıdır. Orijinal Claude for Legal projesinin lisans ve katkı koşulları korunur. Uyarlanan içeriklerde Türk hukuku terminolojisi kullanılsa da hiçbir çıktı doğrudan hukuki mütalaa, avukat görüşü veya resmi kaynak doğrulaması yerine geçmez.

## Lisans

Apache License 2.0. Ayrıntı için [LICENSE](LICENSE).
