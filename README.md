#  OrangeFox recovery tree for Oneplus 13R/Ace 5 with qualcomm processor codenamed pineapple

Platforms, included under oneplus's codename "pineapple", are:
- Qualcomm Snapdragon 8 Gen 3 (SM8650)

Devices, that can run and will run this recovery without any sudden and unforseen issues:
- Oneplus 13R/Ace 5 (ossi)

## Features

Works:

- [X] ADB
- [X] Display
- [X] Fasbootd
- [X] Flashing
- [X] Sideload
- [X] USB OTG
- [X] Touch
- [X] Flashlight
- [X] Vibrator/Haptic
- [X] OTA/Payload
- [ ] User data decryption on RUI(We can only decrypt “/data”)
- [ ] Сannot format DATA on RUI, until user data is decrypted

# Building

```bash
git clone https://github.com/realme-pineapple-devs/recovery_device_realme_pineapple.git device/realme/pineapple
bash device/realme/pineapple/patches/apply-patches.sh .
. build/envsetup.sh
lunch twrp_pineapple-ap2a-eng
make installclean
mka adbd recoveryimage
```

## To use it:

```
fastboot flash recovery out/target/product/pineapple/recovery.img
```
