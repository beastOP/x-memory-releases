# X Memory

An Android app that saves accessible text from public X Home posts to a private archive on your phone and exports each visit as Markdown to your Google Drive.

[Download the latest APK](https://github.com/beastOP/x-memory-releases/releases/latest)

Requires Android 14 or newer, Google Play services and the native X app. This repository contains signed downloads and installation information.

## Installation status

This is an early testing release. Google Play Protect can block installation of an APK downloaded from a browser or messaging app because X Memory declares an Accessibility service. Moving the download to GitHub does not resolve that restriction. This release is not Google-approved, and installation on affected phones is not verified. Keep Play Protect enabled. See [Google's explanation and appeal route](https://developers.google.com/android/play-protect/warning-dev-guidance#app-blocked).

If you already have X Memory, install as an update. Do not uninstall to fix an installation error: uninstalling deletes your local archive and pending uploads. Updates use the existing release signing certificate.

Google Drive authorization is currently configured for invited test accounts. A shared APK alone does not grant a new account access. Ask the maintainer to add your Google account privately, not in a public GitHub issue. Google test authorizations may expire and need reconnection.

## Setup after installation

1. Open X Memory and accept the explanation before enabling its Accessibility service. Android may separately require App info → menu → Allow restricted settings. This setting does not fix a Play Protect installation block.
2. Connect your invited Google Drive account and allow notifications.
3. Enable capture, open X's Home tab, scroll, then leave X. View the visit in X Memory; uploads default to Wi-Fi.

## Data and permissions

Capture starts paused and can be paused at any time. X Memory uses Accessibility to read the supported English X Home feed. It excludes other apps, messages, typing, locked/private and unrecognized screens. This is best-effort text capture, not a screenshot or audio recorder; fast scrolling and unsupported layouts can miss posts.

Saved text stays in private app storage and is uploaded to the Google Drive account you connect, using the limited `drive.file` scope. Optional creator portraits are fetched directly from public X profile pages and image servers; these requests disclose the requested public handle to X. There is no separate X Memory server. The APK contains no personal archive or account credentials.

Existing legacy image queues, if present from older installations, have a separate recovery path that uses the user's configured Groq key. New text captures do not use Groq or language models.

## Verify a download

Each release includes `SHA256SUMS.txt`. Package: `dev.jarvis.xmemory`.

Release signing certificate SHA-1: `CE:8A:51:1F:EC:4B:FE:40:68:31:F0:37:48:16:6F:48:9E:76:96:29`.
