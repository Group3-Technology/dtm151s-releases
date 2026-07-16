# G3 DTM 151-S Teslameter — Control GUI

Downloads for the desktop application that controls and monitors the
**Group3 DTM 151-S digital teslameter** over a serial connection.

### [⬇ Download the latest release](https://github.com/Group3-Technology/dtm151s-releases/releases/latest)

| File | Platform |
|------|----------|
| `G3_DTM151_Control-macos.zip` | macOS |
| `G3_DTM151_Control-windows.zip` | Windows 10/11 |
| `SHA256SUMS.txt` | Checksums for the above |

Each download contains the application, the full **User Guide** (PDF), and
third-party licence notices. No installer, no admin rights, and no separate
runtime to install — unzip and run.

---

## Installing

The application is **not code-signed**, so the first launch needs one extra
click to tell your operating system it is safe to run. This is normal for
in-house instrument software, and only needed once.

### Windows

1. Unzip `G3_DTM151_Control-windows.zip` somewhere convenient — for example
   `C:\Program Files\G3_DTM151` or your Desktop. **Keep all the files
   together in the folder.**
2. Open the folder and double-click **`G3_DTM151_Control.exe`**.
3. If Windows shows a blue **"Windows protected your PC"** dialog, click
   **More info → Run anyway**. Once only.

> Don't move the `.exe` out of its folder on its own — it needs the files
> alongside it.

### macOS

1. Unzip `G3_DTM151_Control-macos.zip` (double-click it in Finder).
2. Drag **`G3_DTM151_Control.app`** to your **Applications** folder.
3. First launch: **right-click (or Control-click) the app → Open**, then
   click **Open** in the dialog. A plain double-click is blocked by
   Gatekeeper on unsigned apps; right-click → Open authorises it once.
4. Afterwards, open it normally.

If macOS still refuses after a right-click → Open, clear the quarantine flag:

```bash
xattr -dr com.apple.quarantine "/Applications/G3_DTM151_Control.app"
```

## Verifying your download

Optional, but worth doing on a shared or unreliable connection — it confirms
the file arrived intact.

```bash
# macOS / Linux
shasum -a 256 -c SHA256SUMS.txt --ignore-missing

# Windows (PowerShell) — compare the output against SHA256SUMS.txt
Get-FileHash G3_DTM151_Control-windows.zip -Algorithm SHA256
```

## Documentation

The **User Guide** ships inside each download as `USER_GUIDE.pdf` — install
notes, the front-panel walkthrough, CSV logging, the derived-measure setup,
and troubleshooting.

## Support

For assistance, contact **Group3 Technology**.

Please include the application version (shown in the header bar, and under
**Help → About**), your operating system, and — if it's a connection problem
— what the CONSOLE tab shows.

## About this repository

This repository hosts **downloads only**. The application source is
maintained privately by Group3 Technology. The serial driver it builds on is
open source and available at
[Group3-Technology/group3lib](https://github.com/Group3-Technology/group3lib).

The application is MIT licensed — see [LICENSE](LICENSE). Third-party licence
notices are included in every download.
