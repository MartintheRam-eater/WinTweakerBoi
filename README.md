
                        WINDOW 10/11 PORTABLE TOOLS
                            Martin Ng's Release
                            
  Supported OS : Windows 10 & Windows 11 (x64)
  Privileges   : Administrator (Auto-elevates on launch)
  Dependencies : None (Uses built-in Windows PowerShell, DISM, SFC & Winget)
================================================================================

1. GETTING STARTED & FIRST-TIME LAUNCH
--------------------------------------------------------------------------------
1. Double-click "Win_Portable_Tools.exe".
2. Click "Yes" on the Windows User Account Control (UAC) Administrator prompt.
   * Note: Because this is an unsigned community/portable executable, Windows
     Defender SmartScreen may display a "Windows protected your PC" pop-up on
     new machines. Click "More info" -> "Run anyway".
3. Always run [Option 1: Create System Restore Point] before making system
   tweaks so you have a clean snapshot to roll back to at any time.

Navigation Controls:
  [M] Main Tweaks  - Appearance, gaming, battery, bloatware, audio & repair
  [E] Repair Kit   - Bootable USB creator, driver backup, mobile & diagnostics
  [T] Test Menu    - Preview custom audio/wallpapers and check live tweak status
  [0] Exit         - Safely close the utility


2. MAIN TWEAKS MENU ([M]) OVERVIEW
--------------------------------------------------------------------------------
[SAFETY]
  1. Create System Restore Point
     Creates a Windows restore point on drive C:\ prior to modifying settings.

[APPEARANCE & WALLPAPER]
  2. Set Custom Login Wallpaper (.jpg/.png)
     Copies your selected image to C:\Windows\Web\CustomWall and sets it as
     the Windows lock/login screen background.
  3. Reset Login Wallpaper
     Removes custom lock screen policies and restores the Windows default.
  4. Classic Win10 Context Menu / 5. Restore Win11 Context Menu
     Toggles the full legacy right-click menu in Windows 11 without extra clicks.
  6. Toggle Dark Mode ON / 7. Toggle Light Mode ON
     Switches both Windows system UI and supported apps between Dark and Light.

[GAMING & PERFORMANCE]
  8. Enable Gaming Tweaks
     Disables Windows mouse acceleration (1:1 raw input) and turns off Game DVR
     background recording to reduce input lag and frame drops.
  9. Unlock Ultimate Performance
     Unlocks Windows' hidden high-throughput power plan in Power Options.
 10. Deep Disk & Temp Cleanup + Flush DNS
     Clears user temp files, Windows temp files, Windows Update download cache,
     and flushes the local DNS resolver cache.
 11. Smart Battery Optimiser
     Keeps 100% CPU performance when plugged into AC power while capping CPU
     boost (70%), enabling PCIe power saving, and pausing background apps on DC.

[PRIVACY, DEBLOAT, AUDIO & BOOT]
 12. Disable Telemetry & Background Apps
     Turns off diagnostic telemetry policies, Advertising ID tracking, and
     global background UWP app execution.
 13. Custom Bloatware Remover Menu
     Opens an interactive sub-menu to individually disable/restore Windows
     Copilot, Taskbar Widgets, OneDrive, Xbox/Game Bar apps, and preinstalled
     consumer apps (Clipchamp, Solitaire, Bing News/Weather).
 14. Install Custom Shutdown Sound (.wav)
     Disables Fast Startup (required for shutdown audio) and assigns a genuine
     PCM .WAV file to Windows Logoff and Exit sound events.
 15. Explorer & Search Speed Pack
     Shows hidden file extensions (.exe, .bat, etc.), disables Bing web search
     inside the Start Menu, and turns off Aero Shake window minimizing.
 16. Remove Desktop Startup Delay
     Eliminates the built-in Windows desktop startup delay so apps load faster.
 17. Verbose Boot/Shutdown Messages
     Displays detailed driver and service loading status during boot/shutdown.
 18. Repair Windows Files (DISM + SFC)
     Runs official Microsoft DISM RestoreHealth and System File Checker scans.
 19. Update All Installed Apps (Winget)
     Updates all Winget-supported applications on the PC in one pass.
 20. REVERT ALL TWEAKS TO DEFAULT
     Rolls back all visual, gaming, power, sound, privacy, and boot registry
     tweaks to stock Windows defaults while keeping DISM/SFC repairs intact.


