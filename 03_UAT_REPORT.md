# LAPORAN USER ACCEPTANCE TEST (UAT)

**PROYEK:** [Nama Proyek]
**MODUL:** [Nama Modul]
**SUBMODUL:** [Kode SubModul - Nama SubModul]

---

## INFORMASI DOKUMEN

| Field | Value |
|-------|-------|
| Nomor Dokumen | UAT/[KodeProyek]/[Modul]/[Tahun] |
| Versi | 1.0 |
| Periode UAT | [DD-MM-YYYY] s/d [DD-MM-YYYY] |
| Tanggal Report | [DD-MM-YYYY] |
| Status | [ ] APPROVED [ ] CONDITIONAL [ ] REJECTED |
| Klasifikasi | Internal |

## HISTORY PERUBAHAN

| Versi | Tanggal | Perubahan | Oleh |
|-------|---------|-----------|------|
| 1.0 | [DD-MM-YYYY] | Laporan awal | Tim QA |

## DIBUAT OLEH

| Role | Nama | Tanggal | Tanda Tangan |
|------|------|---------|--------------|
| QA Lead | [Nama] | | |

## PERSETUJUAN UAT

| Role | Nama | Tanggal | Tanda Tangan | Keputusan |
|------|------|---------|--------------|-----------|
| Business Owner | [Nama] | | | [ ] Approved [ ] Rejected |
| Product Manager | [Nama] | | | [ ] Approved [ ] Rejected |
| Stakeholder | [Nama] | | | [ ] Approved [ ] Rejected |

---

## DAFTAR ISI

1. Pendahuluan
2. Scope UAT
3. Detail Pelaksanaan
4. Risiko UAT
5. Entry & Exit Criteria
6. Hasil Testing
7. Ringkasan Bug
8. Feedback & Issues
9. Kesimpulan & Keputusan
10. Lampiran

---

## 1. PENDAHULUAN

### 1.1 Tujuan Dokumen

Dokumen ini berfungsi untuk mencatat hasil **User Acceptance Testing (UAT)** dan memastikan bahwa fitur memenuhi kebutuhan bisnis yang didefinisikan dalam PRD sebelum rilis ke Production.

Dokumen ini menjelaskan UAT untuk **[Nama SubModul]** yang merupakan bagian dari **[Nama Modul]** dalam proyek **[Nama Proyek]**.

### 1.2 Tujuan UAT

User Acceptance Testing bertujuan untuk:

**1. Memastikan kesesuaian fitur dengan PRD**
- Validasi semua requirement bisnis terpenuhi
- Verifikasi acceptance criteria sesuai dokumentasi

**2. Memvalidasi business flow dari perspektif end-user**
- Testing real-world scenarios
- Validasi usability & user experience
- Konfirmasi workflow sesuai kebutuhan bisnis

**3. Menentukan apakah fitur layak rilis**
- Final approval dari business stakeholder
- Go/No-go decision untuk production release

### 1.3 Partisipan UAT

| Role | Nama | Tanggung Jawab |
|------|------|----------------|
| Business Owner | [Nama] | Final approval, business requirement validation |
| Product Manager | [Nama] | Feature acceptance, PRD alignment check |
| End User Representative | [Nama] | Real-world scenario testing |
| QA Lead | [Nama] | Koordinasi UAT, facilitation |
| QA Engineer | [Nama] | Dukungan eksekusi test, bug tracking |

---

## 2. SCOPE UAT

### 2.1 Yang Termasuk (In Scope)

**Fitur/Fungsi yang Ditest:**

| No | Feature | Sub-Feature | User Role | Prioritas |
|----|---------|-------------|-----------|-----------|
| 1 | [Feature 1] | [Sub-feature 1.1], [Sub-feature 1.2] | Admin/User | Critical |
| 2 | [Feature 2] | [Sub-feature 2.1], [Sub-feature 2.2] | User | High |
| 3 | [Feature 3] | [Sub-feature 3.1] | Admin | Medium |

**Business Flow yang Divalidasi:**

**1. [Business Flow 1]**
- Step 1: [Deskripsi]
- Step 2: [Deskripsi]
- Expected Outcome: [Outcome]

**2. [Business Flow 2]**
- Step 1: [Deskripsi]
- Step 2: [Deskripsi]
- Expected Outcome: [Outcome]

