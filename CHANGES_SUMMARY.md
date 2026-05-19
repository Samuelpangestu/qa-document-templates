# SUMMARY PERUBAHAN - INDONESIAN LANGUAGE UPDATE

## PERUBAHAN YANG AKAN DITERAPKAN

### 1. BAHASA INDONESIA SEBAGAI PRIMARY LANGUAGE

**Header Sections:**
- "DOCUMENT INFORMATION" → "INFORMASI DOKUMEN"
- "DOCUMENT HISTORY" → "HISTORY PERUBAHAN"
- "APPROVAL" → "PERSETUJUAN"
- "TABLE OF CONTENTS" → "DAFTAR ISI"
- "PREPARED BY" → "DIBUAT OLEH"
- "REVIEWED BY" → "DIREVIEW OLEH"

**Common Terms:**
- "Purpose" → "Tujuan"
- "Overview" → "Ringkasan"
- "Status" → "Status" (tetap sama)
- "Priority" → "Prioritas"
- "Feature" → "Feature" (technical term, tetap English)
- "Environment" → "Environment" (technical term, tetap English)
- "Testing" → "Testing" (technical term, tetap English)

**Field Names (Table Headers):**
- "Field" → "Field" (tetap)
- "Value" → "Value" (tetap)
- "Date" → "Tanggal"
- "Version" → "Versi"
- "Name" → "Nama"
- "Role" → "Role" (tetap)
- "Signature" → "Tanda Tangan"

### 2. AUTOMATION MARK AS OPTIONAL

**Test Plan (Section 2.3):**
```markdown
### 2.3 Automation (Opsional - Tergantung Kebutuhan)

**Web/Mobile Automation:**
- Tool: [Playwright/Selenium/Appium] - jika diperlukan
- Target: [N%] automation coverage - sesuai kebutuhan project
- Scope: Regression suite untuk critical path

**API Automation:**
- Tool: [Postman/REST Assured/K6] - jika diperlukan
- Target: [N%] automation coverage - sesuai kebutuhan project
- Scope: API regression testing

**Note:** Automation tidak wajib untuk semua project. Pertimbangkan:
- Kompleksitas project
- Budget dan timeline
- Frekuensi regression testing
- ROI automation
```

**QATM TC_Master Column:**
- "Automated" column tetap ada tapi dengan note: "Opsional - isi jika ada automation"

**Exit Criteria:**
- "Automation Rate >= 60%" → "Automation Rate >= 60% (jika applicable untuk regression suite)"

### 3. TECHNICAL TERMS TETAP ENGLISH

**Tetap English (tidak diterjemahkan):**
- Feature, Bug, Test, Testing
- API, Web, Mobile
- Smoke Test, Regression Test, Sanity Test
- Performance, SLA, P95, P99, RPS, VU
- Critical, High, Medium, Low (priority/severity)
- PASS, FAIL, BLOCKED
- Open, In Progress, Fixed, Verified, Closed
- Browser, OS, Database
- JIRA, Postman, K6, Playwright
- Sprint, Backlog, Release
- Mock, Stub, Driver

**Diterjemahkan ke Indonesia:**
- Summary → Ringkasan
- Objective → Tujuan
- Scope → Scope (tetap, tapi "In Scope" → "Yang Termasuk")
- Schedule → Jadwal
- Entry Criteria → Entry Criteria (tetap)
- Exit Criteria → Exit Criteria (tetap)
- Risk → Risiko
- Mitigation → Mitigasi
- Recommendation → Rekomendasi

---

## CONTOH PERUBAHAN PER TEMPLATE

### 02_SIT_REPORT.md

**Before:**
```markdown
## 1. EXECUTIVE SUMMARY

### 1.1 Overview

System Integration Testing (SIT) for **[Nama SubModul]** has been executed...

### 1.2 Key Results

| Metric | Target | Actual | Status |
```

**After:**
```markdown
## 1. RINGKASAN EKSEKUTIF

### 1.1 Ringkasan

System Integration Testing (SIT) untuk **[Nama SubModul]** telah dilaksanakan...

### 1.2 Hasil Utama

| Metric | Target | Actual | Status |
```

### 03_UAT_REPORT.md

**Before:**
```markdown
## 1. INTRODUCTION

### 1.1 Document Purpose

This document records the results of **User Acceptance Testing (UAT)**...

### 1.2 UAT Objectives

User Acceptance Testing aims to:
- Ensure feature meets PRD requirements
```

**After:**
```markdown
## 1. PENDAHULUAN

### 1.1 Tujuan Dokumen

Dokumen ini mencatat hasil **User Acceptance Testing (UAT)**...

### 1.2 Tujuan UAT

User Acceptance Testing bertujuan untuk:
- Memastikan fitur memenuhi requirement PRD
```

### 04_PERFORMANCE_TEST_REPORT.md

**Before:**
```markdown
## 1. EXECUTIVE SUMMARY

### 1.1 Overview

Performance Test for **[Nama SubModul]** was executed on **[DD-MM-YYYY]**...

### 1.3 Status Decision

**[ ] PASS** - System meets all SLA

**Criteria:**
- Response Time P95 < SLA
```

