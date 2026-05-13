# commercial-legal - Türk Hukuku Uyarlama Denetimi

Bu dosya `commercial-legal` klasörünün Türk hukuku ve Türkiye ticari sözleşme pratiğine uyarlama durumunu izler.

## Genel Karar

Durum: `Tamamlandı - ilk tur; kavram karşılığı ikinci tur senkronizasyonu yapıldı`.

Ana ticari sözleşme skill'leri, profil template'i, başlangıç mülakatı, README, proposal/agent akışları ve entegrasyon açıklamaları Türk sürümle uyumlu hale getirildi. `residuals`, `survival`, damga vergisi, cezai şart ve arabuluculuk kavramları Türk hukuk karşılıklarıyla standardize edildi. İleride gerçek sözleşmelerle örnek çıktı testleri genişletilebilir.

## Dosya Matrisi

| Yol | Karar | Durum | Not |
|---|---|---|---|
| `README.md` | Değişmeli | tamamlandı - ilk tur | Türk sürüm kimliği, komutlar, guardrail'ler ve skill durumu yazıldı. |
| `CLAUDE.md` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | Türk hukuk playbook alanlarıyla yeniden yazıldı; residuals/hafızada kalan bilgi, bakiye hükümler, damga vergisi, TBK m.179-185, TBK m.19/27/28 ve 6325 arabuluculuk notları eklendi. |
| `.mcp.json` | Kısmen değişmeli | tamamlandı - ilk tur | Connector açıklamalarına Legal Turkish ve opsiyonellik notları eklendi. |
| `.gitignore` | Kalabilir | tamam | Teknik dosya. |
| `hooks/hooks.json` | Kalabilir | tamam | Boş hook tanımı. |
| `logs/` | Kalabilir | tamam | Runtime/log alanı. |

## Skill Matrisi

| Skill | Karar | Durum | Not |
|---|---|---|---|
| `review` | Değişmeli | tamamlandı - ilk tur | Türk hukuk router mantığı işlendi. |
| `nda-review` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | GS/NDA, KVKK, rekabet, imza yetkisi işlendi; residuals/hafızada kalan bilgi ve bakiye hükümler Türk hukuk riskleriyle açıklandı. |
| `vendor-agreement-review` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | Tedarikçi sözleşmesi Türk ticari pratik kontrolleri işlendi; TBK m.179-185 cezai şart ve DVK damga vergisi eskalasyonu eklendi. |
| `saas-msa-review` | Değişmeli | tamamlandı - ilk tur | SaaS, KVKK, alt işleyen, yenileme handoff işlendi. |
| `stakeholder-summary` | Değişmeli | tamamlandı - ilk tur | İş birimi özeti ve arındırma kuralları işlendi. |
| `renewal-tracker` | Değişmeli | tamamlandı - ilk tur | KEP/noter/TTK m.18/3 ve tarih ayrımı işlendi. |
| `amendment-history` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | Ek protokol/zeyilname/devir/temlik mantığı işlendi; damga vergisi (DVK/488) ve TBK m.179-185 cezai şart izleme kalemleri eklendi. |
| `customize` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | Türk profil alanları ve guardrail değişiklikleri işlendi; bakiye hükümler, residuals/hafızada kalan bilgi, DVK ve 6325 alanları eklendi. |
| `escalation-flagger` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | TL eşik, imza yetkisi, otomatik eskalasyonlar işlendi; DVK, TBK m.179-185 ve arabuluculuk/dava şartı tetikleri eklendi. |
| `matter-workspace` | Değişmeli | tamamlandı - ilk tur | Müvekkil, vekalet, UYAP-if-applicable, arabuluculuk, conflicts statüsü işlendi. |
| `cold-start-interview` | Değişmeli | tamamlandı - ilk tur + kavram senkronu | Türk commercial profile kurulumunu yazacak şekilde yeniden yazıldı; residuals, bakiye hükümler, DVK, cezai şart ve 6325 soruları eklendi. |
| `review-proposals` | Kısmen değişmeli | tamamlandı - ilk tur | Türkçe onay akışı ve high-impact guardrail'ler eklendi. |

## Agent Matrisi

| Agent | Karar | Durum | Not |
|---|---|---|---|
| `renewal-watcher` | Kısmen değişmeli | tamamlandı - ilk tur | Türk yenileme tracker ve send-by-effective mantığıyla uyumlu hale getirildi. |
| `deal-debrief` | Kısmen değişmeli | tamamlandı - ilk tur | Türk sözleşme risk kategorileri ve deviation log şeması eklendi. |
| `playbook-monitor` | Kısmen değişmeli | tamamlandı - ilk tur | Türkçe proposal ve high-impact attorney gate mantığı eklendi. |

## Öncelik

1. İkinci turda örnek outputların test edilmesi.
2. Gerçek bir Türk NDA / tedarikçi sözleşmesi ile smoke test.
3. Agent outputlarının scheduled-job formatına göre ayrıca denenmesi.
4. Commercial README'in root README plugin tablosuyla senkronize edilmesi.
