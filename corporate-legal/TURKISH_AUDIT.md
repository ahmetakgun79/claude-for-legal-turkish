# corporate-legal - Türk Hukuku Uyarlama Denetimi

Durum: `Kısmen tamamlandı - ilk tur; çıktı ve yapısal veri dili senkronizasyonu yapıldı`

Bu klasör, orijinal projede ABD şirketler hukuku, Delaware/eyalet bazlı şirket kayıtları, SEC halka açık şirket uyumu ve board written consent pratiği üzerine kuruluydu. Türk uyarlamada teknik iskelet korunur; hukuki içerik TTK, sermaye piyasası mevzuatı, ticaret sicili/MERSİS, karar defterleri, imza ve temsil yetkisi, Rekabet Kurumu, KVKK ve Türkiye M&A uygulamasına göre yeniden kurulur.

## Genel Karar

| Bileşen | Karar | Gerekçe | İlk tur durumu |
|---|---|---|---|
| `README.md` | Değişmeli | Kullanıcıya görünen açıklama ABD modüllerini anlatıyordu. | Güncellendi |
| `CLAUDE.md` | Değişmeli | Pratik profili Delaware/SEC/US work-product varsayımlıydı. | Güncellendi |
| `.mcp.json` | Kısmen değişmeli | Connector yapısı teknik olarak kalabilir; açıklamalar ileride Türkiye kaynaklarıyla zenginleştirilebilir. | Bekliyor |
| `.claude-plugin/` | Kısmen değişmeli | Plugin metadata teknik; kapsam açıklamaları marketplace düzeyinde ayrıca ele alınacak. | Güncellendi |
| `hooks/` | Kalabilir | Hukuki içerik taşımıyor. | Şimdilik dokunulmadı |
| `agents/dataroom-watcher.md` | Değişmeli | VDR izleme mantığı kalır; risk kategorileri Türkiye M&A, KVKK ve Rekabet pratiğine çevrilmeli. | Güncellendi |

## Skill Matrisi

| Skill | Karar | Türk uyarlama notu | İlk tur durumu |
|---|---|---|---|
| `cold-start-interview` | Değişmeli | Şirket türü, modül seçimi, M&A, kurumsal yönetim, halka açık şirket ve entity management soruları Türkiye için yeniden yazılmalı. | Güncellendi |
| `written-consent` | Değişmeli | ABD `unanimous written consent` kavramı birebir taşınamaz; yönetim kurulu, müdürler kurulu, genel kurul ve toplantısız/sirküler karar taslaklama akışına çevrilmeli. | Güncellendi |
| `entity-compliance` | Değişmeli | Secretary of State, franchise tax, good standing yerine MERSİS, ticaret sicili, karar defterleri, imza sirküleri, KEP, VERBİS, vergi/SGK ve faaliyet belgesi takibi kurulmalı; tracker şeması canonical `english_snake_case` olmalı. | Güncellendi |
| `board-minutes` | Değişmeli | Quorum, notice, charter/bylaws dili yerine TTK, esas sözleşme, iç yönerge, karar defteri ve toplantı tutanağı formaliteleri kullanılmalı. | Güncellendi |
| `closing-checklist` | Değişmeli | Certificate of good standing, 280G, Delaware/New York MAC örnekleri Türkiye M&A kapanış belgelerine çevrilmeli. | Güncellendi |
| `diligence-issue-extraction` | Değişmeli | Hisse/pay devri, birleşme/bölünme, rekabet izni, KVKK, çalışma, vergi, ruhsat ve ticaret sicili başlıkları eklenmeli. | Güncellendi |
| `material-contract-schedule` | Kısmen değişmeli | Disclosure schedule iskeleti kalabilir; sözleşme türleri, TL eşikleri, Türk bildirim/imza yetkisi kontrolleri eklenmeli; insan-facing tablo başlıkları Türkçe olmalı. | Güncellendi |
| `tabular-review` | Kısmen değişmeli | Tablo review tekniği kalabilir; örnek kolonlar ve risk başlıkları Türkiye’ye çevrilmeli. | Çıktı referansı ve M&A kolon referansı düzeltildi |
| `deal-team-summary` | Kısmen değişmeli | İş birimi özeti mantığı kalır; karar ve eskalasyon dili Türk şirket içi uygulamasına çevrilmeli. | Çıktı referansı düzeltildi |
| `integration-management` | Değişmeli | Post-closing integration kalır; sicil, MERSİS, çalışan, KVKK, sözleşme devri ve bildirim akışı Türkiye’ye göre yazılmalı; tracker alanları canonical `english_snake_case` standardında kalmalı. | Güncellendi |
| `ai-tool-handoff` | Kısmen değişmeli | Kira/Luminance gibi araç mantığı kalır; QA kriterleri Türk risk kategorilerine bağlanmalı. | Çıktı referansı düzeltildi |
| `customize` | Kısmen değişmeli | Profil özelleştirme kalır; TTK/SPK/KVKK/Rekabet eşikleri ve onay matrisi eklenmeli. | Bekliyor |
| `matter-workspace` | Kalabilir / küçük değişiklik | Dosya izolasyonu teknik olarak yararlı; Türk dosya alanları istenirse sonraki turda eklenir. | Çıktı referansı düzeltildi |

