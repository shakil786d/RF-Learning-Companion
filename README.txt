RFIC Learning Companion — Android-friendly PWA

INSTALL ON ANDROID
1. Host this folder on an HTTPS static host (for example GitHub Pages, Netlify, or your own HTTPS server). Service workers and installable PWA behavior require HTTPS (localhost is also allowed for testing).
2. Open the hosted index.html in Chrome on Android.
3. Open Chrome menu (⋮) and choose "Install app" or "Add to Home screen".
4. Launch RFIC Companion from your home screen. After the first successful load, the app shell works offline.

DATA
- Study logs, timer sessions, checklist state, notes and assessment scores are stored in localStorage on this device/browser.
- Export your data from Syllabus > Export my data before clearing browser data or switching phones.
- This is an offline-first web app, not a signed APK from the Play Store.

CHATGPT ASSESSMENT TRANSFER
- In Assessments, tap "Copy assessment prompt" and paste it into this ChatGPT conversation.
- At the end of the assessment, ask ChatGPT to return JSON in this shape:
{"type":"rfic-assessment","name":"Week 1","score":78,"date":"YYYY-MM-DD","feedback":"Summary","strengths":["..."],"gaps":["..."],"next_steps":["..."]}
- Copy that JSON, return to the app, paste it into Import your ChatGPT result and tap Save.
- Direct automatic reading of a private ChatGPT conversation is not available to a standalone app. The structured JSON import is the safe bridge.

NOTE
The timer records elapsed focus sessions; finishing a session adds rounded minutes to the current day. A session left running across browser closure is recoverable while the page remains active; always finish sessions before leaving for best accounting.
