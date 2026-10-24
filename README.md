## Canon LBP printers drivers installer for Ubuntu
Script for installing the Linux CAPT Printer Driver for Canon LBP printers on Ubuntu (both 32-bit and 64-bit)
### Install
```
wget https://github.com/hieplpvip/canon_printer/raw/master/canon_lbp_setup.sh
chmod +x canon_lbp_setup.sh
./canon_lbp_setup.sh
```
### Notes
After installation, there will be a shortcut on your Desktop. Run it to check your printer status (if it shows "Ready to Print", the printer is ready to use)

This is a legacy Canon CAPT driver. The installer uses the system package manager to resolve its dependencies and creates a native systemd service on systemd-based Ubuntu releases. Newer Ubuntu releases no longer provide `libglade2-0`; the installer then downloads the last Ubuntu archive build (checksum-verified) and installs it alongside the driver. The installer does not disable or weaken AppArmor to work around driver incompatibilities.

On 64-bit systems the driver also runs 32-bit helpers that need `libxml2.so.2`, which newer Ubuntu releases no longer ship for i386. The installer adds checksum-verified copies (with `libicu74`) to `/usr/local/lib/i386-linux-gnu` and removes them on uninstall. If the status monitor reports a socket error or printing stalls after a system upgrade, run `sudo ./canon_lbp_setup.sh fix-libs`.

### Supported Models
- LBP-810
- LBP1120
- LBP1210
- LBP2900
- LBP3000
- LBP3010
- LBP3018
- LBP3050
- LBP3100
- LBP3108
- LBP3150
- LBP3200
- LBP3210
- LBP3250
- LBP3300
- LBP3310
- LBP3500
- LBP5000
- LBP5050
- LBP5100
- LBP5300
- LBP6000
- LBP6018
- LBP6020
- LBP6020B
- LBP6200
- LBP6300n
- LBP6300
- LBP6310
- LBP7010C
- LBP7018C
- LBP7200C
- LBP7210C
- LBP9100C
- LBP9200C
### Original Script
http://help.ubuntu.ru/wiki/canon_capt
