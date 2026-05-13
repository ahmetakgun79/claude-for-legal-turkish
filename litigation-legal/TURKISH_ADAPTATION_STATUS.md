# Türk Hukuku Adaptasyon Durumu (Turkish Legal Adaptation Status)

Bu belge, `litigation-legal` eklentisinin Türk hukukuna (HMK, CMK, Av.K., KVKK, Rekabet) uyarlanma sürecini ve güncel durumunu özetler.

## Tamamlanan Modüller (Completed)

| Modül/Dosya | Adaptasyon Kapsamı (Turkish Context) | Durum |
|---|---|---|
| `README.md` | UYAP, KEP, HMK bağlamında genel rehberlik eklendi. | ✅ Tamamlandı |
| `CLAUDE.md` | Risk/Önem kalibrasyonu (KVKK/Rekabet Cezaları, KAP, UYAP/Bilirkişi süreçleri) ve Av.K. m.36 uyarınca gizlilik kuralları yerelleştirildi; kaynak etiketleri Lexpera/Lextera/Kazancı/UYAP/Mevzuat.gov.tr/Resmî Gazete standardına çevrildi. | ✅ Tamamlandı |
| `skills/matter-intake` | Arabuluculuk dava şartı, yetki/görev itirazları, harca esas değer ve Dava Değeri kavramları eklendi. | ✅ Tamamlandı |
| `skills/legal-hold` | Amerikan "Spoliation" doktrini yerine, HMK 400 "Delil Tespiti" ve TTK "Basiretli Tacir" delil muhafaza yükümlülüğü getirildi. | ✅ Tamamlandı |
| `skills/subpoena-triage` | Mahkeme Müzekkeresi (HMK 219), Savcılık (CMK 332) ve İdari Kurum (Rekabet/KVKK) bilgi isteme usullerine göre yeniden tasarlandı. | ✅ Tamamlandı |
| `skills/deposition-prep` | Amerikan "Deposition" (ifade alma) yapısı, Türk hukukundaki **İsticvap (HMK 169)** ve **Tanık Dinletme (HMK 240)** sistemine çevrildi. | ✅ Tamamlandı |
| `skills/privilege-log-review` | Avukat-Müvekkil Gizliliği (Av.K. m.36) ve Rekabet Kurumu "Şirket içi avukat (in-house)" istisnası çerçevesinde yerelleştirildi. | ✅ Tamamlandı |
| `skills/portfolio-status` | Dava aşamaları (İstinaf, Temyiz, Tahkikat) ve UYAP üzerinden risk raporlama diline çevrildi. | ✅ Tamamlandı |
| `skills/oc-status` | Dış hukuk bürolarından istenecek haftalık UYAP safahat raporlaması, harç/avans bütçe takip modeline göre ayarlandı. | ✅ Tamamlandı |
| `skills/claim-chart/references/element-templates.md` | ABD common-law unsur şablonları kaldırıldı; TBK sözleşmeye aykırılık, temerrüt, cezai şart, haksız fiil, sebepsiz zenginleşme, TTK haksız rekabet/ticari sır, iş uyuşmazlığı, KVKK ve usul kapıları için Türk hukuk unsur şablonları yazıldı. | ✅ Tamamlandı |
| `skills/matter-workspace` | Yabancı hukuk/Delaware örneği kaldırıldı; Türk hukuku ve yabancı hukuk/tahkim eskalasyonu örneğine çevrildi. | ✅ Tamamlandı |
| `agents/docket-watcher` | Amerikan PACER/Trellis sistemi yerine **UYAP Evrak ve Duruşma Takibi**, e-Tebligat ve HMK kesin süre takibi konseptine geçirildi. | ✅ Tamamlandı |
| `inbound/_README.md` | Gelen evrakların (İhtarname, Müzekkere) triyaj açıklamaları güncellendi. | ✅ Tamamlandı |
| `demand-letters/_README.md` | Giden İhtarname (Noter/KEP) taslaklarının kayıt süreçleri güncellendi. | ✅ Tamamlandı |
| `matters/_README.md` | Dava/Dosya portföyü dizin yapısının UYAP kütüğü formatında kullanımı açıklandı. | ✅ Tamamlandı |

## Güvenlik ve Mimari Kararları (Architecture & Safety)
1. **İnsan-Devrede (Human-in-the-loop):** Kesin süre hesaplama, gizlilik (privilege) bayraklama ve evrak gönderme (MCP entegrasyonlarıyla Gmail vb.) gibi işlemlerde nihai kararın (onayın) ruhsatlı avukatta olması "gate" (kapı) mekanizmalarıyla güçlendirildi.
2. **Kavramsal Doğruluk:** ABD usulündeki kavramlar doğrudan çevrilmemiş, Türk Hukuku karşılıklarıyla (Örn: Subpoena -> Müzekkere) değiştirilmiş ve açıklamaları eklenmiştir.

## Sistem Durumu
Tüm çekirdek modüller, klasör açıklamaları (`_README.md`), ajanlar ve yetenekler (skills) tamamen Türk hukuk pratiğine uyarlanmıştır. Sistem kararlı durumdadır (Stable/Production-Ready).
