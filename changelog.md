# Changelog

## 19-06-2025 — functional requirements Table and use case diagram syntax Revised (CH-01)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-01 | SRS.md (§ 3.0 Table 5, figure 2) |• Corrected the use case diagram syntax and content defect . <br> • A new column of use case ids is added to the functional requirement table that correctly label them to help with traceability| Hazim | The use case diagram was drawn in correctly according to the project scope.. “Receive Budget Allocation Request” is modelled as an «include» of “Submit Budget Allocation Request”—but it’s a separate actor activity, not a sub‑step. <br> Use Case IDs were added to align with [ISO/IEC/IEEE 15288:2015, 6.4.3.3 d) 2)] Maintain traceability of the system[/software] requirements.Use case ids help with tracing it across the document for easier identification / SEC-3.0 (S001) |

## 19-06-2025 — functional requirements Table (CH-02)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-02 | SRS.md (§ 3.0 Table 5 3.1) | • Reformatted the Functional Requirements table for clarity: split multi-part requirements () into “a”/“b” sub‑items reduce ambiguity  . <br> • A clearer description for club officer responsibilities. <br> •	Actor misassignment in UC012 was corrected to the right primary actor (Campus Space Reservation Database listed as primary actor instead of Club Officer). <br> • Fixed vague terms discovered across inspection sessions S001-003.| Hazim | 	Multiple functional requirements bundled multiple responsibilities and system use cases into a single requirement, which violated the atomicity principle of requirement writing as described in section 5.2.5 of ISO/IEC 2018, "Singular" principle.<br> Vague terminology was replaced to solidify sentences and remove subjectivity. <br> Actor misassignment correction ensures the integrity of the use case logic and system behavior mapping. / SEC-3.1 (S003) |

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

## 20-06-2025 — Use case table defintions (CH-13)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-13 | SRS.md (§ 3.1 use case Tables) | Wrote main / alternative flow for each of the available use cases tables, following the activity diagram provided semantics. | Hazim | Missing main and alternative flows caused content aswell as document defects, as the use case tables lacked clear execution logic, making it difficult to understand user-system interactions. It created validation gaps, and misaligned developer understanding. (Session S001)|

## 21-06-2025 — BookVenue Alt Flow Added (CH-14)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-14 | SRS.md (§ 3.1.1.2 Book Venue - Alternative Flow) |Added alternative flow for unavailable venue scenario. | Nelly | The use case does not include an alternative flow to handle scenarios where the selected venue is already booked or unavailable. This results in incomplete behavioural logic. |

## 21-06-2025 — Product Goals Inserted (CH-15)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-15 | SRS.md (§ 1.1 Purpose - Product Goals) | Added missing goals | Nelly | No product goals were originally included to support the system’s rationale and traceability. |

## 21-06-2025 — Vague Language Corrections (CH-16)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-16 | SRS.md (§ Page 109, 110, 111) | Clarified vague and subjective terms in multiple sections of the SRS by replacing phrases like  "may be involved", and "adequate” with specific, measurable wording to improve document precision and validation readiness. | Nelly | Several descriptions in the SRS contain vague or subjective language such as  "may be involved", “adequate”, and “ease of use”, which reduce the clarity and make validation difficult. |

## 21-06-2025 — Requirements Tracebility Matrix Added (CH-17)

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-17 | SRS.md (§ 3.8.6 Requirements Traceability) | Added a matrix mapping FR/NFR/UC to product goals to support validation and alignment. | Nelly | The initial SRS version lacked a traceability matrix to link requirements with use cases and product goals. |

## 21-06-2025 — Use Case, Glossary & Policy Enhancements

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-18 | SRS.md (§ 3.1 Use Case Tables) |Added missing UC011 – Receive Notifications, aligned with FR-04a/b/c | Si Ting | FR-04 was unlinked to any use case, breaking traceability and test planning.|

## 21-06-2025 — Use Case, Glossary & Policy Enhancements

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-19 | SRS.md (§ 3.1 UC002, UC006)   | Wrote alternative and exception flows for UC002 and UC006   | Si Ting | Use cases lacked behavioral error handling, causing content and validation gaps (Session S004).|

## 21-06-2025 — Use Case, Glossary & Policy Enhancements

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-20 | SRS.md (§ 5.2 Glossary)    | Added missing acronyms: RBAC, TLS, OAuth2, REST, Docker, WCAG, KPI  | Si Ting | Glossary incomplete and violated ISO 29148 glossary inclusion criteria; key terms not explained. |

## 21-06-2025 — Use Case, Glossary & Policy Enhancements

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-21 | SRS.md (§ 2 Version Info)     | Added version control metadata (Version number, Author, Last update)    | Si Ting |   Document lacked traceable version management metadata.|

## 21-06-2025 — Use Case, Glossary & Policy Enhancements

| Change ID | File / Area | Description of Change | Author | Reason |
|-----------|-------------|-----------------------|--------|--------|
| CH-22 | SRS.md (§ 3.5 DRR-04)    | Added missing acronyms: RBAC, TLS, OAuth2, REST, Docker, WCAG, KPI  | Si Ting | DRR-04 was vague and compliance-risky; lacked implementation or retention logic.   |