## İlk Turda Kapatılan ABD Varsayımları

- `Public Company` modülü SEC/NYSE/Nasdaq yerine SPK, Borsa İstanbul, KAP, MKK ve özel durum açıklaması çerçevesine taşındı.
- `written consent` komutu içeride Türk karar taslağı işlevine çevrildi; komut adı geriye dönük uyumluluk için korundu.
- `entity-compliance` Delaware/Secretary of State mantığından çıkarıldı; Türkiye kaynakları ve kayıt takibi esas alındı.
- `board-minutes` ABD board minutes dilinden çıkarıldı; yönetim kurulu, müdürler kurulu, genel kurul ve komite tutanak/karar taslağı akışına çevrildi.
- `diligence-issue-extraction` HSR/CFIUS/280G/stockholder-consent ağırlığından çıkarıldı; Türk M&A due diligence kategorileri, Rekabet Kurumu, KVKK, ticaret sicili, imza yetkisi, çalışan/SGK, vergi, ruhsat ve uyuşmazlık kontrolleriyle yeniden yazıldı.
- `closing-checklist` HSR/good standing/Delaware MAC/280G örneklerinden çıkarıldı; organ kararları, ticaret sicili/MERSİS, Rekabet, SPK/KAP/MKK, sözleşme onayları, teminat fekki, KVKK, ruhsat, vergi/SGK ve kapanış kanıtlarıyla yeniden yazıldı.
- `material-contract-schedule`, `integration-management` ve `agents/dataroom-watcher.md` dosyalarının Türkiye M&A pratiğine uyarlanmış olduğu doğrulandı.
- `tabular-review`, `deal-team-summary`, `ai-tool-handoff`, `matter-workspace`, `excel-output.md` ve `gsheets-output.md` içindeki eski `## Outputs` / `[WORK-PRODUCT HEADER]` referansları yeni `## Çıktı kuralları` ve Türkçe gizli çalışma başlığıyla senkronize edildi.
- Plugin içi yapısal veri dili standardı belirlendi: YAML/JSON/tracker/CSV aktarım alanları canonical ASCII `english_snake_case`, kullanıcıya görünen tablo ve rapor başlıkları Türkçe. `entity-compliance`, `integration-management` ve `material-contract-schedule` bu standarda göre senkronize edildi.
- `tabular-review/references/ma-diligence-columns.md` içindeki FDA/FAR/DFARS/FINRA/SEC odaklı kolon ve sektör ekleri Türkiye M&A pratiğine çevrildi; TİTCK, KİK, SPK, BDDK, TCMB, BTK, EPDK, Rekabet, KVKK, DVK ve kamu ihale sözleşmeleri kontrolleri eklendi.
- Çıktı başlıkları `attorney work product` yerine Türk uygulamasında daha dürüst olan `Gizli hukuki çalışma taslağı / avukat incelemesine tabi` diline alındı.

## Kalan Öncelikler

1. `customize`, `tabular-review`, `deal-team-summary` ve `ai-tool-handoff` dosyalarında ikinci tur terminoloji ve örnek yerelleştirmesi yapılabilir.
2. `.mcp.json` açıklamalarına Türkiye kaynakları, KAP, MERSİS/Ticaret Sicili, KEP/UETS ve belge arşivi notları eklemek.
3. `tabular-review`, `deal-team-summary`, `ai-tool-handoff` dosyalarında ikinci tur örnek çıktı smoke test'i yapılabilir.