**After:**
```markdown
## 1. RINGKASAN EKSEKUTIF

### 1.1 Ringkasan

Performance Test untuk **[Nama SubModul]** telah dilaksanakan pada **[DD-MM-YYYY]**...

### 1.3 Keputusan Status

**[ ] PASS** - Sistem memenuhi semua SLA

**Kriteria:**
- Response Time P95 < SLA
```

### 05_TEST_EXECUTION_SUMMARY.md

**Before:**
```markdown
## PURPOSE

This document summarizes internal testing results (Functional, API, Integration) before UAT starts...

## EXECUTIVE SUMMARY

### Overall Status

**Testing Completion:** [N%]
```

**After:**
```markdown
## TUJUAN

Dokumen ini merangkum hasil testing internal (Functional, API, Integration) sebelum UAT dimulai...

## RINGKASAN EKSEKUTIF

### Status Keseluruhan

**Penyelesaian Testing:** [N%]
```

---

## KONSISTENSI TRANSLATION

### Section Headers (Level 2 ##)

| English | Indonesian |
|---------|-----------|
| EXECUTIVE SUMMARY | RINGKASAN EKSEKUTIF |
| INTRODUCTION | PENDAHULUAN |
| TEST STRATEGY | STRATEGI TESTING |
| TEST SCOPE | SCOPE TESTING |
| TEST ENVIRONMENT | TEST ENVIRONMENT |
| TEST SCHEDULE | JADWAL TESTING |
| ENTRY & EXIT CRITERIA | ENTRY & EXIT CRITERIA |
| DEFECT MANAGEMENT | MANAJEMEN DEFECT |
| RISK MANAGEMENT | MANAJEMEN RISIKO |
| CONCLUSION & RECOMMENDATIONS | KESIMPULAN & REKOMENDASI |
| APPENDIX | APPENDIX |

### Subsection Headers (Level 3 ###)

| English | Indonesian |
|---------|-----------|
| Purpose | Tujuan |
| Overview | Ringkasan |
| Key Results | Hasil Utama |
| Test Objectives | Tujuan Testing |
| In Scope | Yang Termasuk (In Scope) |
| Out of Scope | Yang Tidak Termasuk (Out of Scope) |
| Environment Details | Detail Environment |
| Key Metrics | Metric Utama |
| Bug Summary | Ringkasan Bug |
| Status Decision | Keputusan Status |
| Final Decision | Keputusan Akhir |
| Recommendations | Rekomendasi |
| Contact Information | Informasi Kontak |

### Decision Frameworks

**SIT Report:**
- "PASS" tetap PASS (tidak diterjemahkan)
- "CONDITIONAL" tetap CONDITIONAL
- "NOT PASS" tetap NOT PASS

**UAT Report:**
- "APPROVED" tetap APPROVED
- "CONDITIONAL" tetap CONDITIONAL
- "REJECTED" tetap REJECTED

**Performance Report:**
- "PASS" tetap PASS
- "WARNING" tetap WARNING
- "FAIL" tetap FAIL

**Test Execution Summary:**
- "READY" tetap READY
- "NOT READY" tetap NOT READY

### Checkbox Text

| English | Indonesian |
|---------|-----------|
| [ ] Draft [ ] Review [ ] Approved | [ ] Draft [ ] Review [ ] Approved (tetap) |
| [ ] Yes [ ] No | [ ] Ya [ ] Tidak |
| [ ] Ready | [ ] Siap |
| [ ] Enabled [ ] Disabled | [ ] Enabled [ ] Disabled (tetap) |

---

## VALIDATION CHECKLIST

Setelah update, verify:

- [ ] Semua section headers konsisten
- [ ] Technical terms tetap English
- [ ] Business terms dalam Bahasa Indonesia
- [ ] Decision framework tetap English (PASS/FAIL/etc)
- [ ] Table headers konsisten
- [ ] Automation marked as optional dengan note jelas
- [ ] QATM integration references tetap akurat
- [ ] Formula dan code blocks tidak berubah
- [ ] Placeholder format tetap `[...]`
- [ ] No emojis (tetap clean)

---

## FILES TO UPDATE

1. **02_SIT_REPORT.md** - ~300 lines
2. **03_UAT_REPORT.md** - ~350 lines
3. **04_PERFORMANCE_TEST_REPORT.md** - ~400 lines
4. **05_TEST_EXECUTION_SUMMARY.md** - ~250 lines
5. **README.md** - ~200 lines

**Total:** ~1500 lines perubahan

---

## ESTIMATED TIME

- Per template: 10-15 menit
- Total: 50-75 menit untuk 5 files

---

## APPROVAL NEEDED

Silakan review changes di atas. Jika sudah OK, saya akan proceed dengan update semua template.

**Konfirmasi:**
- [ ] Section headers translation OK
- [ ] Technical terms kept in English OK
- [ ] Automation marking as optional OK
- [ ] Decision frameworks kept in English OK
- [ ] Ready to proceed with update

---

_Status: Waiting for Approval_
_Created: 19 Mei 2026_
