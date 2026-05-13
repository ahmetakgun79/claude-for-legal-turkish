# Employment Legal Practice Profile - Legal Turkish Template

Bu profil, `employment-legal` skill'lerinin Türk iş hukuku ve uygulamasına göre çalışması için varsayılan çerçevedir. Kullanıcıya özel kurulumda `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` yoluna yazılır.

## Kurum ve İşyeri Profili

**İşveren / müvekkil:** [PLACEHOLDER]
**Sektör:** [PLACEHOLDER]
**İşyeri lokasyonları:** [PLACEHOLDER - şehir/işyeri/sicil]
**Çalışan grupları:** [PLACEHOLDER - beyaz yaka, mavi yaka, uzaktan, hibrit, saha, part-time, stajyer, yabancı çalışan]
**Çalışan sayısı ve iş güvencesi eşiği:** [PLACEHOLDER]
**Sendika / TİS durumu:** [PLACEHOLDER]
**Alt işveren / hizmet alımı / geçici iş ilişkisi:** [PLACEHOLDER]
**SGK / İŞKUR / İSG sorumluları:** [PLACEHOLDER]
**KVKK / çalışan verisi sorumluları:** [PLACEHOLDER]

## Kullanıcı Rolü

**Rol:** [Hukukçu / İK / yönetici / non-lawyer]
**Hukuk eskalasyonu:** [PLACEHOLDER]
**İK eskalasyonu:** [PLACEHOLDER]
**Dış hukuk bürosu:** [PLACEHOLDER]

Non-lawyer kullanıcı için skill'ler nihai işlem talimatı vermez; hukukçuya götürülecek kısa karar notu üretir.

## Çıktı Kuralları

İç hukuk/İK değerlendirme çıktılarının başına şu uyarıyı koy:

```text
GİZLİ HUKUKİ / İŞ HUKUKU ÇALIŞMA TASLAĞI - HUKUKÇU İNCELEMESİNE TABİDİR
```

Dışa gidecek çalışan yazısı, teklif, fesih bildirimi, savunma daveti veya politika metnine bu iç çalışma başlığını koyma. İç not ve dış taslak ayrı tutulur.

Her kritik çıktıda kısa reviewer note kullan:

```markdown
Reviewer note
- Kaynaklar:
- Okuma kapsamı:
- Doğrulanması gerekenler:
- Aksiyon öncesi:
```

## Kaynak ve Güncellik

Kaynak önceliği:

- Mevzuat.gov.tr ve Resmi Gazete,
- Çalışma ve Sosyal Güvenlik Bakanlığı,
- SGK, İŞKUR, Arabuluculuk Daire Başkanlığı,
- Yargıtay, Anayasa Mahkemesi, UYAP evrakı,
- Lexpera, Lextera, Kazancı veya kurum araştırma aracı,
- kullanıcı tarafından sağlanan sözleşme, bordro, SGK, personel dosyası ve politika belgeleri.

Asgari ücret, kıdem tazminatı tavanı, SGK/İŞKUR bildirim süreleri, idari para cezaları, İSG yükümlülükleri ve güncel içtihat başlıkları her çıktıda doğrulanacak değişken kabul edilir.

## İşe Alım ve Sözleşme Playbook

Kontrol kapıları:

- iş ilişkisi türü: belirsiz süreli, belirli süreli, kısmi süreli, uzaktan çalışma, çağrı üzerine, deneme süreli, stajyer/çırak, yabancı çalışma izni,
- iş sözleşmesinin yazılılığı ve zorunlu unsurlar,
- ücret, prim, yan hak, fazla çalışma onayı, deneme süresi,
- görev tanımı ve lokasyon,
- KVKK aydınlatma, açık rıza gerektiren haller, özlük dosyası,
- rekabet yasağı, gizlilik, fikri haklar, eğitim masrafı, cezai şart,
- SGK işe giriş, işyeri sicil ve bordro hazırlığı,
- background/reference check ve ayrımcılık riski.

## Ücret ve Çalışma Süresi

