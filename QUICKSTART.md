# Quick Start - Legal Turkish

Bu klasör, Türk hukuku adaptasyonunun bağımsız çalışma kopyasıdır.

## 1. Marketplace Olarak Ekle

Claude Code içinde:






```text
/plugin marketplace add C:\Users\hukuk\.gemini\antigravity\scratch\claude legal\Legal Turkish
```

Yol farklıysa `Legal Turkish` klasörünü terminale sürükleyebilirsiniz.

## 2. Plugin Kur

Örnek:

```text
/plugin install commercial-legal@legal-turkish
```

veya:

```text
/plugin install litigation-legal@legal-turkish
```

## 3. Claude Code'u Yeniden Başlat

Plugin komutları yeniden başlatmadan görünmeyebilir.

## 4. Başlangıç Mülakatını Çalıştır

Ticari hukuk için:

```text
/commercial-legal:cold-start-interview
```

Dava / ihtarname / uyuşmazlık işleri için:

```text
/litigation-legal:cold-start-interview
```

## 5. İlk Komutlar

Ticari sözleşme:

```text
/commercial-legal:review
```

Gizlilik sözleşmesi:

```text
/commercial-legal:review
```

Yenileme takibi:

```text
/commercial-legal:renewal-tracker
```

İhtarname ön hazırlık:

```text
/litigation-legal:demand-intake
```

İhtarname taslak:

```text
/litigation-legal:demand-draft <slug>
```

## 6. Hangi Dosyaya Bakılır?

| İhtiyaç | Bakılacak dosya |
|---|---|
| Repo'nun genel amacı ve kapsamı | `README.md` |
| Kurulumun en kısa yolu | `QUICKSTART.md` |
| Hangi alanların Türk hukukuna uyarlandığı | `TURKISH_ADAPTATION_STATUS.md` |
| Klasör bazında neden değişiklik yapıldığı | `TURKISH_FOLDER_AUDIT.md` |
| Bir plugin'in komutları ve guardrail'leri | `<plugin>/README.md` |
| Claude'un alan profilini ve çıktı kurallarını değiştirmek | `<plugin>/CLAUDE.md` |
| Tek bir komutun davranışını güncellemek | `<plugin>/skills/<skill>/SKILL.md` |
| İzleme veya zamanlı rapor ajanını güncellemek | `<plugin>/agents/<agent>.md` |
| Kaynak, şablon veya tracker örneğini değiştirmek | `<plugin>/references/*` veya `references/*` |

Güncelleme yaparken `SKILL.md` dosyalarında kullanıcıya görünen hukukî açıklamaları Türkçe tutun; klasör, komut ve yapılandırma adlarını ise repo genelinde yeniden adlandırma kararı alınmadıkça değiştirmeyin.

## Not

Komut adları şimdilik orijinal repo ile uyumlu kalır. Türkçeleştirme hukuki içerikte ve çıktı dilindedir. Komut adlarını `/ticari-hukuk:*` gibi Türkçeleştirmek istersek bu ayrı bir repo-geneli yeniden adlandırma işidir.
