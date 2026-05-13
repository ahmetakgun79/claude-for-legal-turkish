# Legal Turkish - Klasör Klasör Uyarlama Denetimi

Bu dosya, `Legal Turkish` klasöründe hangi alanların Türk hukukuna uyarlanması gerektiğini, hangilerinin orijinal yapı gibi kalabileceğini ve uygulama sırasını izler.

Durum etiketleri:

- `Değişmeli`: Hukuki içerik ABD/AB/common law varsayımlarına dayanıyor; Türk hukuku ve uygulaması için uyarlanmalı.
- `Kısmen değişmeli`: Teknik yapı kalabilir, ama açıklama, örnek, kaynak, workflow veya bazı skill'ler Türk hukukuna göre güncellenmeli.
- `Kalabilir`: Hukuki içerik taşımıyor veya repo altyapısı; şimdilik orijinal gibi kalması sorun yaratmaz.
- `Harici`: Üçüncü taraf veya dış kaynak; değiştirmeden önce ayrıca karar verilmeli.

## Kök Dosyalar

| Yol | Karar | Gerekçe | Aksiyon |
|---|---|---|---|
| `README.md` | Kısmen değişmeli | Türk sürüm kimliği kuruldu; tüm plugin tabloları henüz ayrıntılı Türkçeleşmedi. | Ana özet tamamlandı; plugin tabloları alan alan güncellenecek. |
| `QUICKSTART.md` | Kısmen değişmeli | Kurulum Türk sürüme göre yazıldı; plugin kapsamları ilerledikçe örnek komutlar genişletilebilir. | Şimdilik yeterli. |
| `TURKISH_ADAPTATION_STATUS.md` | Kalabilir | Uyarlama takip dosyası. | Her klasör işlendikçe güncellenecek. |
| `CODE_OF_CONDUCT.md` | Kalabilir | Hukuki iş akışı içeriği değil. | Yayınlama yapılacaksa Türkçe versiyon eklenebilir. |
| `CONTRIBUTING.md` | Kısmen değişmeli | Katkı kuralları orijinal projeye göre; Türk adaptasyon katkı kuralları eklenmeli. | Sonraki dokümantasyon turu. |
| `CONNECTORS.md` | Kısmen değişmeli | Connector listesinde ABD/uluslararası hukuk kaynakları ağırlıklı olabilir. | Türkiye kaynakları ve UYAP/UETS/KEP notları eklenecek. |
| `LICENSE` | Kalabilir | Lisans metni değiştirilmemeli. | Dokunma. |
| `.gitignore` | Kalabilir | Teknik dosya. | Dokunma. |

## Tamamlanan Klasörler

