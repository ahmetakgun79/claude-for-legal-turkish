# privacy-legal - Türk Hukuku Uyarlama Denetimi

Durum: `Tamamlandı - ilk tur KVKK çekirdeği`

Bu klasör orijinalde AB/ABD privacy programları üzerine kuruluydu. Türk uyarlamada teknik iskelet korunur; hukuki içerik 6698 sayılı KVKK, Kişisel Verileri Koruma Kurumu/Kurul uygulaması, VERBIS, aydınlatma/açık rıza, özel nitelikli veri, yurt dışına aktarım, veri ihlali bildirimi, çerez/ETK/İYS ve Türkiye sektör regülasyonlarına göre yeniden kuruldu.

## Genel Karar

| Bileşen | Karar | Gerekçe | İlk tur durumu |
|---|---|---|---|
| `README.md` | Değişmeli | Kullanıcıya görünen açıklama yabancı privacy terminolojisiydi. | Güncellendi |
| `CLAUDE.md` | Değişmeli | Profil yabancı privacy ve US work-product varsayımlıydı. | Güncellendi |
| `.mcp.json` | Kısmen değişmeli | Teknik connector yapısı kalabilir; açıklamalar KVKK belge/kaynak kullanımına çekilmeli. | Güncellendi |
| `.claude-plugin/plugin.json` | Kısmen değişmeli | Plugin açıklaması eski yabancı erişim talebi/veri işleme eki dilini taşıyordu. | Güncellendi |
| `references/currency-watch.md` | Değişmeli | ABD privacy watch list yerine KVKK/Kurul/yurt dışı aktarım watch list gerekir. | Güncellendi |
| `hooks/` | Kalabilir | Hukuki içerik taşımıyor. | Dokunulmadı |

## Skill Matrisi

| Skill | Karar | Türk uyarlama notu | İlk tur durumu |
|---|---|---|---|
| `cold-start-interview` | Değişmeli | KVKK profil kurulumu, rol, VERBIS, envanter, aktarım, ihlal ve politika soruları yazılmalı. | Güncellendi |
| `use-case-triage` | Değişmeli | Yabancı etki değerlendirmesi/consumer privacy sınıflaması yerine KVKK işleme şartı, VKED, aktarım ve STOP kapısı kurulmalı. | Güncellendi |
| `pia-generation` | Değişmeli | PIA formatı VKED / kişisel veri işleme değerlendirmesi olarak kurulmalı. | Güncellendi |
| `dpa-review` | Değişmeli | DPA dili veri işleyen sözleşmesi, veri sorumluları arası aktarım ve KVKK m.9 mekanizmalarına çevrilmeli. | Güncellendi |
| `dsar-response` | Değişmeli | Yabancı erişim talebi dili yerine ilgili kişi başvurusu, KVKK m.11/m.13 ve 30 gün yanıt akışı kurulmalı. | Güncellendi |
| `reg-gap-analysis` | Değişmeli | State privacy law / yabancı regülasyon delta yerine KVKK/Kurul/Resmi Gazete gap analizi kurulmalı. | Güncellendi |
| `policy-monitor` | Değişmeli | Privacy policy drift; aydınlatma, çerez, İYS, VERBIS, envanter ve uygulama çıktılarıyla karşılaştırılmalı. | Güncellendi |
| `customize` | Değişmeli | Profil özelleştirmesi KVKK alanlarına göre güncellenmeli. | Güncellendi |
| `matter-workspace` | Kısmen değişmeli | Dosya izolasyonu kalır; veri minimizasyonu ve KVKK matter alanları eklenmeli. | Güncellendi |

## Kapatılan Varsayımlar

- Zorunlu yabancı etki değerlendirmesi ve erişim talebi terminolojisi Türk akışlarında varsayılan olmaktan çıkarıldı.
- `dsar-response` işlevi ilgili kişi başvurusu ve KVKK m.11/m.13 yanıt akışına çevrildi.
- `DPA` işlevi veri işleyen sözleşmesi, alt işleyen, güvenlik tedbirleri, ihlal bildirimi, silme/iade ve yurt dışı aktarım mekanizmalarına bağlandı.
- Yabancı privacy rejimleri yalnızca şirket ayak izinde açıkça varsa ikincil rejim olarak ele alınacak şekilde sınırlandı.
- Kaynak disiplini KVKK/Kurul, Mevzuat.gov.tr, Resmi Gazete, kullanıcı belgesi, sektör regülatörü ve Türk hukuk araştırma araçlarına çekildi.
- Eski İngilizce çıktı bölümü ve çalışma ürünü başlığı referansları yerine privacy skill'leri `## Çıktı Kuralları` ve Türkçe çalışma taslağı başlığını kullanıyor.

## İkinci Tur Önerileri

1. Gerçek aydınlatma metni, açık rıza metni ve DPA ile smoke test yapmak.
2. Yurt dışına aktarım için gerçek standart sözleşme/taahhüt örneği üzerinden redline kontrolü yapmak.
3. Veri ihlali senaryosu ve ilgili kişi başvurusu örneğiyle 30 gün/72 saat takibini uçtan uca denemek.
