# Generic ALC Kernel Release Repo

An custom android12-5.10 Generic Kernel Image

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

## Notes

* Kernel source is in the [`android12-5.10-gki`](https://github.com/A1cInt/alc_android12-5.10-gki) repo.
* When reporting issues, include device, ROM + Android version, build tag, and logs (dmesg/last\_kmsg).