| Klasör | Tamamlanan iş | Not |
|---|---|---|
| `.claude-plugin` | Marketplace kimliği ve plugin açıklamaları Türk sürüm statüsüne göre güncellendi. | Plugin adları ve kaynak yolları korundu; açıklamalar uyarlanmış/bekleyen/harici statüsünü gösteriyor. |
| `commercial-legal` | İlk tur commercial uyarlaması tamamlandı. | README, CLAUDE template, 12 skill, 3 agent, renewal-register ve MCP açıklamaları Türk ticari hukuk pratiğine göre güncellendi; NDA/ticari kavram karşılıkları senkronize edildi. |
| `corporate-legal` | İlk çekirdek corporate uyarlaması yapıldı. | README, CLAUDE template, audit, cold-start, board-minutes, closing-checklist, diligence-issue-extraction, material-contract-schedule, integration-management, dataroom-watcher, written-consent ve entity-compliance Türk şirketler hukuku pratiğine göre güncellendi; yapısal veri dili ve M&A kolon referansları senkronize edildi. |
| `litigation-legal` | İlk tur litigation uyarlaması tamamlandı. | UYAP, UETS, HMK/CMK, arabuluculuk, müzekkere, isticvap/tanık, delil tespiti, Av.K. m.36 gizlilik, portföy ve dış büro raporlama akışları Türk dava pratiğine göre güncellendi; claim-chart unsur şablonları Türk hukukuna çevrildi. |
| `privacy-legal` | İlk tur KVKK uyarlaması tamamlandı. | README, CLAUDE template, 9 skill, currency-watch, MCP ve marketplace açıklamaları KVKK/Kurul/VERBIS, aydınlatma, açık rıza, yurt dışına aktarım, ilgili kişi başvurusu, ihlal ve politika drift pratiğine göre güncellendi. |
| `employment-legal` | İlk tur iş hukuku uyarlaması tamamlandı. | README, CLAUDE template, 20 skill, leave-tracker agent, currency-watch, MCP ve marketplace açıklamaları İş Kanunu, SGK/İŞKUR/İSG, fesih, arabuluculuk, ücret, izin, iç soruşturma ve personel politikalarına göre güncellendi. |
| `product-legal` | İlk tur ürün hukuku uyarlaması tamamlandı. | README, CLAUDE template, 7 skill, launch-watcher agent, launch framework, currency-watch, MCP ve marketplace açıklamaları 6502/6563, reklam, KVKK, sektör, ürün güvenliği ve AI kapılarına göre güncellendi. |
| `regulatory-legal` | İlk tur regulatory uyarlaması tamamlandı. | README, CLAUDE template, 9 skill, reg-change-monitor agent, source catalog, gap/comment tracker örnekleri, MCP ve marketplace açıklamaları Resmi Gazete/Mevzuat, KVKK, Rekabet, SPK, BDDK, BTK, EPDK, TCMB, Ticaret Bakanlığı, MASAK ve sektör kurumlarına göre güncellendi. |
| `managed-agent-cookbooks` | Uyarlandı. | Türkiye kaynak ve takip mantığına göre uyarlandı. |

## Kök Klasör Matrisi

