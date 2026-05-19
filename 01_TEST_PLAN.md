# DOKUMEN TEST PLAN

**PROYEK:** [Nama Proyek]
**MODUL:** [Nama Modul]
**SUBMODUL:** [Kode SubModul - Nama SubModul]

---

## INFORMASI DOKUMEN

| Field | Value |
|-------|-------|
| Nomor Dokumen | TP/[KodeProyek]/[Modul]/[Tahun] |
| Versi | 1.0 |
| Tanggal | [DD-MM-YYYY] |
| Status | [ ] Draft [ ] Review [ ] Approved |
| Klasifikasi | Internal |

## HISTORY PERUBAHAN

| Versi | Tanggal | Perubahan | Oleh |
|-------|---------|-----------|------|
| 1.0 | [DD-MM-YYYY] | Dokumen awal | Tim QA |

## PERSETUJUAN

| Role | Nama | Tanggal | Tanda Tangan |
|------|------|---------|--------------|
| QA Lead | [Nama] | | |
| Project Manager | [Nama] | | |
| Technical Lead | [Nama] | | |

---

## DAFTAR ISI

1. Pendahuluan
2. Strategi Testing
3. Scope Testing
4. Test Environment
5. Jadwal Testing
6. Integrasi QATM
7. Entry & Exit Criteria
8. Manajemen Defect
9. Manajemen Risiko
10. Referensi

---

## 1. PENDAHULUAN

### 1.1 Tujuan

Dokumen ini menjelaskan rencana testing untuk [Nama SubModul] dalam project [Nama Proyek].

### 1.2 Struktur Project

```
Project: [Nama Proyek]
 └─ Modul: [Nama Modul]
     └─ SubModul: [Kode] - [Nama SubModul]
         ├─ Feature 1
         ├─ Feature 2
         └─ Feature 3
```

### 1.3 Deskripsi Scope

**SubModul:** [Deskripsi fungsi SubModul dalam 2-3 kalimat]

**Nilai Bisnis:** [Nilai bisnis yang dihasilkan]

**Fitur Utama:**
- [Feature 1] - [Deskripsi]
- [Feature 2] - [Deskripsi]
- [Feature 3] - [Deskripsi]

---

## 2. STRATEGI TESTING

### 2.1 Test Levels

**Unit Testing**
- Tanggung Jawab: Developer
- Target Coverage: 80% minimum
- Tools: [Jest/JUnit/PyTest]

**Integration Testing**
- Tanggung Jawab: QA + Developer
- Scope: Integrasi komponen dalam SubModul
- Tools: [Postman/REST Assured]

**System Testing**
- Tanggung Jawab: Tim QA
- Scope: End-to-end workflow testing
- Tools: [Playwright/Selenium/Appium]

**User Acceptance Testing**
- Tanggung Jawab: Stakeholder + QA
- Environment: Staging/Pre-Production
- Deliverable: UAT Report dengan sign-off

**Mapping Test Levels → Output Documents:**

| Test Level | Output Document | Template |
|------------|-----------------|----------|
| Unit Testing | Code coverage report | Automated (SonarQube/Jest) |
| Integration + System Testing | SIT Report | 02_SIT_REPORT.md |
| User Acceptance Testing | UAT Report | 03_UAT_REPORT.md |

### 2.2 Jenis Testing

**Functional Testing**
- Positive scenarios (happy path)
- Negative scenarios (error handling)
- Boundary value testing
- Input validation testing

**Performance Testing** (jika diperlukan)
- Load testing (normal capacity)
- Stress testing (beyond capacity)
- Endurance testing (sustained load)
- Tools: K6/JMeter

**Security Testing** (jika diperlukan)
- SAST: SonarQube + DefectDojo
- VAPT: Penetration testing (OWASP Top 10)
- Frekuensi: Setiap 3 bulan atau setelah major release

**Regression Testing**
- Full test suite execution
- Environment: Staging

**Mapping Jenis Testing → Output Documents:**

| Jenis Testing | Output Document | Template |
|---------------|-----------------|----------|
| Functional Testing | SIT Report (functional results section) | 02_SIT_REPORT.md |
| Performance Testing | Performance Test Report | 04_PERFORMANCE_TEST_REPORT.md |
| Security Testing (VAPT) | Security Test Report | 07_SECURITY_TEST_REPORT.md |
| Regression Testing | Regression Test Report | 08_REGRESSION_TEST_REPORT.md |

**Note:** Setiap jenis testing memiliki output document tersendiri untuk memastikan semua aspek quality tercatat dengan baik.

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

### 2.4 Performance SLA