3. REPAIR, DRIVERS & MOBILE TOOLKIT ([E]) OVERVIEW
--------------------------------------------------------------------------------
[BOOTABLE USB & FIRMWARE]
  1. Bootable USB Creator (ISO & DD Raw Image Writer)
     Formats and flashes Windows ISOs (UEFI GPT with automatic NTFS/FAT32 split
     handling) or writes raw byte-for-byte DD images for Linux/recovery tools.
     * WARNING: Permanently erases all data on the selected USB disk number.
  2. Patch Windows 11 USB
     Mounts boot.wim on an existing Windows 11 installer USB and applies LabConfig
     bypasses for TPM 2.0, Secure Boot, and RAM checks.
  3. Reboot Directly into Motherboard BIOS / UEFI
     Restarts straight into firmware setup without pressing F2/Del/Esc.

[DRIVERS, ANDROID & LEGACY iOS REPAIR]
  4. Backup All PC Drivers to C:\DriverBackup
     Exports all installed third-party drivers using pnputil before an OS wipe.
  5. Block / 6. Allow Windows Update Driver Overwrites
     Prevents Windows Update from replacing custom GPU/audio drivers.
  7. Install Android ADB & Fastboot Tools
     Installs official Google Platform Tools via Winget.
  8. Install Apple Device Drivers & libimobiledevice
     Installs Apple iTunes USB drivers and libimobiledevice CLI utilities.
  9. Open Official Legacy iOS Kit Guide
     Opens the LukeZGD Legacy-iOS-Kit GitHub repository in your browser.

[NETWORK, LICENSE & DIAGNOSTICS]
 10. Network Reset + Cloudflare DNS (1.1.1.1)
     Releases/renews IP, resets Winsock, and sets Cloudflare 1.1.1.1 DNS.
 11. Show Saved Wi-Fi Passwords & IP Info
     Displays local IP configuration and saved Wi-Fi SSIDs with passwords.
 12. Check SSD / Hard Drive SMART Health
     Queries physical disk health and operational status via PowerShell.
 13. Save Battery Health & System Audit Reports (Desktop)
     Generates Battery_Report.html and System_Audit.txt on your Desktop.
 14. Backup BitLocker Recovery Key
     Displays the active BitLocker numerical recovery protector for drive C:\.
 15. Install Essential IT Apps
     Installs 7-Zip, VLC Media Player, Notepad++, and Git via Winget.
 16. Show Windows Product Key
     Reads the embedded motherboard UEFI/BIOS OEM product key and decodes the
     active Windows Registry license key.


4. TROUBLESHOOTING & TIPS
--------------------------------------------------------------------------------
* Custom Shutdown Sound Not Playing:
  Windows only plays genuine uncompressed PCM .WAV files for system events.
  An .MP3 file manually renamed to .WAV will not play. Keep Fast Startup off.
* Antivirus / SmartScreen False Positives:
  Self-compiled batch wrappers are unsigned binaries and may trigger heuristic
  warnings in Windows Defender or third-party antivirus suites. Add an
  exclusion if needed, or inspect the source .bat script directly.


================================================================================
5. LEGAL DISCLAIMER & TERMS OF USE
================================================================================
1. "AS-IS" SOFTWARE WARRANTY DISCLAIMER:
   This software ("Window 10/11 portable tools") is provided "AS IS" and "WITH
   ALL FAULTS", without warranty of any kind, express or implied, including but
   not limited to warranties of merchantability, fitness for a particular
   purpose, or non-infringement. As the title states: "Should hopefully work."

2. LIMITATION OF LIABILITY:
   In no event shall the author (-martin ng) or contributors be held liable for
   any direct, indirect, incidental, special, or consequential damages—including
   but not limited to data loss, corrupted OS installations, wiped USB drives,
   voided warranties, or system instability—arising from the use or misuse of
   this tool.

3. USER RESPONSIBILITY & DATA BACKUP:
   This utility modifies Windows Registry keys, system policies, power plans,
   installed packages, and physical storage partitions. You are solely
   responsible for creating backups of important files and creating a System
   Restore Point (Option 1) before running any modifications. Always double-check
   the target disk number before using the Bootable USB Creator.

4. THIRD-PARTY SOFTWARE & TRADEMARKS:
   - Windows, PowerShell, DISM, SFC, BitLocker, OneDrive, Copilot, and Winget
     are registered trademarks of Microsoft Corporation.
   - Android and ADB/Fastboot are trademarks of Google LLC.
   - Apple and iTunes are trademarks of Apple Inc.
   - Legacy iOS Kit is an open-source project maintained by LukeZGD.
   - Third-party packages installed via Winget (7-Zip, VLC, Notepad++, Git,
     Google Platform Tools, iTunes, libimobiledevice) are governed by their
     respective owners' software licenses.
   - All bugs report Martin.
   - If it broke your PC/Laptop/misc the creator and the software owner are not at fault.

5. AUTHORIZED USE ONLY:
   Diagnostic features (such as Wi-Fi password retrieval, BitLocker key backup,
   and OEM product key recovery) are intended strictly for system administration,
   data recovery, and troubleshooting on devices you own or have explicit
   authorization to service.
================================================================================
