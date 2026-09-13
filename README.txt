CWSS TEACHER MANAGEMENT SYSTEM — STAGE 3A
Offline App Shell

WHAT THIS PACKAGE DOES
- Provides a real PWA application shell that can be cached by the phone.
- Keeps the existing Google Apps Script system as the backend.
- Uses the existing localStorage offline teacher data and Stage 2 attendance queue.
- When online, the shell communicates with the Apps Script page through a hidden bridge iframe.
- When offline, the shell opens from the service-worker cache and uses the teacher data already saved on the phone.

IMPORTANT
The file index.html contains a one-time setup screen because the current Apps Script deployment URL was not embedded in this package. The teacher/admin pastes the existing /exec URL once. The URL is then stored on that phone.

HOSTING
This package is designed for static HTTPS hosting such as GitHub Pages. GitHub Pages can publish static HTML, JavaScript, CSS and other files over HTTPS.

FILES
- index.html — CWSS offline PWA shell
- sw.js — service worker that caches the shell
- manifest.json — installable app definition
- icon-192.png / icon-512.png — app icons

STAGE 3A TEST
1. Publish this folder to an HTTPS static host.
2. Open the published index.html while online.
3. Paste the existing CWSS Apps Script /exec link when prompted.
4. Allow the portal to load and verify that the normal CWSS information appears.
5. Close the page.
6. Turn off Wi-Fi and mobile data.
7. Open the PWA URL again.
8. The CWSS shell should open without the Google server being reachable.

DO NOT replace the live Apps Script Index.html with the static shell.
Use Index_STAGE3A_BACKEND.html as the Apps Script Index.html replacement after reviewing/testing it.