| Sıra | Klasör | Karar | Neden | İlk Aksiyon |
|---:|---|---|---|---|
| 1 | `.claude-plugin` | Kısmen değişmeli | Marketplace adı `legal-turkish` yapıldı; plugin açıklamaları hâlâ orijinal İngilizce ve bazıları ABD/AB pratiği anlatıyor. | `marketplace.json` açıklamalarını Türk kapsam dürüstlüğüyle güncelle. |
| 2 | `.github` | Kalabilir | CI, issue template veya GitHub altyapısı; doğrudan hukuki çıktı üretmez. | Yayınlanacak repo olursa template ve açıklamalar Türkçeleştirilebilir. |
| 3 | `ai-governance-legal` | Başlangıç uyarlaması | KVKK/FSEK/TTK ticari sır ve Türkiye AI yönetişimi başlıkları için ilk çerçeve kuruldu. | İkinci fazda kapsam genişletilebilir. |
| 4 | `commercial-legal` | Tamamlandı - ilk tur + kavram senkronu | Ana skill seti, README, CLAUDE template, agents ve MCP açıklamaları Türk ticari hukuk pratiğine göre uyarlandı; residuals, bakiye hükümler, DVK, TBK m.179-185 ve 6325 kavramları eklendi. | İkinci turda gerçek sözleşmelerle smoke test. |
| 5 | `corporate-legal` | Kısmen tamamlandı - ilk tur + referans senkronu | Delaware/US corporate, board consent, M&A diligence mantığı Türk TTK, SPK ve MERSİS/Ticaret Sicili pratiğine çevrilmeli. | Çekirdek profil, governance, entity, due diligence, closing, material schedule, integration ve dataroom watcher güncellendi; YAML/tracker alan standardı canonical `english_snake_case`, insan-facing tablo/rapor dili Türkçe olarak belirlendi; M&A diligence kolonları TİTCK/KİK/SPK/BDDK/KVKK/Rekabet/DVK çizgisine alındı. |
| 6 | `employment-legal` | Tamamlandı - ilk tur Türk iş hukuku çekirdeği | Yabancı employment mantığı Türkiye İş Kanunu, SGK, İŞKUR, İSG, arabuluculuk ve iş mahkemeleri pratiğine çevrildi. | İkinci turda gerçek iş sözleşmesi, fesih dosyası, bordro/izin kaydı ve iç soruşturma örneğiyle smoke test. |
| 7 | `external_plugins` | Harici | CoCounsel/Westlaw gibi üçüncü taraf plugin; doğrudan değiştirmek doğru olmayabilir. | Kullanılacak mı karar ver; Türk hukuk kaynakları yoksa devre dışı/opsiyonel notu. |
| 8 | `ip-legal` | Tamamlandı - ilk tur Türk IP çekirdeği | FSEK, SMK, TÜRKPATENT, WIPO, tecavüzün men'i, 5651 uyar-kaldır ve Türk gizlilik pratiği merkeze alındı. | İkinci turda gerçek marka/telif/patent dosyalarıyla smoke test. |
| 9 | `law-student` | Uyumsuz / kapsam dışı | Bar prep, MBE/UBE/NextGen, case brief, IRAC, Socratic/cold-call ve professor past-exam mantığı ABD hukuk eğitimi varsayımlı. Türk hukuk fakültesi, HMGS/İYÖS, pratik çalışma ve mevzuat-içtihat okuma sistemiyle doğrudan uyumlu değil. | Uyarlama yapılmayacak; ileride ihtiyaç olursa ayrı bir Türk hukuk öğrencisi plugin'i sıfırdan tasarlanmalı. |
| 10 | `legal-builder-hub` | Teknik/meta araç | Hukuki içerik modülü olmadığı için ana uyarlama kapsamı dışında tutuldu; skill bulma, QA ve kurulum yapısı korundu. | Gerekirse sonraki fazda güvenlik/kurulum kontrolleri genişletilebilir. |
| 11 | `legal-clinic` | Ayrık / kapsam dışı | Türkiye'de doğrudan karşılığı olmayan US law school clinic modeli üzerine kurulu. Legal Turkish çekirdeğine çevrilmeyecek; ihtiyaç olursa ayrı bir klinik/adli yardım tasarımı olarak ele alınmalı. | Uyarlama kuyruğundan çıkar; mevcut hali harici/ayrık referans olarak kalsın. |
| 12 | `litigation-legal` | Tamamlandı - ilk tur + unsur şablonu senkronu | Ana dava takip, ihtarname, kronoloji, dilekçe, müzekkere, delil, gizlilik, portföy, dış büro raporu ve UYAP docket watcher akışları Türk uygulamasına uyarlandı; claim-chart common-law unsurları TBK/TTK/HMK odaklı şablonlarla değiştirildi. | İkinci turda gerçek UYAP evraklarıyla smoke test yapılabilir. |
| 13 | `managed-agent-cookbooks` | Tamamlandı - ilk tur otonom ajan YAML çekirdeği | Ajan mimarisi korundu; docket/reg/renewal/diligence/launch cookbook YAML'leri Türk kaynak, güvenli domain ve prosedür mantığına göre kontrol edildi. | İkinci turda gerçek UYAP/Yargı MCP/Lexpera ve Türkiye düzenleyici kaynak bağlantılarıyla smoke test. |
| 14 | `privacy-legal` | Tamamlandı - ilk tur KVKK çekirdeği | Yabancı privacy dili yoğun yapı KVKK, Kurul, veri sorumlusu/veri işleyen, yurt dışı aktarım, VERBIS, aydınlatma/açık rıza ve ilgili kişi başvurusu pratiğine çevrildi. | İkinci turda gerçek aydınlatma, DPA ve ilgili kişi başvurusu örnekleriyle smoke test. |
| 15 | `product-legal` | Tamamlandı - ilk tur Türk ürün hukuku çekirdeği | US product/marketing claims varsayımları 6502 tüketici hukuku, ticari reklam, 6563 e-ticaret, KVKK, BTK/SPK/BDDK/TİTCK/Rekabet ve AI/otomasyon kapılarına çevrildi. | İkinci turda gerçek PRD, reklam metni, abonelik checkout, influencer brief'i ve tracking/cookie örnekleriyle smoke test. |
| 16 | `references` | Kısmen değişmeli | Ana Türk adaptasyon rehberi ve kaynak arşivi var; bazı genel şablonlar orijinal. | Türkiye kaynak katalogları ve alan bazlı referanslar eklenecek. |
| 17 | `regulatory-legal` | Tamamlandı - ilk tur Türk regulatory çekirdeği | Eski yabancı regülasyon izleme mantığı Türkiye Resmî Gazete, Mevzuat, kurum duyuruları, taslak/görüş, gap tracker ve politika diff akışına çevrildi. | İkinci turda gerçek kurum duyurusu ve politika kütüphanesiyle smoke test. |
| 18 | `scripts` | Kalabilir | Teknik yardımcı scriptler; hukuki içerik üretmez. | Ancak path veya marketplace adı hard-code ise ayrıca kontrol edilir. |

