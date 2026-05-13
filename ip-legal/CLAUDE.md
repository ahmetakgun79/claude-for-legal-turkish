<!--
YAPILANDIRMA LOKASYONU

Bu plugin için kullanıcıya özel yapılandırma aşağıdaki yolda tutulur:
  ~/.claude/plugins/config/claude-for-legal/ip-legal/CLAUDE.md

Kurallar:
1. Bu dosya (ayarlar) baz alınarak çalışılır.
2. [PLACEHOLDER] kısımları duruyorsa, /ip-legal:cold-start-interview komutu ile başlatın.
-->

# Fikri Mülkiyet (IP) Pratik Profili
*Bu dosya ilk çalıştırmada (cold-start interview) oluşturulur. İlgili kısımlar dolana kadar bir şablondur.*

---

## Şirket / Hukuk Bürosu Profili

**Kurum Adı:** [PLACEHOLDER — Şirket veya büronun tam yasal adı] 
**Sektör:** [PLACEHOLDER — Örn. teknoloji, medya, ilaç vb.]
**Aşama:** [PLACEHOLDER — Startup / büyüme / halka açık / hukuk bürosu]
**Yetki Alanı:** [PLACEHOLDER — Türkiye, WIPO vb.]

---

## Kullanıcı Profili

**Rol:** [PLACEHOLDER — Avukat / Marka ve Patent Vekili / Profesyonel]
**Sorumlu Avukat / Yönetici:** [PLACEHOLDER — İsim / Departman]

---

## Çıktı Başlıkları ve Gizlilik

**Work-product (İş Ürünü) Başlığı:** (Plugin'in ürettiği her analiz, bilgi notu veya değerleme raporunun başına eklenir). Gizlilik ve Sır Saklama Yükümlülüğü statüsüne göre değişkenlik gösterir:

- Eğer Rol Avukat veya Hukuk Profesyoneli ise: GİZLİDİR — AVUKAT-MÜVEKKİL İLİŞKİSİ KAPSAMINDA HAZIRLANMIŞTIR — AVUKATLIK KANUNU MADDE 36 KAPSAMINDA SIR SAKLAMA YÜKÜMLÜLÜĞÜNE TABİDİR
- Eğer Rol Marka/Patent Vekili ise: GİZLİDİR — MARKA/PATENT VEKİLİ İLİŞKİSİ (TÜRKPATENT İŞLEMLERİ) — HARİCİ PAYLAŞIMLARA KAPALIDIR
- Diğer roller için: ARAŞTIRMA NOTLARI — HUKUKİ TAVSİYE (MÜTOLAA) DEĞİLDİR — İŞLEM YAPMADAN ÖNCE BİR AVUKATA (VEYA VEKİLE) DANIŞIN

**Gizlilik Uyarısı:** Türk Hukuku'nda ABD'deki Attorney Work Product doktrininin birebir karşılığı bulunmamaktır. Ancak Avukatlık Kanunu m.36 gereğince avukatların sır saklama yükümlülüğü esastır ve savunma hakkı kapsamındaki dokümanlar gizlidir. Bu çıktıların 3. taraflarla (veya UYAP'ta herkese açık olarak) denetimsiz paylaşımı feragat anlamına gelebilir. Taraf karşıya veya Noter'e gidecek ihtarname/bildirimlerde bu başlığı kaldırınız.

---

**İnceleyici Notu (Reviewer note)** 
Bu bilgi teslim edilen çalışmanın bir blok üzerinde bulunur. Eksikler veya dikkate alınması gereken hususlar (Örneğin: Kararlar manuel kontrol edilmeli, ihlal durumu şüpheli vb.) burada listelenir.
