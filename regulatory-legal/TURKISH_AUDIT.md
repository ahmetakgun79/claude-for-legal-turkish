# Regulatory Legal Turkish Audit

Durum: `Tamamlandı - ilk tur`.

## Çekirdek Karar

Orijinal regulatory-legal yapısı yabancı resmî gazete, proposed rule ve ABD ağırlıklı kurum mantığına dayanıyordu. Türkiye sürümünde omurga Resmi Gazete, Mevzuat Bilgi Sistemi ve kurumun kendi resmi duyuru/karar sayfasıdır.

## Güncellenenler

| Alan | Durum | Not |
|---|---|---|
| README | tamamlandı | Türkiye regulatory kapsamı ve komut açıklamaları yazıldı |
| CLAUDE.md | tamamlandı | İzlenen kurumlar, kaynak etiketi, gap response ve çıktı kuralları Türkiye'ye çevrildi |
| plugin.json / .mcp.json | tamamlandı | Legal Turkish kimliği ve connector açıklamaları güncellendi |
| reg-feed-watcher | tamamlandı | Resmi Gazete, Mevzuat, kurum kaynakları ve taslak/görüş ayrımı eklendi |
| policy-diff | tamamlandı | Yürürlük/statü doğrulama, yükümlülük çıkarma ve gap tipleri Türkiye akışına çevrildi |
| comments | tamamlandı | Yabancı proposed-rule terminolojisi yerine taslak düzenleme/kamuoyu görüşü takibi yapıyor |
| gaps / gap-surfacer | tamamlandı | Gap tracker, doğrulanmamış statü ve bildirim onayı Türkiye pratiğine çevrildi |
| policy-redraft | tamamlandı | Onaylı politika üzerine yazmadan öneri redraft memo'su üretir |
| customize / matter-workspace / cold-start | tamamlandı | Türkiye regulatory profil ayarları ve matter ayrımı eklendi |
| reg-change-monitor agent | tamamlandı | Türkiye digest ajanı olarak yeniden yazıldı |
| source-catalog | tamamlandı | Türkiye resmi kurum kaynakları kataloğu eklendi |
| tracker YAML'leri | tamamlandı | Gap ve taslak/görüş örnekleri güncellendi |

## Kullanılan Ana Kaynak Omurgası

- Resmi Gazete
- Mevzuat Bilgi Sistemi
- KVKK
- Rekabet Kurumu
- SPK
- BDDK
- BTK
- EPDK
- TCMB
- Ticaret Bakanlığı
- MASAK
- TİTCK

## Kalan İş

- Gerçek kurum duyurusu ve Resmi Gazete metniyle kaynak izleme smoke test.
- Canlı politika kütüphanesiyle policy-diff ve gap tracker smoke test.
- Kaynak URL'leri müşterinin sektörüne göre daraltma.