## Öncelik Sırası

1. `.claude-plugin`: Türk marketplace kimliği ve plugin açıklamaları.
2. `commercial-legal`: Zaten başlanmış alanı tamamla; README/CLAUDE/agents/kalan skill'ler.
3. `litigation-legal`: Tamamlandı - ilk tur; ikinci turda gerçek UYAP evraklarıyla smoke test.
4. `privacy-legal`: Tamamlandı - ilk tur; ikinci turda gerçek belge smoke test'i.
5. `employment-legal`: Tamamlandı - ilk tur; ikinci turda gerçek belge smoke test'i.
6. `corporate-legal`: TTK/SPK/MERSİS/Ticaret Sicili çekirdeği başladı; kalan M&A ve governance skill'leri tamamlanacak.
7. `ip-legal`: ilk tur tamamlandı; ikinci turda gerçek dosyalarla smoke test.
8. `ai-governance-legal`: başlangıç uyarlaması yapıldı; ikinci fazda kapsam genişletilebilir.
9. `legal-builder-hub`.
10. `managed-agent-cookbooks`, `references`, root docs polish.

Not: `legal-clinic`, Türkiye'de doğrudan karşılığı olmayan ayrı bir model olduğu için Legal Turkish uyarlama kuyruğundan çıkarıldı.

## İlk Klasör Detayı: `.claude-plugin`

Durum: `Tamamlandı - ilk tur`.

Yapılan:

- Marketplace adı `legal-turkish` olarak ayrıldı.
- Owner adı `Legal Turkish Adaptation` olarak güncellendi.
- Plugin açıklamaları Türkçe statü notlarıyla güncellendi.
- Uyarlanan pluginler `Uyarlandı` olarak işaretlendi.
- Uyarlanmayan pluginler yalnızca kısa gerekçesiyle `Uyarlanmadı` olarak işaretlendi.
- `law-student` uyumsuz/kapsam dışı olarak ayrıldı; Legal Turkish kapsamında uyarlanmayacak.
- `cocounsel-legal` harici ve opsiyonel üçüncü taraf plugin olarak işaretlendi.

Eksik:

- İleride plugin adlarını Türkçeleştirme kararı alınırsa marketplace kaynakları yeniden ele alınmalı.

Önerilen aksiyon:

- Şimdilik tamam. Sıradaki klasör: `.github` kısa kontrol, ardından `commercial-legal` derin denetim.

## İkinci Klasör Detayı: `.github`

Durum: `Yayın öncesi temizlendi`.

Gerekçe:

- Hukuki workflow üretmiyor.
- Şimdilik plugin kullanımını etkilemez.
- Yayın öncesi eski CLA workflow'u kaldırıldı; repo ilk sürümde otomatik CLA kontrolü çalıştırmaz.

