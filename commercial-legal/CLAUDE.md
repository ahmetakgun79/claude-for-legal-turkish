<!--
CONFIGURATION LOCATION

User-specific configuration for this plugin lives at:

  ~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md

Rules:
1. Skills read configuration from that path, not from this template.
2. If the user config is missing or still contains [PLACEHOLDER], stop before substantive work and ask the user to run /commercial-legal:cold-start-interview.
3. The cold-start interview writes the populated profile to the config path.
4. This file is the shipped template and may be replaced by plugin updates.

This Legal Turkish template keeps command names compatible with the original
plugin but adapts the profile structure to Turkish commercial law and practice.
-->

# Commercial Contracts Practice Profile - Turkish Law Template

Bu dosya ticari sözleşme pratiği profilinin şablonudur. İlk kurulumda `/commercial-legal:cold-start-interview` bu yapıyı kullanarak kullanıcıya ait profili yazar.

Her çıktı avukat incelemesine tabi taslaktır. İmza, gönderim, noter/KEP bildirimi, UYAP işlemi veya karşı tarafa metin iletimi açık insan onayı olmadan yapılmaz.

---

## Who We Are

**Company / client:** [PLACEHOLDER]
**Entity type:** [PLACEHOLDER - A.Ş. | Ltd. Şti. | şahıs | yabancı şirket | diğer]
**Industry:** [PLACEHOLDER]
**Practice setting:** [PLACEHOLDER - in-house | law firm | solo lawyer | legal ops]
**Primary contract flow:** [PLACEHOLDER - purchasing-side | sales-side | both]
**Monthly volume:** [PLACEHOLDER]
**Final escalation point:** [PLACEHOLDER]

**The thing that hurts:** [PLACEHOLDER - kullanıcının kendi cümleleriyle]

---

## Who's Using This

**Role:** [PLACEHOLDER - lawyer/legal professional | non-lawyer with attorney access | non-lawyer without regular attorney access]
**Attorney contact:** [PLACEHOLDER]
**Output header:**

```text
[AVUKAT ÇALIŞMA ÜRÜNÜ - TASLAK / GİZLİ HUKUKİ DEĞERLENDİRME]
```

If the user is a non-lawyer, all signature, filing, notice, and counterparty-facing steps require attorney review gate.

---

## Turkish Law Defaults

**Default governing law:** Türk Hukuku
**Preferred courts:** [PLACEHOLDER - e.g. İstanbul Merkez (Çağlayan) Mahkemeleri ve İcra Daireleri]
**Arbitration posture:** [PLACEHOLDER - ISTAC | MTO | ad hoc | no arbitration without approval]
**Mediation policy:** Check 6325 sayılı Hukuk Uyuşmazlıklarında Arabuluculuk Kanunu and special dava şartı rules where disputes may become commercial, employment, consumer, lease, or other mandatory mediation matters.
**Notice methods:** [PLACEHOLDER - KEP | noter | iadeli taahhütlü posta | contract-defined email/portal]
**UYAP policy:** Use UYAP only when there is a real litigation/enforcement/court file. Do not create UYAP numbers for ordinary contracts.

---

## Turkish Contract Concepts

Use these concepts across all commercial reviews, redlines, escalation notes, and playbook updates:

| US / English term | Turkish-law working term | Review rule |
|---|---|---|
| Residuals / memory clause | Hafızada kalan bilgi istisnası | Treat as non-standard in NDAs. Test against confidentiality duties, TBK m.394-400 service/loyalty-confidentiality context when employees are involved, TTK m.54-55 unfair competition and trade secret protection, KVKK, and competition-sensitive information rules. Do not call it harmless boilerplate. |
| Survival | Bakiye hükümler / sözleşmenin sona ermesinden sonra devam edecek yükümlülükler | Identify which duties continue after expiry/termination: confidentiality, KVKK, payment, IP/FSEK, audit, liability cap, indemnity/tazminat, non-solicit/non-compete, dispute resolution. |
| Damga vergisi terimi | Damga vergisi (488 sayılı Damga Vergisi Kanunu / DVK) | Flag for tax/accounting review when a signed paper, amendment, guarantee, surety, settlement, assignment, or high-value contract may trigger DVK analysis. Do not calculate final tax. |
| Liquidated damages / penalty | Cezai şart (TBK m.179-185) | Check proportionality, one-sidedness, cumulative remedies, cap interaction, and whether a fahiş cezai şart reduction risk should be escalated. |
| Invalidity / interpretation pressure | Geçerlilik ve yorum kontrolü | For harsh, impossible, morality/public-order, or exploitation concerns, flag TBK m.19, m.27 and m.28 style issues for attorney review rather than treating the text as purely commercial. |
| Mediation before suit | Arabuluculuk / dava şartı kontrolü | Before litigation handoff, check 6325 and applicable special statutes for mandatory mediation; do not assume direct lawsuit filing is available. |

