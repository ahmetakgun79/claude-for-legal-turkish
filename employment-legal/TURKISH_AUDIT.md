# employment-legal - Türk Hukuku Uyarlama Denetimi

Durum: `Tamamlandı - ilk tur Türk iş hukuku çekirdeği`

Bu klasör orijinalde yabancı employment law mantığıyla kuruluydu. Türk uyarlamada komut adları korunur; içerik 4857 sayılı İş Kanunu, 7036 sayılı İş Mahkemeleri Kanunu, SGK/İŞKUR uygulamaları, 6331 sayılı İSG, 6356 sayılı sendika/TİS, KVKK/çalışan verisi ve Türkiye iş mahkemesi/arabuluculuk pratiğine göre yeniden kuruldu.

## Genel Karar

| Bileşen | Karar | Gerekçe | İlk tur durumu |
|---|---|---|---|
| `README.md` | Değişmeli | Yabancı yerel iş hukuku dili vardı. | Güncellendi |
| `CLAUDE.md` | Değişmeli | Yabancı çalışma ürünü, serbest fesih ve eyalet footprint varsayımlıydı. | Güncellendi |
| `.mcp.json` | Kısmen değişmeli | Teknik connector yapısı kalabilir; açıklamalar İK/hukuk belgelerine çekilmeli. | Güncellendi |
| `.claude-plugin/plugin.json` | Kısmen değişmeli | Plugin açıklaması yabancı jurisdiction-specific risk dilindeydi. | Güncellendi |
| `references/currency-watch.md` | Eklenmeli | Asgari ücret, SGK, kıdem tavanı ve arabuluculuk değişkenleri için watch list gerekir. | Güncellendi |
| `agents/leave-tracker.md` | Değişmeli | Yabancı leave rejimleri yerine yıllık izin, rapor, doğum ve Türkiye izin kayıtları. | Güncellendi |

## Skill Matrisi

| Skill | Karar | Türk uyarlama notu | İlk tur durumu |
|---|---|---|---|
| `cold-start-interview` | Değişmeli | İşyeri, çalışan grubu, SGK/İŞKUR/İSG, sendika/TİS, fesih ve izin profili kurulmalı. | Güncellendi |
| `hiring-review` | Değişmeli | Offer/serbest fesih dili yerine iş sözleşmesi, deneme süresi, SGK, KVKK, rekabet yasağı. | Güncellendi |
| `termination-review` | Değişmeli | Yabancı fesih/bildirim varsayımları yerine geçerli/haklı fesih, iş güvencesi, savunma, kıdem/ihbar, SGK kodu, arabuluculuk. | Güncellendi |
| `wage-hour-qa` | Değişmeli | Yabancı ücret/mesai rejimi yerine İş Kanunu çalışma süresi, fazla çalışma, UBGT, hafta tatili ve bordro. | Güncellendi |
| `worker-classification` | Değişmeli | Yabancı contractor/state test yerine işçi, bağımsız çalışan, alt işveren, geçici iş ilişkisi ve SGK riski. | Güncellendi |
| `leave-tracker` / `log-leave` | Değişmeli | Yabancı leave dili yerine yıllık izin, rapor, doğum, ücretsiz izin ve dönüş tarihleri. | Güncellendi |
| `policy-drafting` / `handbook-updates` | Değişmeli | Eyalet supplement mantığı yerine personel yönetmeliği, disiplin, KVKK, uzaktan çalışma, İSG. | Güncellendi |
| `internal-investigation` ve `investigation-*` | Değişmeli | Yabancı kurum/şikayet dili yerine mobbing, taciz, disiplin, haklı fesih, KVKK ve delil saklama. | Güncellendi |
| `international-expansion` / `expansion-*` | Kısmen değişmeli | Yeni ülke mantığı kalır; Türkiye'de istihdam ve Türkiye dışı çalışan için yerel danışman kapısı. | Güncellendi |
| `customize` | Değişmeli | Profil özelleştirmesi Türk iş hukuku alanlarına göre güncellenmeli. | Güncellendi |
| `matter-workspace` | Kısmen değişmeli | Dosya izolasyonu kalır; iş hukuku matter alanları eklenmeli. | Güncellendi |

## Kapatılacak Varsayımlar

- Yabancı serbest fesih, leave/mesai ve eyalet ücret rejimi varsayımları kaldırıldı.
- Eski İngilizce çıktı bölümü ve çalışma ürünü başlığı referansları `## Çıktı Kuralları` ve Türkçe gizli çalışma başlığına bağlandı.
- Kaynak etiketi yabancı araştırma aracı varsayımından Mevzuat.gov.tr, Resmi Gazete, ÇSGB, SGK, İŞKUR, Yargıtay/AYM/UYAP ve Türk hukuk araştırma araçlarına çevrildi.
