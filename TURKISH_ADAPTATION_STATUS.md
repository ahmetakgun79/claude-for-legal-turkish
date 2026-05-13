# Turkish Adaptation Status

Bu dosya `Legal Turkish` klasöründeki Türk hukuku adaptasyon durumunu izler.

## Ana Referanslar

- `references/Claude for Legal - Türk Hukuku Adaptasyon Rehberi.md`
- `references/turkish-adaptation-sources/`
- `TURKISH_FOLDER_AUDIT.md`

## Çalışma Yöntemi

Uyarlama bundan sonra klasör klasör yürütülecek. Her klasör için önce `TURKISH_FOLDER_AUDIT.md` dosyasında şu karar verilecek:

- Türk hukukuna göre değişmeli mi?
- Ana dosyadaki haliyle kalması sorun olur mu?
- Kısmen değişecekse hangi dosyalar öncelikli?
- Hangi skill/agent/reference dosyaları ertelenebilir?

## Tamamlanan Skill Uyarlamaları

| Alan | Skill | Dosya |
|---|---|---|
| Commercial | review | `commercial-legal/skills/review/SKILL.md` |
| Commercial | nda-review | `commercial-legal/skills/nda-review/SKILL.md` |
| Commercial | vendor-agreement-review | `commercial-legal/skills/vendor-agreement-review/SKILL.md` |
| Commercial | saas-msa-review | `commercial-legal/skills/saas-msa-review/SKILL.md` |
| Commercial | stakeholder-summary | `commercial-legal/skills/stakeholder-summary/SKILL.md` |
| Commercial | renewal-tracker | `commercial-legal/skills/renewal-tracker/SKILL.md` |
| Commercial | amendment-history | `commercial-legal/skills/amendment-history/SKILL.md` |
| Commercial | customize | `commercial-legal/skills/customize/SKILL.md` |
| Commercial | escalation-flagger | `commercial-legal/skills/escalation-flagger/SKILL.md` |
| Commercial | matter-workspace | `commercial-legal/skills/matter-workspace/SKILL.md` |
| Commercial | cold-start-interview | `commercial-legal/skills/cold-start-interview/SKILL.md` |
| Commercial | review-proposals | `commercial-legal/skills/review-proposals/SKILL.md` |
| Litigation | cold-start-interview | `litigation-legal/skills/cold-start-interview/SKILL.md` |
| Litigation | brief-section-drafter | `litigation-legal/skills/brief-section-drafter/SKILL.md` |
| Litigation | chronology | `litigation-legal/skills/chronology/SKILL.md` |
| Litigation | claim-chart | `litigation-legal/skills/claim-chart/SKILL.md` |
| Litigation | demand-intake | `litigation-legal/skills/demand-intake/SKILL.md` |
| Litigation | demand-draft | `litigation-legal/skills/demand-draft/SKILL.md` |
| Litigation | demand-received | `litigation-legal/skills/demand-received/SKILL.md` |
| Litigation | matter-intake | `litigation-legal/skills/matter-intake/SKILL.md` |
| Litigation | legal-hold | `litigation-legal/skills/legal-hold/SKILL.md` |
| Litigation | subpoena-triage | `litigation-legal/skills/subpoena-triage/SKILL.md` |
| Litigation | deposition-prep | `litigation-legal/skills/deposition-prep/SKILL.md` |
| Litigation | privilege-log-review | `litigation-legal/skills/privilege-log-review/SKILL.md` |
| Litigation | portfolio-status | `litigation-legal/skills/portfolio-status/SKILL.md` |
| Litigation | oc-status | `litigation-legal/skills/oc-status/SKILL.md` |
| Litigation | docket-watcher (Agent) | `litigation-legal/agents/docket-watcher.md` |
| Corporate | cold-start-interview | `corporate-legal/skills/cold-start-interview/SKILL.md` |
| Corporate | board-minutes | `corporate-legal/skills/board-minutes/SKILL.md` |
| Corporate | closing-checklist | `corporate-legal/skills/closing-checklist/SKILL.md` |
| Corporate | diligence-issue-extraction | `corporate-legal/skills/diligence-issue-extraction/SKILL.md` |
| Corporate | written-consent | `corporate-legal/skills/written-consent/SKILL.md` |
| Corporate | entity-compliance | `corporate-legal/skills/entity-compliance/SKILL.md` |
| Corporate | material-contract-schedule | `corporate-legal/skills/material-contract-schedule/SKILL.md` |
| Corporate | integration-management | `corporate-legal/skills/integration-management/SKILL.md` |
| Corporate | dataroom-watcher (Agent) | `corporate-legal/agents/dataroom-watcher.md` |
| Privacy/KVKK | cold-start-interview | `privacy-legal/skills/cold-start-interview/SKILL.md` |
| Privacy/KVKK | use-case-triage | `privacy-legal/skills/use-case-triage/SKILL.md` |
| Privacy/KVKK | pia-generation | `privacy-legal/skills/pia-generation/SKILL.md` |
| Privacy/KVKK | dpa-review | `privacy-legal/skills/dpa-review/SKILL.md` |
| Privacy/KVKK | dsar-response | `privacy-legal/skills/dsar-response/SKILL.md` |
| Privacy/KVKK | reg-gap-analysis | `privacy-legal/skills/reg-gap-analysis/SKILL.md` |
| Privacy/KVKK | policy-monitor | `privacy-legal/skills/policy-monitor/SKILL.md` |
| Privacy/KVKK | customize | `privacy-legal/skills/customize/SKILL.md` |
| Privacy/KVKK | matter-workspace | `privacy-legal/skills/matter-workspace/SKILL.md` |
| Employment | cold-start-interview | `employment-legal/skills/cold-start-interview/SKILL.md` |
| Employment | hiring-review | `employment-legal/skills/hiring-review/SKILL.md` |
| Employment | termination-review | `employment-legal/skills/termination-review/SKILL.md` |
| Employment | wage-hour-qa | `employment-legal/skills/wage-hour-qa/SKILL.md` |
| Employment | worker-classification | `employment-legal/skills/worker-classification/SKILL.md` |
| Employment | leave-tracker | `employment-legal/skills/leave-tracker/SKILL.md` |
| Employment | log-leave | `employment-legal/skills/log-leave/SKILL.md` |
| Employment | policy-drafting | `employment-legal/skills/policy-drafting/SKILL.md` |
| Employment | handbook-updates | `employment-legal/skills/handbook-updates/SKILL.md` |
| Employment | internal-investigation | `employment-legal/skills/internal-investigation/SKILL.md` |
| Employment | investigation-open | `employment-legal/skills/investigation-open/SKILL.md` |
| Employment | investigation-add | `employment-legal/skills/investigation-add/SKILL.md` |
| Employment | investigation-query | `employment-legal/skills/investigation-query/SKILL.md` |
| Employment | investigation-memo | `employment-legal/skills/investigation-memo/SKILL.md` |
| Employment | investigation-summary | `employment-legal/skills/investigation-summary/SKILL.md` |
| Employment | international-expansion | `employment-legal/skills/international-expansion/SKILL.md` |
| Employment | expansion-kickoff | `employment-legal/skills/expansion-kickoff/SKILL.md` |
| Employment | expansion-update | `employment-legal/skills/expansion-update/SKILL.md` |
| Employment | customize | `employment-legal/skills/customize/SKILL.md` |
| Employment | matter-workspace | `employment-legal/skills/matter-workspace/SKILL.md` |
| Employment | leave-tracker (Agent) | `employment-legal/agents/leave-tracker.md` |
| Product | cold-start-interview | `product-legal/skills/cold-start-interview/SKILL.md` |
| Product | launch-review | `product-legal/skills/launch-review/SKILL.md` |
| Product | marketing-claims-review | `product-legal/skills/marketing-claims-review/SKILL.md` |
| Product | is-this-a-problem | `product-legal/skills/is-this-a-problem/SKILL.md` |
| Product | feature-risk-assessment | `product-legal/skills/feature-risk-assessment/SKILL.md` |
| Product | customize | `product-legal/skills/customize/SKILL.md` |
| Product | matter-workspace | `product-legal/skills/matter-workspace/SKILL.md` |
| Product | launch-watcher (Agent) | `product-legal/agents/launch-watcher.md` |
| Regulatory | cold-start-interview | `regulatory-legal/skills/cold-start-interview/SKILL.md` |
| Regulatory | reg-feed-watcher | `regulatory-legal/skills/reg-feed-watcher/SKILL.md` |
| Regulatory | policy-diff | `regulatory-legal/skills/policy-diff/SKILL.md` |
| Regulatory | comments | `regulatory-legal/skills/comments/SKILL.md` |
| Regulatory | gaps | `regulatory-legal/skills/gaps/SKILL.md` |
| Regulatory | gap-surfacer | `regulatory-legal/skills/gap-surfacer/SKILL.md` |
| Regulatory | policy-redraft | `regulatory-legal/skills/policy-redraft/SKILL.md` |
| Regulatory | customize | `regulatory-legal/skills/customize/SKILL.md` |
| Regulatory | matter-workspace | `regulatory-legal/skills/matter-workspace/SKILL.md` |
| Regulatory | reg-change-monitor (Agent) | `regulatory-legal/agents/reg-change-monitor.md` |

