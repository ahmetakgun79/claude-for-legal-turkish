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

## Not

Komut adları şimdilik orijinal repo ile uyumlu kalır. Türkçeleştirme hukuki içerikte ve çıktı dilindedir. Komut adlarını `/ticari-hukuk:*` gibi Türkçeleştirmek istersek bu ayrı bir repo-geneli yeniden adlandırma işidir.