Önerilen aksiyon:

- İleride katkı kabul akışı kurulacaksa yeni `CLA.md`, allowlist ve workflow ayrı olarak tasarlanmalı.

## Üçüncü Klasör Detayı: `corporate-legal`

Durum: `Kısmen tamamlandı - ilk tur`.

Yapılan:

- `corporate-legal/TURKISH_AUDIT.md` eklendi.
- `corporate-legal/README.md` Türk şirketler hukuku açıklaması olarak yeniden yazıldı.
- `corporate-legal/CLAUDE.md` TTK, SPK/KAP/MKK, MERSİS, ticaret sicili, karar defteri, imza/temsil yetkisi ve Türkiye M&A akışına göre yeniden yazıldı; yapısal veri standardı eklendi.
- `corporate-legal/skills/cold-start-interview/SKILL.md` Türk şirket profili, M&A, kurumsal yönetim, sermaye piyasası ve entity management mülakatına çevrildi.
- `corporate-legal/skills/board-minutes/SKILL.md` yönetim kurulu, müdürler kurulu, genel kurul ve komite tutanak/karar taslağı akışına çevrildi.
- `corporate-legal/skills/closing-checklist/SKILL.md` Türk M&A kapanış koşulları, organ kararları, tescil/MERSİS, Rekabet, SPK/KAP/MKK, sözleşme onayları, teminat fekki, KVKK, ruhsat ve kapanış kanıtlarıyla yeniden yazıldı.
- `corporate-legal/skills/diligence-issue-extraction/SKILL.md` Türk M&A due diligence kategorileri, KVKK, Rekabet, ticaret sicili, imza yetkisi, çalışan/SGK, vergi, IP, ruhsat ve uyuşmazlık kontrolleriyle yeniden yazıldı.
- `corporate-legal/skills/material-contract-schedule/SKILL.md`, `corporate-legal/skills/integration-management/SKILL.md` ve `corporate-legal/agents/dataroom-watcher.md` dosyalarının Türkiye M&A pratiğine uyarlanmış olduğu doğrulandı; material schedule insan-facing tablo başlıkları Türkçe, integration tracker alanları canonical `english_snake_case` standardında tutuldu.
- `corporate-legal/skills/tabular-review/references/ma-diligence-columns.md` FDA/FAR/DFARS/FINRA/SEC kolonlarından çıkarılıp TİTCK, KİK, SPK, BDDK, TCMB, BTK, EPDK, Rekabet, KVKK ve DVK kontrol başlıklarına çevrildi.
- `tabular-review`, `deal-team-summary`, `ai-tool-handoff`, `matter-workspace`, `excel-output.md` ve `gsheets-output.md` içindeki eski `## Outputs` / `[WORK-PRODUCT HEADER]` referansları `## Çıktı kuralları` ve Türkçe gizli çalışma başlığına bağlandı.
- `corporate-legal/skills/written-consent/SKILL.md` ABD `unanimous written consent` mantığından çıkarılıp Türk karar taslağı, toplantısız/sirküler karar, tescil/ilan ve formalite kontrol akışına çevrildi.
- `corporate-legal/skills/entity-compliance/SKILL.md` Secretary of State/franchise tax/good standing yapısından çıkarılıp MERSİS, ticaret sicili, faaliyet belgesi, imza sirküleri, karar defteri, VERBİS, vergi/SGK ve sektör izinleri tracker'ına çevrildi; Türkçe YAML anahtarları canonical `english_snake_case` şemaya normalize edildi.

Kalabilecekler:

- Klasör ve komut adları şimdilik korunmalı; repo genelinde yeniden adlandırma yapılmadıkça `/corporate-legal:*` komutları değişmemeli.
- `hooks/` ve teknik workspace dosyaları hukuki içerik taşımadığı için kalabilir.
- Tablo/CSV ve matter-workspace mantığı küçük Türk alanları eklenerek kullanılabilir.