---

## Available Integrations

| Integration | Status | Fallback if unavailable |
|---|---|---|
| CLM / contract repository | [PLACEHOLDER ✓/✗] | Manual upload and local register |
| E-signature | [PLACEHOLDER ✓/✗] | User routes signature outside plugin |
| KEP / e-notice records | [PLACEHOLDER ✓/✗] | User provides records manually |
| Document storage | [PLACEHOLDER ✓/✗] | User uploads documents directly |
| Messaging | [PLACEHOLDER ✓/✗] | Inline output, no automatic send |
| UYAP / court file access | [PLACEHOLDER ✓/✗/N/A] | User provides file details manually |

Re-check: `/commercial-legal:cold-start-interview --check-integrations`

---

## Matter Workspaces

**Enabled:** [PLACEHOLDER ✓/✗]
**Active matter:** [none - practice-level context only]
**Cross-matter context:** [off]
**Matters path:** `~/.claude/plugins/config/claude-for-legal/commercial-legal/matters/`

When cross-matter context is off, skills never read another matter folder. Archived matters are not deleted; they remain available for retention and conflicts awareness.

---

## Playbook

**Active side:** [PLACEHOLDER - sales | purchasing | both]

Sales-side means the company sells products/services. Purchasing-side means the company buys from suppliers/vendors. Skills must determine the side before applying playbook positions.

### Sales-Side Playbook

Applies when the company is vendor/supplier.

#### Limitation of Liability

**Standard position:** [PLACEHOLDER]
**Acceptable fallbacks:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]
**Escalate:** [PLACEHOLDER]

#### Indemnity / Tazminat

**Standard position:** [PLACEHOLDER]
**Acceptable fallbacks:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]

#### Cezai Şart

**Standard position:** [PLACEHOLDER]
**Escalate if:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]

#### KVKK / Data Protection

**Role posture:** [PLACEHOLDER - controller | processor | varies]
**DPA posture:** [PLACEHOLDER]
**Cross-border transfer posture:** [PLACEHOLDER]
**Subprocessor posture:** [PLACEHOLDER]

#### IP / FSEK

**Standard position:** [PLACEHOLDER]
**Assignment limits:** [PLACEHOLDER]
**License posture:** [PLACEHOLDER]

#### Term, Termination, Renewal

**Standard term:** [PLACEHOLDER]
**Auto-renewal posture:** [PLACEHOLDER]
**Notice method:** [PLACEHOLDER]
**Renewal tracker handoff:** [PLACEHOLDER yes/no]

#### Governing Law, Venue, Arbitration

**Preferred:** [PLACEHOLDER]
**Acceptable:** [PLACEHOLDER]
**Escalate:** [PLACEHOLDER]
**Never:** [PLACEHOLDER]

#### The One Thing

[PLACEHOLDER - satış tarafında ilk kontrol edilecek deal-breaker]

### Purchasing-Side Playbook

Applies when the company is customer/buyer.

#### Limitation of Liability

**Standard position:** [PLACEHOLDER]
**Acceptable fallbacks:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]
**Escalate:** [PLACEHOLDER]

#### Indemnity / Tazminat

**Standard position:** [PLACEHOLDER]
**Acceptable fallbacks:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]

#### Cezai Şart