## Eşlik Eden Referans Güncellemeleri

| Dosya | Durum |
|---|---|
| `commercial-legal/skills/renewal-tracker/references/renewal-register.yaml` | Türk bildirim ve yenileme pratiğine göre güncellendi |
| `.claude-plugin/marketplace.json` | `legal-turkish` kimliği ve Türkçe statü açıklamalarıyla güncellendi |
| `commercial-legal/CLAUDE.md` | Türk commercial contracts profil template'i olarak yeniden yazıldı |
| `commercial-legal/README.md` | Legal Turkish commercial açıklaması olarak yeniden yazıldı |
| `commercial-legal/agents/*.md` | Renewal/debrief/playbook monitor ajanları Türk commercial playbook'a göre güncellendi |
| `commercial-legal/.mcp.json` | Connector açıklamaları Legal Turkish kullanımına göre güncellendi |
| `commercial-legal/CLAUDE.md` ve commercial skill/agent'ları | Residuals/hafızada kalan bilgi, bakiye hükümler, damga vergisi (DVK/488), cezai şart (TBK m.179-185), TBK m.19/27/28 ve 6325 arabuluculuk kavramları standardize edildi |
| `corporate-legal/TURKISH_AUDIT.md` | Corporate klasörü için değişmeli/kalabilir matrisi eklendi |
| `corporate-legal/CLAUDE.md` | Türk şirketler hukuku, TTK/SPK/MERSİS/Ticaret Sicili profil template'i olarak yeniden yazıldı |
| `corporate-legal/README.md` | Legal Turkish corporate açıklaması olarak yeniden yazıldı |
| `corporate-legal/CLAUDE.md` ve yardımcı output dosyaları | Eski `## Outputs` / `[WORK-PRODUCT HEADER]` referansları `## Çıktı kuralları` ve Türkçe gizli çalışma başlığına bağlandı |
| `corporate-legal/CLAUDE.md`, `entity-compliance`, `integration-management`, `material-contract-schedule` | Yapısal veri dili standardı eklendi: YAML/JSON/tracker/CSV aktarım alanları canonical `english_snake_case`, kullanıcıya görünen tablo/rapor başlıkları Türkçe |
| `corporate-legal/skills/tabular-review/references/ma-diligence-columns.md` | FDA/FAR/DFARS/FINRA/SEC kolonları Türkiye M&A pratiğine çevrildi: TİTCK, KİK, SPK, BDDK, TCMB, BTK, EPDK, Rekabet, KVKK ve DVK kontrolleri eklendi |
| `litigation-legal/TURKISH_ADAPTATION_STATUS.md` | Litigation klasörü için tamamlandı/stable durum özeti eklendi |
| `litigation-legal/CLAUDE.md`, `claim-chart/references/element-templates.md`, `matter-workspace` | Kaynak etiketleri UYAP/Yargı MCP/Mevzuat.gov.tr çizgisine alındı (Lexpera vb. işlevsel yerel araçlar olmadığı için sadece Yargı MCP eklendi); claim-chart common-law şablonları Türk TBK/TTK/HMK dava unsurlarıyla değiştirildi; yabancı hukuk/Delaware örneği kaldırıldı |
| `privacy-legal/TURKISH_AUDIT.md` | Privacy/KVKK klasörü için ilk tur tamamlandı matrisi eklendi |
| `privacy-legal/README.md`, `privacy-legal/CLAUDE.md`, `.mcp.json`, `.claude-plugin/plugin.json` | Privacy plugin kimliği KVKK, Kurul, VERBIS, aydınlatma, açık rıza, yurt dışına aktarım, ihlal ve ilgili kişi başvurusu eksenine çekildi |
| `privacy-legal/references/currency-watch.md` | KVKK m.6/m.9, standart sözleşme, ihlal, VERBIS, aydınlatma/açık rıza, çerez/İYS ve sektör regülasyonu watch list'i eklendi |
| `employment-legal/TURKISH_AUDIT.md` | Employment klasörü için ilk tur tamamlandı matrisi eklendi |
| `employment-legal/README.md`, `employment-legal/CLAUDE.md`, `.mcp.json`, `.claude-plugin/plugin.json` | Employment plugin kimliği İş Kanunu, SGK, İŞKUR, İSG, zorunlu arabuluculuk, fesih, ücret/çalışma süresi, izin ve iç soruşturma eksenine çekildi |
| `employment-legal/references/currency-watch.md` | Asgari ücret, SGK, kıdem tavanı, arabuluculuk, İSG, izin, fesih ve çalışan verisi watch list'i eklendi |
| `product-legal/TURKISH_AUDIT.md` | Product klasörü için ilk tur tamamlandı matrisi eklendi |
| `product-legal/README.md`, `product-legal/CLAUDE.md`, `.mcp.json`, `.claude-plugin/plugin.json` | Product plugin kimliği tüketici hukuku, reklam, e-ticaret, KVKK, ürün güvenliği, sektör regülasyonu ve AI/otomasyon eksenine çekildi |
| `product-legal/references/currency-watch.md` | 6502, 6563, reklam/haksız ticari uygulama, KVKK, sektör ve AI güncellik listesi eklendi |
| `product-legal/skills/launch-review/references/seven-category-framework.md` | ABD product launch framework'ü Türk ürün hukuku için sekiz kapılı lansman framework'üne çevrildi |
| `regulatory-legal/TURKISH_AUDIT.md` | Regulatory klasörü için ilk tur tamamlandı matrisi eklendi |
| `regulatory-legal/README.md`, `regulatory-legal/CLAUDE.md`, `.mcp.json`, `.claude-plugin/plugin.json` | Regulatory plugin kimliği Türkiye düzenleyici izleme, Resmi Gazete/Mevzuat, KVKK, Rekabet, SPK, BDDK, BTK, EPDK, TCMB, Ticaret Bakanlığı ve sektör kurumları eksenine çekildi |
| `regulatory-legal/skills/reg-feed-watcher/references/source-catalog.md` | Yabancı kaynak kataloğu Türkiye resmi kaynak kataloğuna çevrildi |
| `regulatory-legal/skills/gap-surfacer/references/*.yaml` | Gap ve taslak/görüş tracker örnekleri Türkiye regulatory pratiklerine göre güncellendi |
| `managed-agent-cookbooks/**/*.yaml` | Uyarlandı. Türkiye kaynak ve takip mantığına göre uyarlandı. |
| `ip-legal/README.md`, `ip-legal/CLAUDE.md`, `.mcp.json` | Uyarlandı. Türk fikri mülkiyet pratiğine göre uyarlandı. |
| `ai-governance-legal/skills/vendor-ai-review`, `use-case-triage` ve bazı AI governance skill'leri | Uyarlandı. Türkiye AI yönetişimi ve KVKK odağıyla uyarlandı. |
| `legal-builder-hub/skills/skills-qa`, `legal-builder-hub/skills/skill-installer`, `.claude-plugin/marketplace.json` | Yönetici mekanizma için Legal Turkish identifier/source path stabilitesi kontrolü eklendi; marketplace açıklamaları `legal-clinic`, `ip-legal`, `ai-governance-legal` ve `legal-builder-hub` gerçek durumuyla senkronize edildi |

