# Geeboon Solder Station Firmware Update Guide

This guide provides step-by-step instructions for updating the firmware on Geeboon solder stations (**TC22**, **HC24**, **TA305**, **HA310**) using a **Windows PC**. 

> [!IMPORTANT]  
> Use a **USB-C cable that supports both power and data transfer**.  
> *Charging-only ("fast charge") cables will **not** work.*

> [!NOTE]  
> Customization (e.g., background images, text colors) is possible via supplied tools—covered in a separate guide.

---

## Supported Models & Firmware Files

| Model(s)       | Latest Firmware (as of Oct 2025) 
|----------------|---------------------------------|
| TC22, HC24     | `TC22_HC24_1.27.bin`            | 
| TA305, HA310   | `TA305_HA310_1.21.bin`          |


> Additional sources:
>
> [Geeboon TC22 (240W)](https://s.click.aliexpress.com/e/_c2J6rGEr)<br>
> [Geeboon TC22 (240W) Diferent Handlers](https://s.click.aliexpress.com/e/_c3aeKzxl)<br>
> [Geeboon HC24 (400W)](https://s.click.aliexpress.com/e/_c4PUoRr9)<br>
> [Geeboon HA310 (350W)](https://s.click.aliexpress.com/e/_c3HQJADl)<br>
> [Geeboon TA305 (150W)](https://s.click.aliexpress.com/e/_c4rsrmb1)<br>
> [Geeboon SDC02](https://s.click.aliexpress.com/e/_c4T9GRHt).
> 

---

## Prerequisites

- Windows PC with **File Explorer**
- USB-C cable (data + power)
- Antivirus allowance for downloads (`.bin` files may trigger false positives)

---

## Checking Current Firmware Version

1. Power on the station.
2. **TC22/HC24**: Press and hold the knob.  
   **TA305/HA310**: Press and hold the **Menu** button.  
   → Navigate to **About** menu.
3. View **AppVER: x.xx** at the bottom.

---

## Downloading & Extracting Firmware

1. Download the ZIP from the appropriate Google Drive link.
2. Extract the ZIP (right-click → **Extract All**).  
   → Contains: `.bin` files, `GBN_MAKER.exe` (for customization), `Update Notes.txt`, user guide PDF.
3. If nested ZIP (e.g., `TC22_HC24_1.27.bin.zip`): Extract again to access the raw `.bin` file.

> [!TIP]  
> Read `Update Notes.txt` before proceeding.

---

## Update Procedure

### 1. Connect the Solder Station
Plug the USB-C cable into the station's front USB-C port and your PC.  
*(Station can be powered on or off—USB provides temporary power if needed.)*

→ Within **1–2 seconds**:
- Station screen shows USB connection indicator.
- Windows plays the **device connection sound** (`da-ding`).
- Display updates to: **`USB ON`**

### 2. Open the Mass Storage Device
In **File Explorer** → **This PC**, locate the new drive:
GEEBOON-MSD (X:)
text*`X:` is the assigned drive letter (e.g., `E:`, `F:`). Multiple instances may appear—use any.*

### 3. Copy the Firmware File
1. Locate your extracted `.bin` file (e.g., `TC22_HC24_1.27.bin`).
2. Right-click and drag it to **`GEEBOON-MSD (X:)`**.
3. Release → Select **Copy to GEEBOON-MSD (X:)**.

→ Windows transfer dialog appears (progress bar advances in ~3 stages).

### 4. Monitor Transfer Progress
On the station display:
- **`BIN`** + counter from `0` to `180`.
- Upon completion:
UPDATA SUCCESS!
Please unplug USB.
text### 5. Complete the Update
**Unplug** the USB cable.  

- **If powered on**: Reboots automatically (~1 second); resumes heating if iron attached.  
- **If unpowered**: Return to workstation and reconnect to mains.

---

## Verification

- Re-check **About** menu: **AppVER** matches new version.
- Station boots normally; no errors.
- Test features (e.g., fan noise reduction, temperature stability).

---

## Troubleshooting

| Issue                                 | Solution |
|---------------------------------------|----------|
| No `da-ding`/drive not found          | Verify data-capable USB-C cable/port; try rear USB ports. |
| Antivirus quarantines files           | Restore from quarantine; add exception for Geeboon files. |
| `GEEBOON-MSD` missing/duplicated      | Replug; duplicates are safe—use first. |
| Transfer fails/freezes                | Re-download/extract; ensure no file corruption. |
| Post-update errors                    | Revert to previous `.bin`; contact Geeboon support. |

---

## Additional Resources

- **Video**: [Youtube](https://www.youtube.com/watch?v=zUvFAQcq4so)
- **Customization Guide**: Forthcoming (using `GBN_MAKER.exe` for `.gbn` files).
- **Manuals/Pinouts**: Included in downloads (e.g., `TA305.png`).


🤝 Contact

[Instagram](https://www.instagram.com/3lectro.crashvibes)
