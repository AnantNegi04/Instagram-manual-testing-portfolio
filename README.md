# Instagram Manual Testing Portfolio

**Tester:** Anant Negi  
**Type:** Self-Directed System Testing Project  
**Platforms:** Android (Realme Narzo 20a – Android 11) · Windows 11 (Lenovo LOQ, i5 12th Gen)  
**Duration:** January 2026 – February 2026  
**Status:**  Completed

---

##  Project Objective

To perform end-to-end **system-level manual testing** of the Instagram application, simulating a real-world QA cycle from requirement understanding to test summary reporting.

The project covers core application modules with a focus on:
- Functional correctness across positive and negative scenarios
- Stability under real-world conditions (network interruptions, background states, rapid switching)
- Cross-platform behavioral consistency (Android vs Windows)
- Structured defect documentation following industry-standard practices

---

##  Repository Structure

```
instagram-manual-testing-portfolio/
│
├── test-cases/                  # Module-wise test case documentation
│   ├── LOGIN_TEST_CASES
│   ├── DM_TEST_CASES
│   ├── Home_feed_test_cases
│   ├── Navigation_Test_Cases
│   └── MULTI_ACCOUNT_NAV
│
├── bug-reports/                 # Defect log with severity, priority & evidence
│   └── BUG_REPORT
│
├── test-execution/              # Execution results and test run summaries
│
├── rtm/                         # Requirement Traceability Matrix
│
└── project-summary/             # Full project overview and metrics
    └── 00_Project_Summary
```

---

##  Modules Covered

| Module | Functional | Non-Functional | Stability | Cross-Platform |
|--------|------------|----------------|-----------|----------------|
| Login  | ✅ | ✅ | ✅ | ✅ |
| Signup | ✅ | — | — | — |
| Forgot Password | ✅ | — | — | — |
| Home Feed | ✅ | ✅ | ✅ | ✅ |
| Navigation | ✅ | ✅ | ✅ | — |
| Multi-Account Navigation | ✅ | ✅ | ✅ | — |
| Direct Messaging – Basic | ✅ | — | — | — |
| Direct Messaging – Media | ✅ | — | — | — |
| Direct Messaging – Stability | — | ✅ | ✅ | — |

---

## Test Metrics

| Metric | Count |
|---|---|
| Total Test Cases Designed | 150+ |
| Total Test Cases Executed | 80+ |
| Platforms Tested | 2 (Android + Windows) |
| Defects Identified | 1 (High Severity) |
| Modules Covered | 7 |
| RTM Prepared | ✅ Yes |
| Test Summary Report | ✅ Yes |
| Evidence Captured | ✅ Screen Recordings |

---

## Testing Types Applied

- **Functional Testing** — positive and negative flows across all modules
- **Non-Functional Testing** — network handling, slow connectivity, no connectivity
- **Stability Testing** — kill app during send, logout mid-upload, background state, rapid navigation
- **State Transition Testing** — DM message states (Sent → Delivered → Seen), session retention
- **Boundary Value Analysis** — character limits, empty fields, oversized media
- **Equivalence Partitioning** — valid/invalid credential classes
- **Cross-Platform Testing** — behavioral comparison between Android and Windows
- **Multi-Device Sync Testing** — simultaneous login and message sync across two devices
- **Regression Awareness** — retesting after defect fixes

---

## Sample Defect

**Bug ID:** BUG_001  
**Title:** Home Feed Refresh Fails on Windows App  
**Module:** Home Feed  
**Severity:** High  
**Priority:** High  
**Environment:** Windows 11  
**Steps to Reproduce:**
1. Launch Instagram on Windows 11
2. Login to an existing account
3. On the home feed, scroll down to trigger pull-to-refresh

**Expected:** Feed refreshes and loads new content  
**Actual:** Refresh fails silently — no new content loads, no error message shown  
**Status:** Logged  
**Evidence:** Screen recording attached in bug-reports/

---

##  Notable Test Scenarios

These test cases go beyond standard happy-path coverage and reflect real-world edge case thinking:

- **Kill app immediately after pressing send** — verifies message delivery integrity
- **Logout mid-upload of large media file** — checks retry/failure handling on re-login
- **Network switch (WiFi → Mobile Data) during login** — validates session continuity
- **Send message then immediately minimize app** — tests background delivery
- **Rapid account switching across all screens for 2 minutes** — stress tests session management
- **Send large video on 40kbps throttled network** — validates graceful degradation
- **Simultaneous message send from two devices on same account** — tests sync consistency
- **Login with leading space in username vs password** — username trims (passes), password fails (correct behavior)
- **View-once media delivery verification** — validates single-access enforcement

---

## Tools Used

| Tool | Purpose |
|---|---|
| MS Excel / Google Sheets | Test case documentation, RTM, bug reports |
| Screen Recorder (Android + Windows) | Evidence capture for defects and execution |
| Google Drive | Structured artifact repository |
| GitHub | Version-controlled portfolio hosting |

---

## STLC Followed

```
1. Requirement Understanding
        ↓
2. Test Case Design (Functional + Non-Functional)
        ↓
3. Test Execution (Android + Windows)
        ↓
4. Defect Logging (with evidence)
        ↓
5. Retesting Awareness
        ↓
6. Test Summary Reporting
        ↓
7. RTM Update (traceability maintained)
```

---

##  Key Learnings

- Cross-platform behavior differences are subtle but critical — the Windows Home Feed bug would have gone undetected in Android-only testing
- Stability edge cases (kill app, mid-upload logout, network interruption) reveal application robustness that functional testing alone misses
- State handling in DM (Sent → Delivered → Seen) requires careful test design to validate correctly
- Session retention across account switches and app restarts is a common real-world failure point
- Structured bug reporting with severity, priority, reproducibility, and evidence makes defects actionable for developers

---

## About the Tester

I'm a QA Engineer with 1 year 9 months of IT industry experience (Citrix L1 Support at HCLTech), transitioning into QA Engineering. This project was built to apply STLC concepts hands-on and demonstrate structured testing thinking to potential employers.

📧 anantnegi04@gmail.com  
📍 Kotdwar, Uttarakhand, India  
🔗 [LinkedIn](https://linkedin.com/in/) ← *www.linkedin.com/in/anant-negi-5a0811401*

---

*This is a self-directed learning project. Instagram is owned by Meta. This repository is for educational and portfolio purposes only.*