Kontrol kapıları:

- asgari ücret ve bordro kalemleri,
- fazla çalışma / fazla sürelerle çalışma,
- hafta tatili, ulusal bayram ve genel tatil,
- gece çalışması, vardiya, denkleştirme,
- prim/bonus/komisyon,
- uzaktan çalışma ve masraf,
- ücret kesintisi, avans, zimmet,
- bordro ihtirazi kayıt ve işçilik alacağı riski.

## İzin ve Devamsızlık

Kontrol kapıları:

- yıllık ücretli izin,
- hastalık/iş göremezlik raporu,
- analık, süt izni, ebeveynlik ve ücretsiz izin,
- mazeret izinleri,
- askerlik ve kamu görevleri,
- devamsızlık ihtarı ve haklı fesih riski,
- engellilik/sağlık uyarlaması ve ayrımcılık riski,
- izin kayıtları ve KVKK hassas veri.

## Fesih ve Arabuluculuk

Fesih incelemesinde şu kapılar zorunludur:

- fesih türü: istifa, ikale, işveren feshi, haklı nedenle derhal fesih, geçerli nedenle fesih, toplu işçi çıkarma,
- iş güvencesi kapsamı,
- yazılı bildirim ve gerekçe,
- savunma alma zorunluluğu / disiplin süreci,
- ihbar, kıdem, yıllık izin, ücret, fazla çalışma ve diğer alacaklar,
- SGK işten çıkış kodu,
- ibraname geçerliliği,
- işe iade ve işçilik alacakları bakımından zorunlu arabuluculuk,
- sendikal, hamilelik, sağlık, izin, şikayet, mobbing, ayrımcılık veya whistleblowing riski.

## İşyeri Politikaları

Tipik politika alanları:

- personel yönetmeliği,
- disiplin prosedürü,
- taciz/mobbing/ayrımcılık,
- uzaktan çalışma,
- bilgi güvenliği ve cihaz kullanımı,
- kamera/CCTV ve çalışan verisi,
- fazla çalışma onayı,
- masraf/yan hak,
- sosyal medya,
- çıkar çatışması ve hediye,
- iş sağlığı ve güvenliği.

## İç Soruşturma

Soruşturma guardrail'leri:

- iddia ve kapsam yazılı tanımlanır,
- delil ve görüşmeler kontrollü saklanır,
- çalışan verisi minimizasyonu yapılır,
- tanık/şikayetçi gizliliği korunur,
- haklı fesih ihtimali varsa öğrenme tarihi ve hak düşürücü süre ayrıca işaretlenir,
- disiplin yaptırımı öncesi savunma ve eşit işlem kontrol edilir,
- dışa gidecek özet iç hukuk değerlendirmesinden ayrılır.

## SGK / İŞKUR / İSG / KVKK Kapıları

- SGK işe giriş ve işten ayrılış bildirimi,
- muhtasar ve prim hizmet beyannamesi,
- İŞKUR işgücü çizelgesi, engelli/eski hükümlü yükümlülükleri, kısa çalışma veya teşvikler,
- 6331 sayılı İSG yükümlülükleri, iş kazası/meslek hastalığı bildirimi,
- çalışan verisi, sağlık verisi, kamera, e-posta izleme, biyometrik veri ve KVKK.

## Matter Workspaces

**Enabled:** [PLACEHOLDER - evet/hayır]
**Active matter:** none - practice-level context only
**Cross-matter context:** off
**Matters path:** `~/.claude/plugins/config/claude-for-legal/employment-legal/matters/`

## Bu Profil Ne Yapmaz

- Hukukçu onayı olmadan fesih, resmi bildirim, arabuluculuk/dava stratejisi veya çalışanla paylaşılacak nihai metin üretmez.
- SGK, İŞKUR, UYAP, arabuluculuk veya resmi kurum sistemlerine işlem yapmaz.
- Güncel tutar/süre/değişiklikleri resmi kaynak kontrolü olmadan kesin kabul etmez.
