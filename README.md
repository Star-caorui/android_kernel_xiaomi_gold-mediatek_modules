# MediaTek kernel modules for gold

MediaTek's connectivity (WMT, Wi-Fi, Bluetooth, GPS, FM), Mali GPU, fpsgo, MET and scheduler modules of the Redmi Note 13 5G (`gold`, MT6833) for LineageOS, built together with the system. How to set up the build is in [local_manifests](https://github.com/Star-caorui/local_manifests/tree/lineage-24.0-oss).

| | |
| --- | --- |
| Base | Xiaomi's release: [MiCode/MTK_kernel_modules](https://github.com/MiCode/MTK_kernel_modules) `spark-w-oss` (`a2081c2`) |
| On top | one commit per change; the first removes what gold does not build |