## Klasör Denetim Durumu

| Klasör | Durum | Not |
|---|---|---|
| `.claude-plugin` | tamamlandı - ilk tur | Plugin açıklamaları uyarlanmış/bekleyen/harici statüsünü gösteriyor |
| `.github` | tamamlandı - ilk tur | Lokal/plugin kullanımı için kalabilir; yayın öncesi CLA workflow ayrıca kontrol edilmeli |
| `commercial-legal` | tamamlandı - ilk tur + kavram senkronu | README, CLAUDE, 12 skill, 3 agent, renewal register ve MCP açıklamaları güncellendi; NDA/ticari kavram karşılıkları standardize edildi |
| `corporate-legal` | tamamlandı - ilk tur + referans senkronu | README, CLAUDE, audit, tüm skill'ler ve agent'lar Türkiye uygulamasına göre güncellendi; M&A diligence kolonları Türkiye regülatörleriyle derinleştirildi |
| `litigation-legal` | tamamlandı - ilk tur + unsur şablonu senkronu | README, CLAUDE, dava/intake/hold/müzekkere/isticvap-görgü tanığı/gizlilik/portföy/dış büro raporlama skill'leri ve docket-watcher UYAP pratiğine göre güncellendi; claim-chart referans unsurları Türk hukukuna çevrildi |
| `privacy-legal` | tamamlandı - ilk tur KVKK çekirdeği | README, CLAUDE, 9 skill, currency-watch, MCP ve marketplace açıklamaları KVKK/Kurul/VERBIS/aydınlatma/açık rıza/yurt dışına aktarım/ilgili kişi başvurusu pratiğine göre güncellendi |
| `employment-legal` | tamamlandı - ilk tur Türk iş hukuku çekirdeği | README, CLAUDE, 20 skill, leave-tracker agent, currency-watch, MCP ve marketplace açıklamaları İş Kanunu, SGK/İŞKUR/İSG, fesih/arabuluculuk, ücret/çalışma süresi, izin, iç soruşturma ve personel politikalarına göre güncellendi |
| `product-legal` | tamamlandı - ilk tur Türk ürün hukuku çekirdeği | README, CLAUDE, 7 skill, launch-watcher agent, currency-watch, MCP ve marketplace açıklamaları tüketici/e-ticaret, reklam, KVKK, sektör, ürün güvenliği ve AI kapılarına göre güncellendi |
| `regulatory-legal` | tamamlandı - ilk tur Türk regulatory çekirdeği | README, CLAUDE, 9 skill, reg-change-monitor agent, source catalog, gap/comment tracker, MCP ve marketplace açıklamaları Resmi Gazete/Mevzuat, KVKK, Rekabet, SPK, BDDK, BTK, EPDK, TCMB, Ticaret Bakanlığı, MASAK ve sektör kaynaklarına göre güncellendi |
| `managed-agent-cookbooks` | tamamlandı - ilk tur YAML/cookbook çekirdeği | Docket watcher allowlist'i UYAP/Yargı MCP çizgisine; reg monitor kaynak allowlist'i Resmi Gazete/Mevzuat/KVKK/Rekabet/SPK/BDDK/BTK/EPDK/TCMB/Ticaret/MASAK/TİTCK çizgisine alındı (Başka işlevsel araç olmadığı için sadece MCP Yargı entegre edildi) |
| `ip-legal` | uyarlandı | Türk fikri mülkiyet pratiğine göre uyarlandı. |
| `ai-governance-legal` | başlangıç uyarlaması | Vendor AI review ve use-case triage Türkiye/KVKK/FSEK/TTK çizgisine çekildi; bu alan ikinci fazda geliştirilecek. |
| `legal-builder-hub` | teknik/meta araç | Hukuki içerik modülü olmadığı için ana uyarlama kapsamı dışında tutuldu; skill QA ve installer yapısı korundu. |

