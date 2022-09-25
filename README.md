# TUF GAMING B550M-PLUS WIFI II - OpenCore EFI

适用于 ASUS TUF GAMING B550M-PLUS WIFI II（华硕 B550-M PLUS 重炮手 II）的 OpenCore EFI.

## 配置

| 组件 | 型号 |
|------|-----|
| CPU | AMD Ryzen 9 5900X 12-Core Processor |
| 内存 | 32 GB (16 * 2) 4000 MHz DDR4 |
| 显卡 | Vastarmor (瀚铠) RX 6650 XT 8GB |
| 硬盘 | ZHITAI (致态) TiPlus 5000 |
| 声卡 | Realtek ALCS1200A |
| 有线网卡 | Reaktek RTL8215 2.5GbE Controller |
| 无线 | Mediatek MT7921 Wi-Fi 6 |

## 状态

- 适配系统版本为 macOS Monterey 12 （或以上）。
- 除蓝牙、无线不可用外，其余功能均正常。
- 请自行修改 Kernel - Path 中的 `algrey - Force cpuid_cores_per_package` 适配你的 CPU
    -  取决于你的核心数，举例：5900X 有 12 (0C) 个物理核心，因此将三项的值分别改为 `B80C0000 0000`, `BA0C0000 0000` 和 `BA0C0000 0000`。
    - 如果你用的是 8 (08) 个核心的 5700X 或 5800X，则将三项分别改为 `B8080000 0000`, `BA080000 0000` 和 `BA080000 0000`。
- 请自行生成 SMBIOS 信息，建议使用 `MacPro7,1`，否则 USB 定制可能失效。