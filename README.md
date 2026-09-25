# FLORA for After Effects: setup guide (beta)

Capture composition frames, generate video with FLORA, run reusable Techniques, and bring finished takes straight into After Effects. This repository holds the setup guide only. The plugin itself is a ZIP file you download from Google Drive. No GitHub account is needed.

## Download
**[Download the latest plugin ZIP from Google Drive](https://drive.google.com/drive/folders/1e_QzTLhbZDFxxdwHsV81VOhE3lLUNNCW?usp=sharing)** and open the newest `flora-ae-plugin-…-beta.zip` in the folder. Only use the ZIP from this link.

## You need
- After Effects 2025 (25.x) on macOS. AE 2026 should load but is not fully verified. Windows is experimental and untested in AE.
- A FLORA account with API access (currently a paid plan with credits). In FLORA open **Settings → API Keys** and copy your own key. See [FLORA API setup](https://developer.flora.ai/api/).

## Install (Mac)
1. Download the ZIP above, unzip the whole folder, and keep its contents together.
2. Quit After Effects.
3. Double-click **Install FLORA - Mac.command** and wait for "FLORA installed".
4. Open AE and choose **Window → Extensions → FLORA**. Dock the panel where you like.
5. In AE **Settings/Preferences → Scripting & Expressions**, enable **Allow Scripts to Write Files and Access Network**.
6. Paste your API key into the panel, connect, and choose your workspace.

**If macOS blocks the installer:** open Terminal, type `bash ` (with a trailing space), drag `scripts/install-mac.sh` from the unzipped folder into the window, and press Return.

## Install (Windows, experimental)
Unzip, quit AE, double-click **Install FLORA - Windows.cmd**, then follow steps 4–6 above. Keys are not saved between sessions on Windows, and work-area movie export is Mac-only.

## Good to know
- This is an unsigned beta. The installer turns on Adobe's per-user `PlayerDebugMode` so AE loads it. It needs no admin access. To undo it on Mac: `defaults delete com.adobe.CSXS.12 PlayerDebugMode` (only if no other unsigned extension needs it).
- Your key stays private: held in memory, optionally saved in the macOS Keychain. It is never written to project files.
- Generations use your own credits. If a submission reports "uncertain", check the run in FLORA before retrying.
- **Update:** download the newest ZIP from the same Drive folder, quit AE, and run the installer from it. History is kept and the old panel is backed up.
- **Remove:** quit AE and delete the `ai.flora.aftereffects` folder from `~/Library/Application Support/Adobe/CEP/extensions`.

## Troubleshooting
- **Not in the Extensions menu:** confirm AE 25.x/26.x, unzip fully, rerun the installer, fully quit and reopen AE.
- **Frame capture fails:** enable the AE scripting permission above, open a comp, and put the playhead on a visible frame.
- **Connection fails:** check your key, network, API access, and workspace membership. Never post a key publicly.

Problems? Send the person who shared this guide the exact error message and your AE version. See the [changelog](CHANGELOG.md).
