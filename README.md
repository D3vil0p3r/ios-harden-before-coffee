# iPhone Hardening in 20 Minutes

A short, practical iPhone hardening guide: only the settings that matter most, with no 100-step checklists.

Each step lists the exact menu path and one line explaining why it matters. Tick the boxes as you go.

---

## Contents

1. [Before you start](#1-before-you-start-2-min)
2. [Essentials](#2-essentials-5-min)
3. [Lockdown Mode](#3-lockdown-mode-1-min)
4. [Privacy quick wins](#4-privacy-quick-wins-3-min)
5. [Go local: minimize iCloud](#5-go-local-minimize-icloud-10-min)
6. [Emergency: disable Face ID in 2 seconds](#6-emergency-disable-face-id-in-2-seconds)
7. [Good habits](#7-good-habits)
8. [What this guide does NOT protect against](#8-what-this-guide-does-not-protect-against)

---

## 1. Before you start (2 min)

- [ ] **Update iOS:** `Settings > General > Software Update`
  Why: most real-world attacks target vulnerabilities that are already patched.
- [ ] **Make an encrypted local backup** (see [section 5.1](#51-make-a-local-encrypted-backup-first)) and keep a copy in a safe place, such as an external drive stored away from your computer.
  Why: this guide moves your data off iCloud, so the local backup becomes your only copy. It also protects you from your own mistakes while changing settings.

---

## 2. Essentials (5 min)

### Passcode and Face ID

- [ ] **Use a strong passcode:** `Settings > Face ID & Passcode > Change Passcode`
  Enter your current passcode. On the next screen, tap on **(Passcode Options)** (the three dots **...** on top-right the keypad) and choose **Custom Alphanumeric Code**.
  Why: the passcode protects everything else on the phone. A 4-digit code can be guessed or watched over your shoulder. At minimum, use 6+ digits.
- [ ] **Keep Face ID ON**
  Why: Face ID makes a long passcode practical, because you rarely have to type it. Stolen Device Protection also depends on it. If you're worried about being forced to unlock, learn [section 6](#6-emergency-disable-face-id-in-2-seconds).
- [ ] **Face ID with a Mask: OFF:** `Settings > Face ID & Passcode > Face ID with a Mask`
  Why: it only checks the area around your eyes, which is less accurate than full-face recognition. Enable it only if you wear a mask often.
- [ ] **Require Attention for Face ID: ON:** `Settings > Face ID & Passcode > Require Attention for Face ID`
  Why: the phone won't unlock if your eyes are closed or you're not looking at it.

### Anti-theft

- [ ] **Stolen Device Protection: ON, set to Always:** `Settings > Face ID & Passcode > Stolen Device Protection` → turn on → `Require Security Delay` → **Always**
  Why: even with your passcode, a thief can't change your Apple Account password, view saved passwords or turn off Find My without your face, plus a 1-hour delay.
- [ ] **Find My iPhone: ON:** `Settings > [your name] > Find My > Find My iPhone` → enable **Find My iPhone**, **Find My network** and **Send Last Location**
  Why: lets you locate or erase the phone, and enables Activation Lock, which makes a stolen iPhone nearly worthless to resell.
- [ ] **SIM PIN: ON:** `Settings > Cellular > SIM PIN` (for eSIM: `Settings > Cellular > [your line] > SIM PIN`)
  Why: without it, a thief can put your SIM in another phone and receive your SMS codes for banking and other accounts.\
  ⚠️ Carriers often set a default PIN like `0000` or `1234`, so change it. Keep your PUK code somewhere safe: 3 wrong PINs lock the SIM.

### Lock screen

- [ ] **Limit what works while locked:** `Settings > Face ID & Passcode > Allow Access When Locked`
  Turn **OFF**: Control Center, Accessories, Reply with Message, Home Control, Wallet, Siri.
  Why: with Control Center open, a thief can enable airplane mode and cut off Find My tracking. With Accessories off, USB data connections are blocked while the phone is locked.
- [ ] **Hide notification previews:** `Settings > Notifications > Show Previews > When Unlocked`
  Why: SMS login codes and private messages won't show on the lock screen.

### Updates

- [ ] **Automatic updates: ON:** `Settings > General > Software Update > Automatic Updates` → turn on **iOS Updates** (download and install) and **Security Responses & System Files**
  Why: security fixes are installed without you having to remember.
- [ ] **Background Security Improvements: ON** (if present): `Settings > Privacy & Security > Background Security Improvements`
  Why: installs security fixes between regular iOS updates.

---

## 3. Lockdown Mode (1 min)

**Recommended for everyone, unless one of the restrictions below is a problem for you.**

Lockdown Mode greatly reduces how much of the iPhone can be attacked. It was designed against advanced spyware, but it works just as well against everyday attacks that arrive through messages, links and websites.

- [ ] **Turn on Lockdown Mode:** `Settings > Privacy & Security > Lockdown Mode > Turn On Lockdown Mode` → restart

**What changes:**

| Area | Impact |
|---|---|
| Messages | Most attachment types other than images are blocked. Link previews are disabled. |
| Web browsing | Some web technologies are disabled. Complex websites may load slower or display incorrectly. |
| FaceTime | Calls from people you haven't called before are blocked. |
| Apple services | Invitations from unknown people (e.g. Home, shared notes) are blocked. Shared Albums are removed. |
| Photos | Location data is removed when you share photos. |
| Wired connections | Connections to computers and accessories are blocked while the iPhone is locked. |
| Configuration profiles | Profiles can't be installed and the device can't be enrolled in device management (MDM). ⚠️ This matters for **work phones**. |
| Network | 2G support is disabled, and the phone won't auto-join non-secure Wi-Fi networks. |

**Don't enable it if** you depend heavily on Shared Albums, or regularly receive files other than images via iMessage.

**Work phone with MDM?** Phones already enrolled stay managed after you enable Lockdown Mode. If you still need to enroll your phone or install a configuration profile, turn Lockdown Mode off temporarily, complete the setup, then turn it back on. Please test if your organization's apps (i.e., VPN connection too) work as intended.

**Tip:** if a specific app or website breaks, you can exclude it from Lockdown Mode's web restrictions instead of turning the whole mode off: `Settings > Privacy & Security > Lockdown Mode > Configure Web Browsing`.

---

## 4. Privacy quick wins (3 min)

- [ ] **Block app tracking requests:** `Settings > Privacy & Security > Tracking` → **Allow Apps to Request to Track: OFF**
  Why: one tap stops every current and future app from asking to track you across other apps.
- [ ] **Safari: block fingerprinting everywhere:** `Settings > Apps > Safari > Advanced > Advanced Tracking and Fingerprinting Protection` → **All Browsing**
  Why: by default this protection only applies in Private Browsing.
- [ ] **Safari: Fraudulent Website Warning: ON:** `Settings > Apps > Safari > Fraudulent Website Warning`
  Why: warns you before you open known phishing sites.
- [ ] **Review location access:** `Settings > Privacy & Security > Location Services`
  Change apps set to **Always** to **While Using** or **Never**. Turn off **Precise Location** for apps that don't need it, such as weather or shopping apps.
- [ ] **Significant Locations: OFF:** `Settings > Privacy & Security > Location Services > System Services > Significant Locations`
  Why: stops the phone from building a history of places you visit often. If you have some data stored, delete the history.
- [ ] **Personalized Ads: OFF:** `Settings > Privacy & Security > Apple Advertising`
- [ ] **Analytics sharing: OFF:** `Settings > Privacy & Security > Analytics & Improvements`
- [ ] **AirDrop: Receiving Off** (or **Contacts Only** if you use AirDrop often): `Settings > General > AirDrop`
  Why: strangers nearby can't send you files. You can still send files, and temporarily allow receiving when needed.
- [ ] **Run Safety Check:** `Settings > Privacy & Security > Safety Check > Manage Sharing & Access`
  Why: a guided review of who can see your location, which apps can access your data, and which devices are signed in to your account. Remove anything you don't recognize.

---

## 5. Go local: minimize iCloud (10 min)

For users who want their data to live **on the iPhone only**. This takes longer than 10 minutes if you have a lot of data in iCloud. **Follow the steps in order.**

### 5.1 Make a local encrypted backup first

Without iCloud Backup, this becomes your **only** backup.

- [ ] Connect the iPhone to a computer.
  **Mac:** open Finder → select the iPhone → **General**.
  **Windows:** open the **Apple Devices** app (or iTunes) → select the iPhone.
- [ ] Check **Encrypt local backup**, choose a password and store it in a password manager. Then click **Back Up Now**.
  Why: an encrypted backup also includes your saved passwords and Health data. Without the password, the backup can't be restored.
- [ ] Repeat regularly, for example monthly.

### 5.2 Download your data before turning off sync

- [ ] **Photos:** `Settings > Apps > Photos` → under **iCloud Photos**, select **Download and Keep Originals**, then wait for the download to finish. If you don't see this option, iCloud Photos is already off: skip this step.
  When you later turn off iCloud Photos, choose **Download Photos & Videos** if asked, never **Remove from iPhone**.\
  ⚠️ If you skip this, the iPhone may only hold reduced-quality copies, and deleting iCloud Photos would lose the originals.
- [ ] **Passwords:** turning off iCloud Keychain keeps passwords **only on this device**. They're protected by your encrypted local backup (5.1).

### 5.3 Turn off iCloud for apps

- [ ] Where apps offer it, choose **local-only** storage (e.g. Notes: `Settings > Apps > Notes` → turn on **"On My iPhone" Account**).
- [ ] `Settings > [your name] > iCloud` → under **Saved to iCloud** tap **See All** → turn off every app.
  When asked, choose **Keep on My iPhone**.
- [ ] **Turn off iCloud Backup:** `Settings > [your name] > iCloud > iCloud Backup` → OFF
- [ ] **Delete existing iCloud backups:** `Settings > [your name] > iCloud > iCloud Backup` → delete each backup

> ⚠️ Third-party apps that back up through iCloud Drive (e.g. WhatsApp) will **stop backing up**. Check each important app's own backup settings.

> **Keep Find My ON.** It requires being signed in with your Apple Account, so stay signed in even with everything else off.

### 5.4 Clean up and lock down iCloud

- [ ] Sign in at [icloud.com](https://www.icloud.com) and **verify that nothing is left**: Photos, iCloud Drive, Notes, Mail, Contacts, Calendars, Reminders. Empty every **Recently Deleted** folder too.
- [ ] **Advanced Data Protection: ON:** `Settings > [your name] > iCloud > Advanced Data Protection`
  You'll need to set up a **recovery contact** or a **recovery key**.
  Why: encrypts almost all iCloud data end to end, so even Apple can't read it. Worth enabling as an extra layer, in case anything ends up in iCloud by mistake.\
  ⚠️ If you lose your devices **and** your recovery key or contact, Apple cannot recover your data.
- [ ] **Access iCloud Data on the Web: OFF:** `Settings > [your name] > iCloud > Access iCloud Data on the Web`
  Why: your iCloud data can't be accessed from a browser, even with your password. Do this **after** the check at icloud.com, because afterwards you'll no longer see your data there.

### 5.5 Review your account

- [ ] `Settings > [your name]` → scroll to the **device list** → remove any device you don't own or no longer use.

---

## 6. Emergency: disable Face ID in 2 seconds

If someone might force you to unlock your phone with your face (theft, robbery, a border check):

1. **Press and hold the side button and either volume button** for about 2 seconds.
2. When the power-off / Emergency SOS sliders appear, **release** and tap **Cancel**.
3. The iPhone now requires the **passcode** to unlock.

> ⚠️ **Don't keep holding the buttons** after the sliders appear. Doing so starts an emergency-call countdown.

---

## 7. Good habits

- **Restart your iPhone about once a week.** After a restart, before the first unlock, the iPhone is in its most protected state. Restarting also clears some kinds of spyware that don't survive a reboot.
- **Turn the phone off completely** before crossing a border or in other high-risk situations.
- **Delete apps you don't use.** Fewer apps means fewer things that can be attacked and fewer permissions to manage.
- **Never install configuration profiles** from websites, emails or messages unless they come from your employer's IT team.
- **Treat unexpected messages with links as suspicious**, even if they appear to come from your bank, a courier or Apple.

### Optional: Erase Data after 10 attempts

`Settings > Face ID & Passcode > Erase Data`
Erases the iPhone after 10 wrong passcode attempts.\
⚠️ Enable it only if **you have a recent backup** and **no children** are likely to play with your phone.

---

## 8. What this guide does NOT protect against

- **Phishing:** no setting can stop you from typing your password into a fake website. Check links before entering credentials.
- **Weak or reused passwords** on your online accounts. Use a password manager and enable two-factor authentication everywhere.
- **Apps you install and grant permissions to yourself.**
- **Someone who knows your passcode and has your phone unlocked.**

Security is a balance. This guide covers the measures with the highest impact for the least effort, and it doesn't try to make an iPhone unbreakable.

---

## Contributing

Found a setting that has moved, a translation issue, or an important quick win that's missing? Open an issue or a pull request. Please keep the spirit of the guide: **few steps, high impact.**

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): free to share and adapt, with attribution.

## Disclaimer

This guide is provided as-is, with no warranty. Apple may change settings in any iOS update. Always make sure you have a backup before changing security settings.
