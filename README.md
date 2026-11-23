# PC Pulse Companion

**Turn your phone into a remote for your Windows PC.**

PC Pulse Companion is the Windows program that works with the **PC Pulse** Android app. Install it on your PC, scan a QR code with your phone, and you can control and check on your computer from anywhere in the house.

> This repository contains **downloads only**. There is no source code here.

## [⬇ Download the latest version](../../releases/latest)

Pick **`PCPulseCompanion-Setup.exe`** from the latest release, run it, and follow the steps. You will be asked to accept the terms of use during setup and again the first time the program starts.

**Requirements:** Windows 10 or 11 (64-bit) and the PC Pulse app on an Android phone. Your phone and PC need to be on the same network.

---

## What you can do

- **Trackpad and keyboard.** Move the mouse, scroll, type and press shortcuts from your phone.
- **See and control the screen.** View your PC's screen and tap or click on it.
- **Gamepad, up to four players.** Each phone becomes its own virtual Xbox 360 controller (Player 1 to 4), so friends can play together on your PC. Needs the free ViGEmBus driver, which the program can install for you.
- **Scenes and automations.** Chain steps like "switch to TV mode, set the volume, open a website" into one tap, or run a scene automatically when a program starts or closes, or at a set time.
- **Display and sound.** Switch display profiles, resolutions, refresh rates, the main monitor, the sound output and brightness.
- **Launch things.** Start games, programs and websites with shortcuts you arrange yourself.
- **PC health.** See CPU, graphics card, memory and storage use and temperatures, with your graphics card's real name.
- **Power.** Lock, sleep, restart or shut down.
- **Files and clipboard.** Send files to a shared folder and share clipboard text.
- **Web app.** Browsers and iPhones can use a basic version without installing anything. It is **not encrypted**, so it is off until you turn it on, and only use it on a network you trust.

## Setting up

1. Install PC Pulse Companion and let it start.
2. In the program, click **Pair a device**. A QR code appears.
3. In the PC Pulse app on your phone, choose **Add PC** and scan the QR code.
4. If your phone cannot find the PC, allow it through the Windows Firewall when the program asks. Your home network needs to be set to **Private** in Windows (Settings > Network & internet > Properties).

You can pair several phones, and one phone can be paired with several PCs.

## Security

- **The connection between your phone and PC is always encrypted** (TLS). It cannot be turned off.
- **Pairing uses a QR code** that identifies your PC, so the phone knows it is talking to the right computer and not an impostor.
- **You choose what each phone may do.** Advanced features such as scenes, automations, screen view, files and the clipboard are switched on per phone in the program's settings.
- **The firewall rule only covers Private networks**, not public Wi-Fi.
- **The optional web app is not encrypted.** The program warns you before you turn it on.
- **Secure desktop control is optional and off by default.** It lets a paired phone see and control UAC prompts and the lock screen. That is powerful and risky, so you have to read and confirm the risks before you can turn it on.

Remove phones you no longer use in the program's settings.

## Troubleshooting

**Windows says "Windows protected your PC" when I run the installer.**
Only continue if you downloaded it from this page. Click *More info*, then *Run anyway*.

**My phone cannot connect.**
Check that both devices are on the same Wi-Fi, that the program is running (look for its tray icon), that Windows has your network set to Private, and that the firewall rule exists (the program's Settings page shows its status).

**The gamepad says it needs a driver.**
Open the program, go to Settings, find *Gamepad driver* and click *Install ViGEmBus*, then accept the Windows prompt.

**The screen view shows "Windows security screen".**
Windows is showing a UAC prompt or the lock screen, which normal programs cannot see. Approve it on the PC, or see *Secure desktop control* in the program's Settings.

**I cannot control Task Manager or other administrator windows.**
Windows ignores input sent to administrator windows unless the program runs as administrator too. In Settings, turn on *Start as administrator*.

## Verifying your download

Each release lists the **SHA-256** checksum of its installer. To check yours, open PowerShell in the download folder and run:

```
Get-FileHash .\PCPulseCompanion-Setup.exe -Algorithm SHA256
```

The result should match the checksum in the release notes.

## Updates

Each new version is published here as a release. Installing a new version over the old one keeps your settings and paired phones.

## Feedback and problems

Found a bug or have an idea? Please [open an issue](../../issues) and say which version you use (shown in the program's window title) and what happened.

## Terms

PC Pulse Companion is pre-release software provided as is, without warranty. By installing or using it you agree to the terms of use shown during setup and on first start.
