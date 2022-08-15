# Lenovo-Tiny6-M90Q-P340tiny-OpenCore-
The smallest fully functional (with dGPU) hackintosh


## My Configuration

- CPU: intel Core i9 10850K
- GPU: AMD Radeon Pro WX 4100 dGPU + UHD630 iGPU
- Memory: 64GB. 2x32 Hynix DDR4 3200 @ 2933MHz
- Storage: 2x Hynix Gold P31 2TB
- Wireless: Apple BCM943602CS with adapter and additional antenna in front bezel and tiny rear antenna.
- Power Supply: 230W
- BIOS: M2WKT57
- SMBIOS: iMac20,2

## Functionality

|Feature|Status|
|-------|------|
|Sleep/Wake|ok|
|iGPU&dGPU acceleration|ok|
|USB|ok|
|LAN|ok|
|WLAN|ok|
|BT|ok|
|Continuity|ok|
|Sidecar|ok|
|iMessage/facetime|ok|
|Sound|ok|
|HDMI/DP audio|ok|
|DRM|requires switching GPU with a command|

## What is different?

- This hack is the smallest fully functional hack I was able to build, including a dGPU for DRM.
- No kext needed for USB mapping as it only has 14 ports and doesn't exceed the macOS limitation. Only one dsdt patch was needed to enable the M.2 USB port.
- For efficiency, I combined all ACPI patches into a single SSDT. ACPI patching adds all the devices (including cosmetic ones) seen on a real iMac20 but avoids all cosmetic renaming.
- Recompiled all the kexts with highest level of optimization and opencore uses the least possible amount of patches and injections. The entire EFI is <2.8MB.
