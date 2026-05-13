# Managed Agent Cookbooks Turkish Audit

Durum: `Tamamlandı - ilk tur`.

## Kapsam

Bu klasördeki YAML manifestleri otonom alt-ajanların davranışını, izinlerini, veri kaynaklarını, güvenli domain sınırlarını ve çıktı şemalarını belirler. Prompt/skill düzeyi temiz olsa bile bu katmanda kalan yabancı kaynak veya prosedür varsayımı ajanı yanlış çalıştırabilir.

## Kontrol Edilen Cookbook'lar

| Cookbook | Durum | Not |
|---|---|---|
| `docket-watcher` | tamamlandı | UYAP/Yargı MCP/Lexpera çizgisine alındı; eski yabancı mahkeme domain allowlist'i temizlendi |
| `reg-monitor` | tamamlandı | Resmi Gazete, Mevzuat ve Türkiye kurum kaynakları allowlist'e alındı |
| `launch-radar` | kontrol edildi | Product/legal risk sınıflandırması genel kalıyor; Türk product skill'lerine bağlı çalışır |
| `renewal-watcher` | kontrol edildi | Ticari sözleşme yenileme mantığıyla uyumlu; para birimi alanı teknik numeric alan olarak bırakıldı |
| `diligence-grid` | kontrol edildi | M&A diligence grid ajan mimarisi genel; Türk corporate skill'leriyle çalışır |

## Yapılan Kritik Düzeltmeler

- `docket-watcher/subagents/docket-reader.yaml` içindeki `doc_url` güvenli domain pattern'i `uyap.gov.tr`, `lexpera.com.tr`, `yargimcp.surucu.dev` ile sınırlandı.
- `docket-watcher/subagents/deadline-mapper.yaml` içindeki yabancı kural numarası izi taşıyan örnek Türkiye usul rejimleri için nötr hale getirildi.
- `reg-monitor/subagents/feed-reader.yaml` içindeki egress allowlist `resmigazete.gov.tr`, `mevzuat.gov.tr`, `kvkk.gov.tr`, `rekabet.gov.tr`, `spk.gov.tr`, `bddk.org.tr`, `btk.gov.tr`, `epdk.gov.tr`, `tcmb.gov.tr`, `ticaret.gov.tr`, `masak.hmb.gov.tr`, `titck.gov.tr` çizgisine alındı.
- `reg-monitor/subagents/digest-writer.yaml` içindeki örnek kaynak URL'si Resmi Gazete örneğine çevrildi.

## Doğrulama

YAML dosyalarında yabancı usul kuralları, yabancı mahkeme kaynakları, yabancı düzenleyici kaynaklar, yabancı hukuk veri tabanı adları ve ABD hukuk eğitimi sınav terminolojisi için kalıntı taraması yapıldı; temiz sonuç alındı.

## Kalan İş

İkinci turda gerçek bağlantılarla smoke test yapılmalı:

- UYAP MCP
- Yargı MCP / Danıştay modülü
- Lexpera veya kurum içi hukuk veritabanı
- Türkiye düzenleyici kurum kaynakları
