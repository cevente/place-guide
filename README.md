# 👋 Welcome to The Angel Place — Sapphire (SM6225)

Welcome to the official build guide repository for **Xiaomi Redmi Note 13 4G (Sapphire / SM6225)**.

This repository provides all the essential scripts and setup resources needed to initialize the device trees and HALs for building custom ROMs based on **AOSP / LineageOS**.

Whether you're maintaining, testing, or building your own ROM, this repo aims to make setup faster and cleaner.

---

# 📦 Repository Structure

This repository includes separated setup scripts for better organization:

* 🌳 **Device Trees**
* ⚙️ **HALs (Hardware Abstraction Layer)**

Keeping them separated makes updates easier and avoids unnecessary syncs.

---

# 🚀 Quick Start

Make sure you are inside the root of your source directory before executing them.

---

# 🌳 Device Trees Setup (`trees.sh`)

```bash
# Clone Device Trees for Sapphire
echo "Cloning Device Trees for Sapphire..."

rm -rf device/xiaomi/sapphire-kernel
git clone --depth 1 -b lineage-23.2 https://github.com/The-Angel-Place-Sapphire/device_xiaomi_sapphire-kernel.git device/xiaomi/sapphire-kernel

rm -rf device/xiaomi/sepolicy
git clone --depth 1 -b 16 https://github.com/The-Angel-Place-Sapphire/device_xiaomi_sepolicy.git device/xiaomi/sepolicy

rm -rf device/xiaomi/sapphire
git clone --depth 1 -b lineage-23.2 https://github.com/The-Angel-Place-Sapphire/device_xiaomi_sapphire.git device/xiaomi/sapphire

rm -rf vendor/xiaomi/sapphire
git clone --depth 1 -b lineage-23.2 https://github.com/The-Angel-Place-Sapphire/vendor_xiaomi_sapphire.git vendor/xiaomi/sapphire

rm -rf hardware/xiaomi
git clone --depth 1 -b lineage-23.2 https://github.com/The-Angel-Place-Sapphire/android_hardware_xiaomi.git hardware/xiaomi

echo "============================"
echo "Device Trees cloned successfully"
echo "============================"
```

---

# ⚙️ HALs Setup (`hals.sh`)

```bash
# Clone HALs for SM6225
echo "Cloning HALs for SM6225..."

rm -rf hardware/qcom-caf/common
git clone --depth 1 -b lineage-23.2 https://github.com/The-Angel-Place-Sapphire/android_hardware_qcom-caf_common.git hardware/qcom-caf/common

rm -rf hardware/qcom-caf/sm6225/audio/agm
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/vendor_qcom_opensource_agm.git hardware/qcom-caf/sm6225/audio/agm

rm -rf hardware/qcom-caf/sm6225/audio/pal
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/vendor_qcom_opensource_arpal-lx.git hardware/qcom-caf/sm6225/audio/pal

rm -rf hardware/qcom-caf/sm6225/data-ipa-cfg-mgr
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/vendor_qcom_opensource_data-ipa-cfg-mgr.git hardware/qcom-caf/sm6225/data-ipa-cfg-mgr

rm -rf hardware/qcom-caf/sm6225/dataipa
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/vendor_qcom_opensource_dataipa.git hardware/qcom-caf/sm6225/dataipa

rm -rf hardware/qcom-caf/sm6225/display
git clone --depth 1 -b lineage-22.0-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/hardware_qcom_display.git hardware/qcom-caf/sm6225/display

rm -rf hardware/qcom-caf/sm6225/media
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/hardware_qcom_media.git hardware/qcom-caf/sm6225/media

rm -rf hardware/qcom-caf/sm6225/audio/primary-hal
git clone --depth 1 -b lineage-22.0-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/hardware_qcom_audio.git hardware/qcom-caf/sm6225/audio/primary-hal

rm -rf device/qcom/sepolicy_vndr/sm6225
git clone --depth 1 -b lineage-23.2-caf-sm6225 https://github.com/The-Angel-Place-Sapphire/device_qcom_sepolicy_vndr.git device/qcom/sepolicy_vndr/sm6225

echo "============================"
echo "HALs cloned successfully"
echo "============================"
```

---

# 📌 Notes

* This repository always tracks the **latest available stable branch** for each component.
* If a repository does not provide `lineage-23.2`, the latest compatible branch is used.

---

# 💡 Recommendation

For long-term maintenance and cleaner syncing, using **local manifests** is recommended over manual clone scripts.

However, these scripts are useful for:

* Fast setup
* Testing
* Temporary builds
* Development environments

---

# 🤝 Contributions

Contributions, fixes, and improvements are welcome.

Feel free to open issues or submit pull requests.

---

# 👑 Maintained by

**The Angel Place**
Building Sapphire, one commit at a time.
