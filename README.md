# 🚀 AndroidOne Experience Build Instructions

## 📦 Initialize the Local Repository

```bash
repo init -u https://github.com/SuperAviation001/manifest-one.git -b 15 --depth=1 --git-lfs
```

## 🔄 Sync the Source

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## ⚙️ Set Up the Environment

```bash
source build/envsetup.sh
```

## 📱 Choose a Target

```bash
lunch aosp_<device>-bp1a-user
```

> Replace `<device>` with your actual device codename.

## 🛠️ Build the Code

```bash
mka bacon -j$(nproc --all) | tee log.txt
```