**Standard position:** [PLACEHOLDER]
**Escalate if:** [PLACEHOLDER]
**Never accept:** [PLACEHOLDER]

#### KVKK / Data Protection

**Role posture:** [PLACEHOLDER]
**DPA posture:** [PLACEHOLDER]
**Cross-border transfer posture:** [PLACEHOLDER]
**Subprocessor posture:** [PLACEHOLDER]

#### IP / FSEK

**Standard position:** [PLACEHOLDER]
**Assignment/license posture:** [PLACEHOLDER]

#### Term, Termination, Renewal

**Standard position:** [PLACEHOLDER]
**Auto-renewal posture:** [PLACEHOLDER]
**Notice method:** [PLACEHOLDER]
**Renewal tracker handoff:** [PLACEHOLDER yes/no]

#### Governing Law, Venue, Arbitration

**Preferred:** [PLACEHOLDER]
**Acceptable:** [PLACEHOLDER]
**Escalate:** [PLACEHOLDER]
**Never:** [PLACEHOLDER]

#### The One Thing

[PLACEHOLDER - satın alma tarafında ilk kontrol edilecek deal-breaker]

---

## NDA Triage Positions

**Attorney-reviewed:** [PLACEHOLDER yes/no]

| Check | GREEN | YELLOW | RED |
|---|---|---|---|
| Mutuality | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Confidential information definition | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Süre / bakiye hükümler (survival) | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Carveouts | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Residuals / hafızada kalan bilgi | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Cezai şart | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| KVKK/data transfer | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Governing law/venue | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |
| Competition-sensitive information | [PLACEHOLDER] | [PLACEHOLDER] | [PLACEHOLDER] |

**Closing action:** [PLACEHOLDER - e.g. CLM/e-signature approval flow]

---

## Escalation and Approval Matrix

| Can approve | Threshold / issue | Escalates to | Via |
|---|---|---|---|
| [PLACEHOLDER] | [PLACEHOLDER TL / standard terms] | [PLACEHOLDER] | [PLACEHOLDER] |

### Automatic Escalation Triggers

- sınırsız sorumluluk,
- fahiş veya tek taraflı cezai şart (TBK m.179-185),
- FSEK/IP assignment,
- KVKK yurt dışına aktarım risk,
- foreign law/forum outside playbook,
- unclear arbitration,
- guarantee/surety/letter of guarantee,
- signature authority gap,
- uncapped price increase or FX exposure,
- competition-sensitive information exchange.

---

## Review Preferences

**confirm_routing:** true
**redline style:** surgical edits first
**explanation depth:** [PLACEHOLDER - concise | standard | detailed]
**stakeholder summary default:** [PLACEHOLDER yes/no]
**language:** Turkish by default; English summary if requested.

---

## Renewal Tracking

**Register path:** `~/.claude/plugins/config/claude-for-legal/commercial-legal/renewal-register.yaml`
**Alert horizon:** 90 days
**Urgency bands:** 0-13 / 14-44 / 45-89 days based on `send_by_effective`
**Default notice methods:** KEP / noter / iadeli taahhütlü / contract-defined method
**Alert destination:** [PLACEHOLDER]

---

## Playbook Monitor Settings

```yaml
pattern_threshold: 5
lookback_months: 12
exclude_one_off_exceptions: true
```

---

## Outputs

### Work Product Header

```text
[AVUKAT ÇALIŞMA ÜRÜNÜ - TASLAK / GİZLİ HUKUKİ DEĞERLENDİRME]
```

### Next-Steps Decision Tree

End substantive outputs with tailored options:

1. Revize metin hazırla.
2. Hukukçu / onay makamına eskale et.
3. Eksik bilgi iste.
4. Yenileme / süre takibine ekle.
5. Diğer.

### Destination Rule

Before sending outside legal/confidential circle, produce a sanitized business version.

---

## What This Profile Does Not Do

- It does not give legal advice by itself.
- It does not authorize signature, filing, notice, or counterparty delivery.
- It does not replace conflicts checks.
- It does not make UYAP, KEP, notary, or e-signature submissions.
- It does not calculate final legal deadlines without verified trigger dates and applicable law.
