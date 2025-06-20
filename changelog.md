# Changelog

## 20-06-2025 — Non-functional Attribute Tables Revised (CH-03)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-03 | SRS.md (§ 3.7 Tables 3.27–3.31) | Added “Metric / Unit” and “Rationale / Source” columns; converted all descriptions into measurable statements (e.g., REL-01 ≤ 60 s MTTR, SEC-01 TLS 1.3 + AES-256); aligned with ISO 29148 §9.4.4 & Session S002 defects | Zhi Xuan | Close Documentation Defect DOC-3.7-01 and Agreement issues AVAIL-01 / SEC-01 (S002) |

## 20-06-2025 — Reference List Overhaul (CH-04)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-04 | SRS.md (§ 2 References) | • Replaced ISO 29148 entry with full APA-7 format (corporate authors, italicised title, correct DOI).<br>• Added missing sources: OAuth 2.0 RFC 6749, WCAG 2.1 guideline, Docker Desktop manual v4.30, Firebase Cloud Messaging docs, MMU IT security & retention policy.<br>• Numbered list remains in alphabetical order by first author / organisation. | Zhi Xuan | Close Documentation Defects DOC-REF-01 & DOC-REF-02 (Session S002) |

## 20-06-2025 — Glossary & Acronyms Update (CH-05)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-05 | SRS.md (§ 1.4 Definitions) | Inserted a comprehensive, alphabetised table that now includes 12 previously-missing acronyms (RBAC, OAuth 2.0, REST, TLS, WCAG, KPI, Docker, API, SMTP, CRUD, FCM, SSO) alongside existing key terms; updated caption to “Definitions, acronyms, and abbreviations”. | Zhi Xuan | Resolve Documentation Defect *1.4 Definitions — Table 37* (Session S002) |

## 20-06-2025 — Venue / RSVP / Notification Requirements Refactor (CH-06)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-06 | SRS.md (Table 3.1) | *FR-02* split corrected: **FR-02a Check Venue Availability** (UC012) & **FR-02b Submit Venue Booking Request** (UC002).<br>*FR-03* split corrected: **FR-03a Submit RSVP** (UC011) & **FR-03b View Attendance Count** (UC003).<br>*FR-04* now decomposed by **channels** — **FR-04a Email Notifications**, **FR-04b Push Notifications**, **FR-04c In-app Notifications**; each covers approval / rejection / action-required across all three workflows. | Zhi Xuan | Close Content Defects FR-02, FR-03, FR-04 (Session S002) |

## 20-06-2025 — Performance SLA Refinement (CH-07)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-07 | SRS.md (§ 3.2 Performance Requirements) | • Replaced ambiguous wording in PR-01 with measurable concurrency + response-time SLA (500 users, P95 ≤ 2 s). <br>• Replaced PR-02 “respond within 2 s” with tighter, clearly-scoped login SLA (P95 ≤ 1 s, worst-case ≤ 1.5 s). | Zhi Xuan | Close Content Defects PR-01 & PR-02 (Session S002) |

## 20-06-2025 — Localisation Requirement Quantified (CH-08)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-08 | SRS.md (§ 3.3 Usability – Table 3.16) | Updated UR-02 to specify ≥ 95 % bilingual coverage, a UI language toggle in user settings, and a hard cap of 5 % untranslated fallback strings per release. | Zhi Xuan | Resolve Content Defect UR-02 (Session S002) |

## 20-06-2025 — Availability, Security & Maintainability Refactor (CH-09)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-09 | SRS.md (§ 3.7 Tables 3.28–3.30) | • **AVAIL-01** now guarantees ≥ 99.5 % uptime **24 × 7** with < 2 h/mo scheduled maintenance announced ≥ 48 h in advance.<br>• Split **SEC-01** into: (a) TLS 1.3 + AES-256 encryption, (b) RBAC with four roles & SoD, (c) audit log retention ≥ 1 yr & quarterly OWASP-Top-10 pen-test pass rate 100 %.<br>• **MAIN-01** now requires ≥ 80 % unit-test coverage, < 6 coupling index, ≤ 15 average cyclomatic complexity, and 100 % public REST API documented in OpenAPI 3.0. | Zhi Xuan | Close content defects AVAIL-01, SEC-01, MAIN-01 (Session S002) |

## 20-06-2025 — Usability, Data, Interface & Portability Fixes (CH-10)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-10 | SRS.md (Tables 3.16, 3.18, 3.24, 3.31) | • **UR-01** now unambiguous: max 3 user interactions (click, tap, key-press) to complete top-3 tasks and ≥ 90 % users succeed on first attempt in moderated tests.<br>• **DBR-02** aligned with PR-01: 500 concurrent users **and** ≥ 50 tx/s mixed R/W at P95 latency ≤ 300 ms.<br>• **INT-13**: API URI `/api/v1/…`, `Content-Type: application/json`, responses include HAL `_links` for discoverability; backward compatibility guaranteed for minor updates.<br>• **PORT-01**: clarified target OS (Ubuntu 22.04 LTS, Windows Server 2022), Docker 20.10+, Kubernetes ≥ 1.29 deployment, Helm charts provided. | Zhi Xuan | Close S002 defects UR-01, DBR-02, INT-13, PORT-01 |

## 20-06-2025 — Agreement-Mismatch Closure (CH-11)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-11 | SRS.md (§ 3.8 C Agreement Defects & Conflict Analysis) | • Added “Resolved in CH-08” note to UR-02 row and “Resolved in CH-09” note to AVAIL-01 row.<br>• Removed severity for resolved items.<br>• Updated Conflict C-04 status to **Resolved (Y)** in § 3.8.4. | Zhi Xuan | Document closure of outstanding Agreement defects after implementing quantifiable localisation and 24 × 7 availability. |

## 20-06-2025 — Conflict-Resolution Evidence Added (CH-12)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-12 | `Conflict_Resolution_Proofs/` folder + SRS.md (§ 3.8) | • Added five PNG screenshots (**C-01.png … C-05.png**) that capture the Teams negotiations for each conflict.<br>• Embedded references to those images in the Conflict Analysis / Resolution tables and labelled them IMG-001 → IMG-005.<br>• Merged the standalone “Supporting Information” Word doc into **TT5L_G6_SRS.md** so all validation artefacts live in a single source. | Zhi Xuan | Provide instructor-requested proof of conflict-resolution technique and keep SRS self-contained. |
