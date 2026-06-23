🧪 Arattai Messenger — Manual Testing Project
Independent QA Practice Project | Arattai is a real instant messaging application developed by Zoho Corporation. This project was independently undertaken to gain hands-on manual testing experience on a live production application.

📌 Project Overview
FieldDetailsApplication NameArattai MessengerDeveloped ByZoho CorporationPlatformAndroidProject TypeIndependent Manual Testing PracticeTesterHarish KDurationJanuary 2024Total Test Cases80+Defects Logged30+Retest Closure Rate100%Release Cycles3 (Smoke → Functional → Regression)OS Versions CoveredAndroid 8, 9, 10, 11, 12 (via BrowserStack)


📋 Modules Tested
#ModuleTest CasesKey Focus1Login & Authentication11OTP validation, BVA on mobile number, session handling2One-to-One Chat10Message delivery, network switch, delete/reply features3Group Chat10Group creation, BVA on name length, admin access control4Audio Calls5Call connect/disconnect, mute, network drop behaviour5Video Calls4Camera toggle, Android 9 compatibility, video off feature6Media Sharing9BVA on 16MB file size limit, file types, image sharing


🔍 Testing Types Performed
✅ Functional Testing
✅ Smoke Testing
✅ Regression Testing
✅ UI Testing
✅ Compatibility Testing (Android 8–12)
✅ Exploratory Testing
✅ Ad-hoc Testing
✅ Network Testing
✅ Boundary Value Analysis (BVA)
✅ Equivalence Partitioning (EP)


🛠️ Tools & Technologies
CategoryToolsDefect TrackingJIRA, BugzillaCompatibility TestingBrowserStackTest DocumentationMicrosoft ExcelVersion ControlGit, GitHub

📂 Repository Structure
arattai-messenger-qa-testing/
│
├── README.md
│
├── test-cases/
│   ├── TC_Login_Module.xlsx
│   ├── TC_Chat_Module.xlsx
│   ├── TC_GroupChat_Module.xlsx
│   ├── TC_AudioVideo_Module.xlsx
│   └── TC_MediaSharing_Module.xlsx
│
├── defect-reports/
│   ├── Bug_Report_Login.xlsx
│   ├── Bug_Report_Chat.xlsx
│   ├── Bug_Report_MediaSharing.xlsx
│   └── Master_Defect_Log.xlsx
│
├── traceability-matrix/
│   └── RTM_Arattai.xlsx
│
└── test-execution-reports/
    └── Test_Execution_Report_All_Cycles.xlsx


📊 Defect Summary
ModuleTotal BugsHighMediumLowLogin3201Chat3120Group Chat2200Audio / Video Calls2101Media Sharing2020Total12642


🔬 Key Test Techniques Applied
Boundary Value Analysis (BVA)
Mobile number field — tested at 9 digits (min-1), 10 digits (valid boundary), 11 digits (max+1)
File size limit (16MB) — tested at 15.9MB, 16.0MB, 16.1MB
Group name character limit (25 chars) — tested at 24, 25, and 26 characters

Equivalence Partitioning (EP)
Mobile number — Valid class (10-digit numeric), Invalid class (alphabets, special chars, short/long numbers)
OTP field — Valid class (6-digit numeric), Invalid class (alphabets, wrong digits)
File type — Valid class (jpg, pdf, mp4), Invalid class (exe, zip unsupported formats)


🐛 Notable Defects Found
Bug IDModuleTitleSeverityBUG_001ChatMessage not delivered on WiFi → Mobile data switch (silent failure)HighBUG_002Group ChatGroup name truncated without ellipsis beyond 25 chars on Android 8MediumBUG_003LoginOTP field accepts alphabetic characters — no input validationHighBUG_004Video CallsVideo feed freezes on Android 9 after camera toggleHighBUG_005Media SharingNo error message shown when uploading file above 16MBMediumBUG_008Group ChatNon-admin users can see the Remove Participant optionHigh


🔄 Test Execution Cycles
Cycle 1 — Smoke Testing
Verified all core features work at a basic level before full testing
6 test cases executed | 5 Passed | 1 Failed

Cycle 2 — Functional Testing
In-depth testing of all 6 modules with BVA and EP techniques
13 test cases executed | 9 Passed | 4 Failed | 4 Defects raised

Cycle 3 — Regression Testing
Re-executed after defect fixes to ensure no new issues introduced
10 test cases executed | 10 Passed | 0 Failed | Zero escaped defects


📎 Traceability
All test cases are mapped to requirements in the RTM (Requirements Traceability Matrix) available in the traceability-matrix/ folder. This ensures:
Every requirement has at least one test case
All defects are linked to the test case that discovered them
Full coverage visibility across all 6 modules