**User Roles yang Ditest:**

- [ ] Super Admin - Full access, system configuration
- [ ] Admin - User management, content moderation
- [ ] User - Standard user operations
- [ ] Guest - Limited access (jika applicable)

### 2.2 Yang Tidak Termasuk (Out of Scope)

**Yang TIDAK Termasuk UAT:**

- Performance Testing - Sudah covered di Performance Test Report
- Security Testing - Sudah covered di VAPT Report
- Integration Testing - Sudah covered di SIT Report
- Cross-browser Compatibility - Sudah covered di E2E Testing
- Load Testing - Sudah covered di Performance Test
- Backend API Testing - Sudah covered di API Testing

**Alasan:**
UAT fokus pada **business acceptance** dari perspektif end-user, bukan technical validation.

---

## 3. DETAIL PELAKSANAAN

### 3.1 Periode Pelaksanaan

| Item | Detail |
|------|--------|
| Tanggal Mulai | [DD-MM-YYYY] |
| Tanggal Selesai | [DD-MM-YYYY] |
| Total Hari | [N] hari kerja |
| Jumlah Sesi UAT | [N] sessions |

### 3.2 Environment

| Item | Detail |
|------|--------|
| Environment | Staging / Pre-Production |
| URL | [URL] |
| Database | [Nama database] (production-like data) |
| VPN Required | [ ] Ya [ ] Tidak |

### 3.3 Device & Browser

**Hardware:**

| Jenis Device | Model | Versi OS | Screen Resolution |
|--------------|-------|----------|-------------------|
| Desktop | [Model] | Windows 10/11 / macOS | 1920x1080 |
| Mobile Android | [Model] | Android 11+ | [Resolution] |
| Mobile iOS | [Model] | iOS 14+ | [Resolution] |

**Software:**

| Software | Versi | Tujuan |
|----------|-------|--------|
| Browser | Chrome 120+, Firefox 115+, Safari 16+ | Web testing |
| Mobile App | Version [X.Y.Z] | Mobile testing |

### 3.4 Test Accounts

| Role | Username | Password | Tujuan |
|------|----------|----------|--------|
| Super Admin | [Username] | [Password] | Full access testing |
| Admin | [Username] | [Password] | Admin role testing |
| User 1 | [Username] | [Password] | Standard user testing |
| User 2 | [Username] | [Password] | Standard user testing |

**Note:** Jangan gunakan akun production untuk UAT!

---

## 4. RISIKO UAT

### 4.1 Risk Assessment

| No | Deskripsi Risiko | Probabilitas | Dampak | Mitigasi |
|----|------------------|--------------|--------|----------|
| 1 | Kegagalan UAT - Ditemukan defect kritis yang menghambat proses bisnis utama | Low | High | Feature-complete sebelum UAT; Internal QA regression sebelum handover; Daily bug triage selama UAT |
| 2 | Environment tidak stabil - Staging downtime atau data issues | Low | High | Environment readiness checklist; Dedicated DevOps support; Backup environment tersedia |
| 3 | Perubahan requirement saat UAT | Low | High | Freeze scope saat UAT dimulai; Change Request process untuk perubahan; Impact assessment untuk setiap CR |
| 4 | UAT participant tidak available | Medium | Medium | Flexible schedule; Record UAT sessions untuk review; Backup UAT participants |
| 5 | Misalignment antara PRD vs Implementation | Low | High | PRD walkthrough sebelum UAT; QA validate vs PRD sebelum handover; Early stakeholder demo |

---

## 5. ENTRY & EXIT CRITERIA

### 5.1 Entry Criteria

UAT dapat dimulai jika:

- [ ] **Development telah selesai**
  - All features implemented sesuai PRD
  - Code freeze untuk UAT scope

- [ ] **SIT/Internal QA telah selesai dan PASS**
  - SIT Report status = PASS
  - Pass rate >= 95%

- [ ] **Tidak ada Critical blocker open**
  - Open Blocker = 0
  - Prod Bugs = 0

- [ ] **Test scenarios telah direview dan disetujui**
  - UAT test scenarios based on PRD
  - Approved by Product Manager & Business Owner

- [ ] **Environment siap**
  - Staging environment stable
  - Test data prepared (production-like)
  - Access credentials ready

- [ ] **UAT participants ready**
  - Schedule confirmed
  - Training/walkthrough done (if needed)