Eksik:

- `customize`, `tabular-review`, `deal-team-summary`, `ai-tool-handoff` ve bazı reference dosyalarında ikinci tur terminoloji/örnek yerelleştirmesi yapılabilir.
- `.mcp.json` açıklamaları Türkiye kaynakları ve manuel kaynak fallback'leriyle zenginleştirilmeli.

Önerilen aksiyon:

- Sıradaki corporate adımı: yardımcı corporate dosyalarında ikinci tur polish veya başka ana modüle geçiş.

## Dördüncü Klasör Detayı: `litigation-legal`

Durum: `Tamamlandı - ilk tur`.

Yapılan:

- `litigation-legal/TURKISH_ADAPTATION_STATUS.md` yerel durum dosyası oluşturuldu.
- `README.md` ve `CLAUDE.md` UYAP, UETS, HMK, CMK, Av.K. m.36, KVKK/Rekabet ve Türk dava safahatına göre güncellendi.
- `CLAUDE.md` kaynak etiketi ve örnekleri ABD dava araştırması çizgisinden Lexpera/Lextera/Kazancı/UYAP/Mevzuat.gov.tr/Resmî Gazete çizgisine alındı.
- `matter-intake`, `legal-hold`, `subpoena-triage`, `deposition-prep`, `privilege-log-review`, `portfolio-status`, `oc-status` ve önceki dava/ihtarname skill'leri Türk hukuk pratiğine uyarlandı.
- `claim-chart/references/element-templates.md` ABD common-law unsur kütüphanesinden Türk TBK/TTK/HMK dava unsurları kütüphanesine çevrildi.
- `skills/matter-workspace/SKILL.md` içindeki yabancı hukuk/Delaware örneği Türk hukuku ve yabancı hukuk eskalasyonu örneğiyle değiştirildi.
- `agents/docket-watcher.md` yabancı docket izleme mantığından UYAP evrak, e-tebligat, tensip, bilirkişi raporu ve HMK kesin süre uyarısı mantığına çekildi.
- `inbound/_README.md`, `demand-letters/_README.md` ve `matters/_README.md` Türk dosya ve evrak akışına göre açıklandı.

Eksik:

- İlk tur için kapalı. İkinci turda gerçek UYAP çıktısı, noter/KEP ihtarnamesi ve dava portföyüyle smoke test yapılabilir.

## Beşinci Klasör Detayı: `privacy-legal`

Durum: `Tamamlandı - ilk tur KVKK çekirdeği`.

Yapılan:

- `privacy-legal/TURKISH_AUDIT.md` eklendi ve tamamlandı statüsüne alındı.
- `README.md` ve `CLAUDE.md` KVKK, Kurul uygulaması, VERBIS, aydınlatma, açık rıza, özel nitelikli veri, yurt dışına aktarım, veri ihlali ve ilgili kişi başvurusu akışına göre yeniden yazıldı.
- `.mcp.json`, `.claude-plugin/plugin.json` ve marketplace açıklaması privacy plugin'in KVKK kapsamını doğru gösterecek şekilde güncellendi.
- `references/currency-watch.md` KVKK m.6/m.9, standart sözleşme, ihlal bildirimi, VERBIS, aydınlatma/açık rıza, çerez/İYS ve sektör regülasyonları için watch list'e çevrildi.
- `cold-start-interview`, `use-case-triage`, `pia-generation`, `dpa-review`, `dsar-response`, `reg-gap-analysis`, `policy-monitor`, `customize` ve `matter-workspace` skill'leri Türk KVKK uygulamasına uyarlandı.
- Skill içi eski `## Outputs` / `[WORK-PRODUCT HEADER]` referansları kullanılmadı; çıktılar `## Çıktı Kuralları` ve Türkçe gizli çalışma taslağı başlığına bağlandı.

Kalabilecekler:

