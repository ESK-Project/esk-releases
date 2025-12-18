# ESK Kernel Release Repo

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/ESK-Project/gki_kernel_builder/release.yml) [![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?logo=telegram&logoColor=white)](https://t.me/xaga_kernel)

Custom kernel for **xaga(in)** / **xagapro(in)**. Supports **AOSP** and **HyperOS**.

---

## Download

Get the latest **AnyKernel3 package** or **boot image** here:
- [Latest GitHub Release](https://github.com/ESK-Project/esk-releases/releases/latest)

---

## How to flash

### AnyKernel3

#### 1. Userspace (Recommended)

Flash directly from Android using any of these kernel flasher apps:
- Franco Kernel Manager (FKM)
- Kernel Flasher
- Horizon Kernel Flasher
- Or any other compatible tool

#### 2. Recovery

1. Reboot your device into recovery mode.  
2. Flash the package using ADB sideload or through flasher in custom recovery.

### Boot Image

1. Reboot your device into fastboot mode.
2. Flash the package:

```bash
fastboot flash boot <boot image>
```

> [!NOTE]
> If `fastboot` can’t determine the slot (or `fastboot flash boot ...` doesn’t work), check the active slot and flash to the matching one:
> ```bash
> fastboot flash boot_a boot.img   # if slot is a
> fastboot flash boot_b boot.img   # if slot is b
> ```

---

## Builds

All builds are automatically produced by:
[`ESK-Project/esk_builder`](https://github.com/ESK-Project/esk_builder)

Older builds (v2.4 and earlier) used:
[`ESK-Project/gki_kernel_builder`](https://github.com/ESK-Project/gki_kernel_builder)

---

## Notes

* Kernel source is in the [`android_kernel_xiaomi_mt6895`](https://github.com/ESK-Project/android_kernel_xiaomi_mt6895) repo.
* When reporting issues, include device, ROM + Android version, build tag, and logs (dmesg/last\_kmsg).