### 5.2 Exit Criteria

UAT dianggap complete dan APPROVED jika:

**Mandatory:**

- [ ] **Semua UAT scenarios telah dieksekusi**
  - Execution rate = 100%
  - All critical & high priority scenarios tested

- [ ] **Pass rate >= 95%**
  - Success rate memenuhi target
  - All critical scenarios PASS

- [ ] **Tidak ada Critical blocker open**
  - Zero critical bugs open
  - Zero high severity bugs blocking core business flow

- [ ] **Semua Medium/High bugs memiliki workaround atau fix plan**
  - Documented workarounds untuk known issues
  - Clear timeline untuk fixes (if post-release)

- [ ] **Business stakeholder approval obtained**
  - Sign-off dari Business Owner
  - Sign-off dari Product Manager
  - Formal approval documented

**Conditional:**

- [ ] **Low priority bugs**
  - Dapat defer ke next release
  - Max [N] low bugs open dengan approval

---

## 6. HASIL TESTING

### 6.1 Ringkasan Keseluruhan

| Metric | Count | Persentase |
|--------|-------|------------|
| Total Scenarios | [N] | 100% |
| Dieksekusi | [N] | [N%] |
| Passed | [N] | [N%] |
| Failed | [N] | [N%] |
| Blocked | [N] | [N%] |
| Tidak Dieksekusi | [N] | [N%] |
| **PASS RATE** | **[N]** | **[N%]** |

### 6.2 Hasil per Feature

| Feature | Total | Passed | Failed | Blocked | Pass Rate | Status |
|---------|-------|--------|--------|---------|-----------|--------|
| [Feature 1] | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| [Feature 2] | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| [Feature 3] | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| **TOTAL** | **[N]** | **[N]** | **[N]** | **[N]** | **[N%]** | **PASS/FAIL** |

### 6.3 Hasil per Prioritas

| Prioritas | Total | Passed | Failed | Blocked | Pass Rate | Status |
|-----------|-------|--------|--------|---------|-----------|--------|
| Critical | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| High | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| Medium | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| Low | [N] | [N] | [N] | [N] | [N%] | PASS/FAIL |
| **TOTAL** | **[N]** | **[N]** | **[N]** | **[N]** | **[N%]** | **PASS/FAIL** |

### 6.4 Detail Hasil Testing

#### Scenario #1: [Nama Scenario]

| Field | Value |
|-------|-------|
| Scenario ID | UAT-001 |
| Feature | [Nama feature] |
| Prioritas | Critical/High/Medium/Low |
| Tested By | [Nama UAT participant] |
| Tanggal Test | [DD-MM-YYYY] |
| Durasi | [N] menit |
| Status | PASS / FAIL / BLOCKED |

**Business Flow:**
```
Given [precondition]
When [user action]
Then [expected outcome]
```

**Langkah Test:**
1. [Langkah 1]
2. [Langkah 2]
3. [Langkah 3]

**Expected Result:**
[Deskripsi expected result]

**Actual Result:**
[Deskripsi actual result]

**Evidence:**
- Screenshot: [URL]
- Video: [URL]

**Notes/Comments:**
[Catatan dari UAT participant]

---

#### Scenario #2: [Nama Scenario]