## Kaynaklardan Bekleyenler

| Kaynak | Muhtemel Hedef | Durum |
|---|---|---|
| `references/turkish-adaptation-sources/playbook önerilerini incele.txt` | `commercial-legal/skills/review-proposals/SKILL.md` | bekliyor |

## Genel Bekleyen Alanlar

- Privacy/KVKK için ikinci tur gerçek belge smoke test'i.
- Employment/İş hukuku için ikinci tur gerçek belge smoke test'i.
- Product/ürün hukuku için gerçek PRD, reklam metni, abonelik checkout, influencer brief'i ve cerez/tracking örnekleriyle ikinci tur smoke test'i.
- IP/FSEK, marka, patent, haksız rekabet uyarlamasının kalan skill temizliği: tamamlandı. Tüm IP skill dosyaları Türkiye mevzuatına (FSEK, SMK, 5651 vd.) entegre edildi.
- AI governance uyarlamasının kalan çekirdek temizliği: vendor/use-case katmanı uyarlanmış, ancak README/CLAUDE ve AIA/reg-gap/policy-starter dosyaları Türkiye yönetişim, KVKK, TTK ticari sır, FSEK ve sektör regülatörleri eksenine tamamlanmalı.
- `legal-builder-hub` uyarlanmadı: hukuki içerik modülü değil, teknik/meta araç olduğu için kapsam dışında bırakıldı.
- `legal-clinic` bekleyen iş değildir: Türkiye'de doğrudan karşılığı olmayan US law school clinic modeli olduğu için ayrık/kapsam dışı tutulacak. İhtiyaç doğarsa ayrı klinik/adli yardım plugin'i sıfırdan tasarlanmalı.
- Regulatory/SPK, BDDK, BTK, EPDK, Rekabet Kurumu için gerçek kaynak ve politika kütüphanesiyle ikinci tur smoke test'i.
- Managed-agent cookbook'lar için gerçek UYAP/Yargı MCP ve Türkiye düzenleyici kaynak bağlantılarıyla ikinci tur smoke test'i. (Mevcut entegrasyon yalnızca Yargı MCP ile sınırlıdır, başkaca bir yerel MCP aracı bulunmamaktadır).
- `law-student` bekleyen iş değildir: ABD hukuk eğitimi/bar prep yapısı Türk sistemle uyumsuz olduğu için kapsam dışı bırakıldı. İhtiyaç doğarsa ayrı Türk hukuk öğrencisi plugin'i sıfırdan tasarlanmalı.
- README tablolarının tüm pluginler için ayrıntılı Türkçe karşılıkları.
- Marketplace açıklamalarının tüm pluginler için Türkçe ve kapsam dürüstlüğüyle güncellenmesi.
