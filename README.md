PowerShell diagnostic and repair script designed to fix performance and stability issues related to Windows Explorer, COM/CLSID registry entries, and shell extensions.
The script focuses on resolving Explorer crashes, hangs, slow context menus, and corrupted registry handlers by performing a structured, automated cleanup and analysis.
    
    Features:

✔ Registry Backup

Creates full backups of critical Explorer‑related registry locations:
HKCR\Directory\shellex\ContextMenuHandlers
HKCR\Drive\shellex\ContextMenuHandlers
HKCR\AllFilesystemObjects\shellex\ContextMenuHandlers
HKCR\CLSID

✔ Explorer Crash & Hang Diagnostics

Parses Windows Event Log (last 7 days) for:
Application Error (1000) – Explorer crashes
Application Hang (1002) – Explorer freezes / slowdowns
Outputs a readable summary to the log file.

✔ CLSID Integrity Scanner

Detects:
broken CLSID entries
missing DLL targets
empty or malformed COM registrations
Saves results for manual inspection.

✔ Context Menu Handler Cleanup

Automatically removes:
empty handlers
invalid CLSID references
malformed entries
This directly improves:
right‑click menu speed
Explorer responsiveness
system stability

✔ Thumbnail & Preview Handler Audit

Enumerates all non‑Microsoft thumbnail/preview providers that may cause:
folder freeze
thumbnail generation delays
Explorer crashes
Outputs a full list for further analysis.

✔ Explorer Restart

Gracefully restarts explorer.exe to apply changes immediately.

    Purpose:
    
This script is intended for:

PWSH/PS1 Script prepared for diagnose and repair issues with DCOM/Component Services (Explorer.exe crashes and hangs):
Cleaning corrupted or invalid COM/CLSID entries, removing problematic shell extensions, improving context menu performance,
identifying unstable thumbnail/preview handlers, restoring stability after software uninstallations or registry corruption.
It is especially useful on systems affected by heavy shell extension load, leftover entries from uninstalled software, 
broken COM registrations Explorer slowdowns or freezes.

03.06.2026
Jacek Żaczek
j.zaczek@post.pl