- Klasör ve komut adları korunmalı; repo genelinde yeniden adlandırma yapılmadıkça `/privacy-legal:*` komutları değişmemeli.
- `hooks/` hukuki içerik taşımadığı için kalabilir.

Eksik:

- Gerçek aydınlatma/açık rıza metni, DPA, ilgili kişi başvurusu ve standart sözleşme örnekleriyle smoke test yapılmalı.
- Sektörel alanlar için BDDK/SPK/BTK/TİTCK gibi kurum bazlı ikinci tur derinleştirme yapılabilir.

## Altıncı Klasör Detayı: `employment-legal`

Durum: `Tamamlandı - ilk tur Türk iş hukuku çekirdeği`.

Yapılan:

- `employment-legal/TURKISH_AUDIT.md` eklendi ve tamamlandı statüsüne alındı.
- `README.md` ve `CLAUDE.md` İş Kanunu, SGK, İŞKUR, İSG, zorunlu arabuluculuk, iş güvencesi, ücret/çalışma süresi, izin/rapor, iç soruşturma, çalışan verisi ve personel politikaları çerçevesine göre yeniden yazıldı.
- `.mcp.json`, `.claude-plugin/plugin.json` ve marketplace açıklaması Türk iş hukuku kapsamını doğru gösterecek şekilde güncellendi.
- `references/currency-watch.md` asgari ücret, SGK, kıdem tavanı, arabuluculuk, İSG, izin, fesih ve çalışan verisi değişkenleri için eklendi.
- `cold-start-interview`, `customize`, `hiring-review`, `termination-review`, `wage-hour-qa`, `worker-classification`, `leave-tracker`, `log-leave`, `policy-drafting`, `handbook-updates`, `internal-investigation`, `investigation-*`, `international-expansion`, `expansion-*` ve `matter-workspace` skill'leri Türkiye uygulamasına uyarlandı.
- `agents/leave-tracker.md` yıllık izin, rapor, analık, ücretsiz izin, devamsızlık ve dönüş tarihi izlemesine çevrildi.

Kalabilecekler:

- Klasör ve komut adları korunmalı; repo genelinde yeniden adlandırma yapılmadıkça `/employment-legal:*` komutları değişmemeli.
- `hooks/` ve `data/.gitkeep` hukuki içerik taşımadığı için kalabilir.

Eksik:

- Gerçek iş sözleşmesi, fesih dosyası, bordro/puantaj, izin kaydı ve iç soruşturma dosyasıyla ikinci tur smoke test yapılmalı.
- Sendika/TİS ve toplu işçi çıkarma akışları gerçek örneklerle derinleştirilebilir.

## Yedinci Klasör Detayı: `regulatory-legal`

Durum: `Tamamlandı - ilk tur Türk regulatory çekirdeği`.

Yapılan:

- `regulatory-legal/TURKISH_AUDIT.md` eklendi.
- `README.md` ve `CLAUDE.md` Türkiye düzenleyici izleme profiline çevrildi.
- `.mcp.json`, `.claude-plugin/plugin.json` ve marketplace açıklaması regulatory kapsamı doğru gösterecek şekilde güncellendi.
- `reg-feed-watcher`, `policy-diff`, `comments`, `gaps`, `gap-surfacer`, `policy-redraft`, `customize`, `matter-workspace` ve `cold-start-interview` skill'leri Türkiye uygulamasına uyarlandı.
- `agents/reg-change-monitor.md` Resmi Gazete/Mevzuat ve kurum kaynaklarını izleyen Türkiye digest ajanına dönüştürüldü.
- `source-catalog.md` Türkiye resmi kaynak kataloğuna çevrildi.
- `gap-tracker.yaml` ve `comment-tracker.yaml` taslak/görüş ve policy gap şemalarına göre güncellendi.

Eksik:

- Gerçek Resmi Gazete metni, KVKK/Rekabet/SPK/BDDK/BTK kurum duyurusu ve canlı politika kütüphanesiyle ikinci tur smoke test yapılmalı.