| Kategori API | P95 Response Time | Error Rate | Prioritas |
|--------------|-------------------|------------|-----------|
| Critical (Auth, Payment) | < 1.500ms | < 0.1% | Mandatory |
| High-Priority (Search, Dashboard) | < 2.500ms | < 1% | Mandatory |
| Standard CRUD | < 3.600ms | < 5% | Mandatory |
| Batch/Report | < 10.000ms | < 10% | Important |

---

## 3. SCOPE TESTING

### 3.1 In Scope

**Fitur yang Akan Ditest:**

| No | Feature | Sub-Feature | Prioritas | Jenis Test |
|----|---------|-------------|-----------|------------|
| 1 | [Feature 1] | [Sub-feature 1.1] | Critical | Functional, Performance |
| 2 | [Feature 2] | [Sub-feature 2.1] | High | Functional, Security |
| 3 | [Feature 3] | [Sub-feature 3.1] | Medium | Functional |

**RBAC Roles:**
- [ ] Super Admin
- [ ] Admin
- [ ] User
- [ ] Guest

**Environments:**
- [ ] Development
- [ ] Staging
- [ ] Production (verifikasi saja)

### 3.2 Out of Scope

- [SubModul X.Y] - Ditest terpisah
- Backend infrastructure - Tanggung jawab DevOps
- Third-party integration - Tanggung jawab tim eksternal
- Legacy system (tidak ada perubahan)

### 3.3 Dependencies

| SubModul | Deskripsi Dependency | Impact |
|----------|---------------------|--------|
| [SubModul X.Y] | [Deskripsi] | High/Medium/Low |
| [SubModul X.Z] | [Deskripsi] | High/Medium/Low |

---

## 4. TEST ENVIRONMENT

### 4.1 Detail Environment

| Environment | URL | Tujuan | Status |
|-------------|-----|--------|--------|
| Development | [URL] | Testing oleh developer | [ ] Ready |
| Staging | [URL] | Pre-production testing | [ ] Ready |
| Production | [URL] | Verifikasi production | [ ] Ready |

### 4.2 Hardware & Software

**Hardware:**
- Desktop/Laptop: [Spesifikasi]
- Mobile: [Daftar device]

**Software:**
- OS: [Windows 10+, macOS, Android 11+, iOS 14+]
- Browser: [Chrome 120+, Firefox 115+, Safari 16+]
- Tools: [Postman, K6, Playwright]

---

## 5. JADWAL TESTING

| Phase | Tanggal Mulai | Tanggal Selesai | Durasi | PIC |
|-------|---------------|-----------------|--------|-----|
| Test Planning | [DD-MM-YYYY] | [DD-MM-YYYY] | [N] hari | QA Lead |
| Test Design | [DD-MM-YYYY] | [DD-MM-YYYY] | [N] hari | Tim QA |
| Test Execution | [DD-MM-YYYY] | [DD-MM-YYYY] | [N] hari | Tim QA |
| Bug Fixing & Retest | [DD-MM-YYYY] | [DD-MM-YYYY] | [N] hari | Dev + QA |
| UAT | [DD-MM-YYYY] | [DD-MM-YYYY] | [N] hari | Stakeholder |
| Go Live | [DD-MM-YYYY] | - | - | PM |

---

## 6. INTEGRASI QATM

### 6.1 Informasi QATM

**Spreadsheet URL:** [Google Sheets URL]
**Spreadsheet ID:** [44-character ID]
**Dashboard URL:** [Dashboard URL jika sudah register]

### 6.2 Struktur QATM

```
QATM Spreadsheet
├─ Summary          : KPI dashboard (auto-calculated)
├─ TC_Master        : Web/Mobile test cases
├─ TC_Execution     : Web/Mobile execution log
├─ API_Master       : API test cases
├─ API_Execution    : API execution log
├─ BugReport        : Bug tracking (Jira sync)
├─ PerfTest         : Performance test results
├─ Detail Finding - VAPT : Security findings
├─ Evidence - VAPT  : VAPT evidence & PoC
└─ Appendix         : Documentation
```

### 6.3 Format Test Case

**TC_Master (Web/Mobile):**

| Kolom | Deskripsi | Format |
|-------|-----------|--------|
| SubModul | Kode SubModul | [1.1] atau [PO] |
| TC_ID | Test case ID | [SubModule].[001] |
| Feature | Nama feature | [Nama feature] |
| Priority | Prioritas test | Critical/High/Medium/Low/Lowest |
| Platform | Target platform | Web/Mobile/Web & Mobile |
| Test Type | Jenis test | Functional/Regression/Smoke/Sanity |
| Automated | Status automation | Automated/Manual/To Do/Cannot be Automated |
| Role (RBAC) | User role | Admin/User/Guest |
| Scenario | Skenario test | [Deskripsi skenario] |
| Steps | Langkah test | Format Given-When-Then direkomendasikan |
| Expected Result | Hasil yang diharapkan | [Expected result] |

