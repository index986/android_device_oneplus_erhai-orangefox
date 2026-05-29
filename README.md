# OnePlus Pad 3 erhai Android device tree

## Working

- [X] Display
- [X] Touch (Even in FastbootD)
- [ ] Decryption
- [ ] Flashing
- [ ] Backup & Restore
- [ ] MTP/OTG Storage
- [X] ADB/FastbootD
- [?] Factory Reset
- [N] Vibrator ( Not Applicable as OnePlus Pad 3 does not have one )

## Not working
- [ ] ????????

# How To Build

### Clone & Sync Source
```
mkdir -p ~/android/OrangeFox_14
cd ~/android/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/android/fox_14.1
```
### Clone Device-tree
```
cd ~/android/fox_14.1/device
mkdir -p oneplus
cd oneplus
git clone https://github.com/index986/android_device_oneplus_erhai-orangefox.git erhai
```
### BUILD!
```
cd ~/android/fox_14.1
source build/envsetup.sh
lunch twrp_erhai-ap2a-eng
mka adbd recoveryimage
```