[Struktur sama dengan Scenario #1]

---

### 6.5 Log Sesi UAT

| Sesi | Tanggal | Waktu | Participant | Scenarios Tested | Hasil |
|------|---------|-------|-------------|------------------|-------|
| 1 | [DD-MM-YYYY] | [HH:MM-HH:MM] | [Nama] | [N] scenarios | [N] pass, [N] fail |
| 2 | [DD-MM-YYYY] | [HH:MM-HH:MM] | [Nama] | [N] scenarios | [N] pass, [N] fail |
| 3 | [DD-MM-YYYY] | [HH:MM-HH:MM] | [Nama] | [N] scenarios | [N] pass, [N] fail |

---

## 7. RINGKASAN BUG

### 7.1 Statistik Bug

| Metric | Count | Persentase |
|--------|-------|------------|
| Total Bugs | [N] | 100% |
| Resolved | [N] | [N%] |
| Open | [N] | [N%] |

**Per Severity:**

| Severity | Ditemukan | Resolved | Open |
|----------|-----------|----------|------|
| Critical | [N] | [N] | [N] |
| High | [N] | [N] | [N] |
| Medium | [N] | [N] | [N] |
| Low | [N] | [N] | [N] |
| **TOTAL** | **[N]** | **[N]** | **[N]** |

### 7.2 Bug Critical & High

#### Bug #1: [Judul Bug]

| Field | Value |
|-------|-------|
| Bug ID | [JIRA-XXX] |
| Severity | Critical/High |
| Priority | P0/P1 |
| Status | Open/In Progress/Fixed/Verified |
| Feature | [Nama feature] |
| Reported By | [Nama UAT participant] |
| Tanggal Report | [DD-MM-YYYY] |

**Deskripsi:**
[Deskripsi detail dari bug]

**Business Impact:**
[Impact pada business process]

**Langkah Reproduksi:**
1. [Langkah 1]
2. [Langkah 2]
3. [Langkah 3]

**Expected Behavior:**
[Apa yang seharusnya terjadi]

**Actual Behavior:**
[Apa yang sebenarnya terjadi]

**Workaround:**
[Workaround jika ada, atau "None"]

**Resolusi:**
- [ ] Fixed - [Deskripsi fix]
- [ ] Will fix post-release - [Timeline]
- [ ] Won't fix - [Justifikasi dengan approval]

**Evidence:**
- Jira Link: [URL]
- Screenshot: [URL]

---

#### Bug #2: [Judul Bug]

[Struktur sama dengan Bug #1]

---

### 7.3 Keputusan Penerimaan Bug

| Bug ID | Severity | Status | Keputusan | Justifikasi |
|--------|----------|--------|-----------|-------------|
| [JIRA-XXX] | Critical | Resolved | Accepted | Fixed and retested |
| [JIRA-XXX] | High | Open | Conditional | Workaround available, fix post-release |
| [JIRA-XXX] | Medium | Open | Accepted | Non-blocking, defer to next release |
| [JIRA-XXX] | Low | Open | Accepted | Minor UI issue, defer to backlog |

---

## 8. FEEDBACK & ISSUES

### 8.1 Feedback Stakeholder

**Feedback dari Business Owner:**

| No | Kategori | Feedback | Prioritas | Action Plan |
|----|----------|----------|-----------|-------------|
| 1 | [Usability] | [Detail feedback] | High/Medium/Low | [Action plan] |
| 2 | [Performance] | [Detail feedback] | High/Medium/Low | [Action plan] |
| 3 | [Feature Request] | [Detail feedback] | High/Medium/Low | [Action plan] |

**Feedback dari Product Manager:**

| No | Kategori | Feedback | Prioritas | Action Plan |
|----|----------|----------|-----------|-------------|
| 1 | [Kategori] | [Detail feedback] | High/Medium/Low | [Action plan] |

**Feedback dari End User:**

| No | Kategori | Feedback | Prioritas | Action Plan |
|----|----------|----------|-----------|-------------|
| 1 | [Kategori] | [Detail feedback] | High/Medium/Low | [Action plan] |

### 8.2 Usability Issues

| No | Issue | Impact | Rekomendasi |
|----|-------|--------|-------------|
| 1 | [Deskripsi issue] | High/Medium/Low | [Rekomendasi] |
| 2 | [Deskripsi issue] | High/Medium/Low | [Rekomendasi] |

### 8.3 Feature Enhancement Requests

| No | Request | Prioritas | Feasibility | Target Release |
|----|---------|-----------|-------------|----------------|
| 1 | [Detail request] | High/Medium/Low | [Analisis] | [Version X.Y] |
| 2 | [Detail request] | High/Medium/Low | [Analisis] | [Version X.Y] |

---

## 9. KESIMPULAN & KEPUTUSAN

### 9.1 Keputusan Akhir

**[ ] APPROVED** - Feature disetujui untuk rilis ke Production

**Justifikasi:**
- Pass rate: [N%] (>= 95%)
- Zero critical/high blocker open
- All business flows validated successfully
- Stakeholder approval obtained

**Persetujuan:**
- Business Owner: [ ] Approved - [Nama] - [Date]
- Product Manager: [ ] Approved - [Nama] - [Date]
- QA Lead: [ ] Approved - [Nama] - [Date]

**Rencana Production Release:**
- Go Live Date: [DD-MM-YYYY]
- Deployment Window: [HH:MM - HH:MM]
- Rollback Plan: [Ready/Documented]

---

**[ ] CONDITIONAL** - Disetujui dengan catatan

**Kondisi untuk Proceed:**

1. **[Kondisi 1]**
   - PIC: [Nama]
   - Target: [Date]
   - Must be resolved before release

2. **[Kondisi 2]**
   - PIC: [Nama]
   - Target: [Date]
   - Can be resolved post-release dengan monitoring

**Persetujuan dengan Catatan:**
- Business Owner: [ ] Conditional Approval - [Nama] - [Date]
  - Kondisi: [Specify condition]
- Product Manager: [ ] Conditional Approval - [Nama] - [Date]
  - Kondisi: [Specify condition]

**Monitoring Plan:**
[Monitoring plan untuk post-release jika ada conditional approval]

---

**[ ] REJECTED** - Tidak disetujui untuk rilis

**Alasan Rejection:**
- Pass rate: [N%] (< 95%)
- Critical bugs: [N] open
- Business flow [X] tidak berfungsi sesuai ekspektasi

**Required Actions Sebelum Re-UAT:**

| No | Action | PIC | Target Date | Prioritas |
|----|--------|-----|-------------|-----------|
| 1 | [Deskripsi action] | [Nama] | [DD-MM-YYYY] | Critical/High |
| 2 | [Deskripsi action] | [Nama] | [DD-MM-YYYY] | Critical/High |

**Rencana Re-UAT:**
- Re-UAT Date: [DD-MM-YYYY]
- Scope: [Full re-test atau partial]
- Participants: [Same atau different]

---

### 9.2 Rekomendasi Pasca UAT

#### A. Immediate Actions (Sebelum Go Live)

| No | Action | PIC | Target Date | Prioritas |
|----|--------|-----|-------------|-----------|
| 1 | [Deskripsi action] | [Nama] | [DD-MM-YYYY] | Critical |
| 2 | [Deskripsi action] | [Nama] | [DD-MM-YYYY] | High |

#### B. Post-Release Monitoring

**Minggu 1 Setelah Release:**
- [ ] Monitor production logs untuk errors
- [ ] Track user adoption & feedback
- [ ] Monitor performance metrics
- [ ] Daily stand-up untuk issue resolution

**Minggu 2-4 Setelah Release:**
- [ ] Weekly review of production bugs
- [ ] User feedback analysis
- [ ] Performance optimization (jika needed)

#### C. Improvements untuk Masa Depan

**1. Automation (Opsional - Jika Diperlukan)**
- Automate regression scenarios dari UAT
- Target: [N%] automation coverage - sesuai kebutuhan project

**2. Dokumentasi**
- User guide/manual based on UAT feedback
- FAQ based on UAT questions

**3. Training**
- End-user training based on UAT learnings
- Admin training untuk new features

---

## 10. LAMPIRAN

### 10.1 Referensi Test Scenarios

**QATM Spreadsheet:** [Google Sheets URL]
**Spreadsheet ID:** [44-character ID]
**UAT Test Scenarios:** [Link to UAT scenarios document]

### 10.2 Bug Reports

**Jira Board:** [Link to Jira]
**Bug Filter:** [Link to filtered view showing UAT bugs]

### 10.3 Test Evidence

**Screenshots Folder:** [Google Drive URL]
**UAT Session Recordings:** [URL jika ada]

### 10.4 Approval Document

**Formal Approval Email:** [Link or attach email]
**Sign-off Form:** [Attach scanned form if physical]

### 10.5 Referensi PRD

**Product Requirements Document (PRD):** [Link to PRD]

**Acceptance Criteria Checklist:**
- [ ] All PRD requirements covered in UAT
- [ ] All acceptance criteria validated
- [ ] Traceability matrix complete

### 10.6 Informasi Kontak

| Role | Nama | Email | Phone |
|------|------|-------|-------|
| Business Owner | [Nama] | [Email] | [Phone] |
| Product Manager | [Nama] | [Email] | [Phone] |
| QA Lead | [Nama] | [Email] | [Phone] |
| Project Manager | [Nama] | [Email] | [Phone] |

---

**END OF REPORT**

_Versi: 1.0_
_Template: UAT Report v2.0 - Clean & Professional_
_© QA INA Digital_