**API_Master:**

| Kolom | Deskripsi | Format |
|-------|-----------|--------|
| SubModul | Kode SubModul | [1.1] atau [API] |
| TC_ID | Test case ID | [SubModule].API.[001] |
| Endpoint | API endpoint | POST /api/v1/auth/login |
| Method | HTTP method | GET/POST/PUT/DELETE/PATCH |
| Priority | Prioritas test | Critical/High/Medium/Low/Lowest |
| Auth Required | Authentication | Bearer Token/Basic Auth/None |
| Request Body | Request payload | Format JSON |
| Expected Status | HTTP status code | 200/201/400/401/500 |
| Expected Response | Struktur response | Format JSON |
| SLA | Performance SLA | P95 < 1.500ms, Error < 1% |

### 6.4 Key Metrics

**Dari QATM Summary Tab:**

| Metric | Deskripsi | Kegunaan |
|--------|-----------|----------|
| Pass Rate % | (Passed / Total) * 100 | Exit Criteria |
| Open Blocker | Bug Medium-Critical BUKAN Closed/Won't Fix | Go/No-Go Decision |
| Prod Bugs | Bug di environment Production | Red Flag Alert |
| Execution Rate % | (Executed / Total) * 100 | Entry Criteria |
| Automation Rate % | (Automated / Total) * 100 | Process Improvement (opsional) |

---

## 7. ENTRY & EXIT CRITERIA

### 7.1 Entry Criteria

Sebelum test execution dimulai:

- [ ] Requirements complete dan approved
- [ ] Design document tersedia
- [ ] Environment ready dan stable
- [ ] Test cases direview dan approved
- [ ] Build deployed ke test environment
- [ ] QATM configured dan ready

### 7.2 Exit Criteria

Testing dianggap complete ketika:

**Mandatory:**
- [ ] Test Execution Rate = 100% (semua Critical/High dieksekusi)
- [ ] Pass Rate >= 95% (Web, API, Mobile)
- [ ] Open Blocker = 0
- [ ] Prod Bugs = 0
- [ ] VAPT Blocker = 0 (jika security testing dilakukan)
- [ ] Smoke Open Blocker = 0
- [ ] Performance SLA terpenuhi
- [ ] UAT sign-off diperoleh

**Formula Open Blocker (dari QATM):**
```
=SUMPRODUCT(
  (ISNUMBER(MATCH(BugReport!D5:D2000,
    {"Open","In Progress","Reopen","Fixed","Verified","In Progress VAPT","Done VAPT"},0)))*
  (ISNUMBER(MATCH(BugReport!C5:C2000,{"Critical","High","Medium"},0)))
)
```

**Conditional:**
- [ ] LOW priority test cases: Pass rate >= 90%
- [ ] Automation Rate >= 60% (jika applicable untuk regression suite)

---

## 8. MANAJEMEN DEFECT

### 8.1 Severity vs Priority

**Severity (Technical Impact):**

| Level | Definisi | Contoh |
|-------|----------|--------|
| Critical | System crash, data loss, security breach | App crash saat launch |
| High | Major functionality broken, tidak ada workaround | Tidak bisa login |
| Medium | Feature partially broken, workaround tersedia | Search lambat tapi masih berfungsi |
| Low | Minor issue, minimal impact | UI alignment tidak pas |

**Priority (Business Urgency):**

| Level | Response Time | Resolution Time |
|-------|---------------|-----------------|
| P0 (Critical) | Immediate | Same day |
| P1 (High) | 24 jam | 2-3 hari |
| P2 (Medium) | 3-5 hari | 1 minggu |
| P3 (Low) | 1-2 minggu | Sprint berikutnya |

### 8.2 Bug Status Workflow

```
QA Phase:
   Open → In Progress → Fixed → Verified

VAPT Phase (jika security-related):
   Verified → In Progress VAPT → Done VAPT → Closed

Exception:
   Any Status → Won't Fix (dengan approval)
```

### 8.3 Definisi Blocker

**Blocker = Bug yang menghalangi release:**

**Kriteria:**
- Priority: Critical/High/Medium
- Status: BUKAN ("Closed", "Won't Fix")

**Termasuk:**
- Open
- In Progress
- Reopen
- Fixed (Dev claim fixed, menunggu QA verification)
- Verified (QA verified, menunggu VAPT atau release)
- In Progress VAPT (Security testing sedang berjalan)
- Done VAPT (VAPT done, menunggu final sign-off)

**Tidak Termasuk:**
- Closed (Released ke production)
- Won't Fix (Rejected dengan approval)

### 8.4 Format Bug Report

**BugReport Tab Columns:**

| Kolom | Deskripsi |
|-------|-----------|
| Type | Web/Mobile/API/Security |
| Priority | Critical/High/Medium/Low/Lowest |
| Status | Open/In Progress/Fixed/Verified/Closed/etc |
| Feature | Nama feature |
| Bug ID | Jira ticket ID (PROJ-123) |
| Title | Deskripsi singkat |
| Link | URL ke Jira atau evidence |
| Environment | Dev/Staging/UAT/Production |
| Reporter | Siapa yang menemukan bug |
| Comment | Catatan tambahan |

---

## 9. MANAJEMEN RISIKO

### 9.1 Test Risks

| Risiko | Probabilitas | Impact | Mitigasi |
|--------|--------------|--------|----------|
| Perubahan requirement saat testing | Medium | High | Freeze scope saat test execution, change request process |
| Environment tidak stabil | Low | High | Environment readiness checklist, dukungan DevOps |
| Test data tidak lengkap | Medium | Medium | Persiapan test data di entry criteria |
| Critical blocker dekat deadline | Low | High | Test critical features dulu, daily bug triage |
| Resource constraint | Medium | High | Prioritize test scenarios, automation untuk regression (jika applicable) |
| Integration dependency delay | Medium | High | Koordinasi early, mock services untuk isolated testing |

### 9.2 Project Risks

| Risiko | Mitigasi |
|--------|----------|
| Development delay | Buffer time di schedule, parallel testing |
| Third-party service downtime | Mock external services |
| UAT resource tidak available | Early coordination, flexible schedule |

---

## 10. REFERENSI

### 10.1 Dokumen Terkait

| Dokumen | Link/Lokasi |
|---------|-------------|
| PRD (Product Requirements Document) | [Link] |
| FSD (Functional Specification Document) | [Link] |
| Technical Design Document | [Link] |
| API Documentation | [Link] |
| QATM Spreadsheet | [Link] |
| QA Dashboard | [Link] |

### 10.2 Tools & Resources

| Tool | Tujuan | URL |
|------|--------|-----|
| JIRA | Bug tracking | [Link] |
| Postman | API testing | [Link to collection] |
| K6 | Performance testing | [Link to scripts] |
| SonarQube | Code quality | [Link] |
| DefectDojo | Vulnerability management | [Link] |

### 10.3 Glossary

| Term | Definisi |
|------|----------|
| QATM | QA Test Management Template (berbasis Google Sheets) |
| Blocker | Bug yang menghalangi release (Medium-Critical, BUKAN Closed) |
| Smoke Test | Verifikasi cepat untuk critical functionality |
| Regression Test | Re-test existing features setelah code changes |
| VAPT | Vulnerability Assessment & Penetration Testing |
| SAST | Static Application Security Testing (code analysis) |
| SLA | Service Level Agreement (performance target) |
| P50/P95/P99 | Percentile metrics (50th, 95th, 99th percentile) |
| VU | Virtual User (simulated concurrent users di perf test) |
| RPS | Requests Per Second (throughput metric) |

---

## APPENDIX

### A. Informasi Kontak

| Role | Nama | Email |
|------|------|-------|
| QA Lead | [Nama] | [Email] |
| QA Engineer | [Nama] | [Email] |
| Project Manager | [Nama] | [Email] |
| Technical Lead | [Nama] | [Email] |

### B. Definisi QATM Tab

**Summary Tab:** KPI dashboard auto-calculated (Pass Rate, Open Blocker, dll)

**TC_Master Tab:** Repository test case Web/Mobile

**TC_Execution Tab:** Log eksekusi Web/Mobile dengan status tracking

**API_Master Tab:** Repository test case API

**API_Execution Tab:** Log eksekusi API

**BugReport Tab:** Bug tracking dengan Jira sync

**PerfTest Tab:** Hasil performance test (data K6/JMeter)

**Detail Finding - VAPT Tab:** Temuan security dari penetration testing

**Evidence - VAPT Tab:** Screenshot PoC dan evidence retest

**Appendix Tab:** Workflow guide dan dokumentasi

---

**END OF DOCUMENT**

_Versi: 1.0_
_Template: Test Plan v2.0 - Clean & Professional_
_© QA INA Digital_
