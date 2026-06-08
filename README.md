Proton Punch 🥊
The Ultimate All-in-One Linux Performance Hub
Proton Punch consolidates fragmented kernel, memory, and hardware tuning tools into a single, cohesive ecosystem. Built for gamers and power users, it unlocks your hardware's true potential without the terminal headache.

🏗️ Split-Agent Architecture
Maximum performance, zero security compromises. Proton Punch isolates high-privilege system tweaks from the user interface:

The Engine (Backend Daemon): A high-performance Rust/C++ daemon running with native root/polkit privileges to safely manage hardware registers, systemd, and the kernel.

The Control Panel (Frontend GUI): A sleek dashboard communicating via secure local sockets/D-Bus. Run it anywhere, completely sandboxed.

📦 Packages: Flatpak, AppImage | pacman (Arch), dnf (Fedora), apt (Ubuntu/Debian)

⚡ Key Features
🎮 Low-Latency & Memory Optimization
Dynamic Tuning: Automated kernel management via bpftune—no manual sysctl guesswork required.

Stutter Elimination: auto-cpufreq + Ananicy-CPP balance CPU scaling and process priorities on the fly.

RAM-Speed Profiles: Profile Sync Daemon (PSD) moves heavy app data to tmpfs to slash disk I/O.

Intelligent Swap: Automatically configures lightning-fast ZRAM pools using zstd or lz4.

🔌 Hardware Tuning & Overclocking Suite
GPU Control: Overclock AMD via sysfs (ppfeaturemask) and NVIDIA via native NVML bindings.

CPU Undervolting: Precision voltage offsets via AMD Curve Optimizer (ryzen_smu) and Intel MSR clamps.

RAM & Cooling: Verify XMP/EXPO ratings via dmidecode and draw custom fan curves mapped straight to hwmon.

🐧 Custom Kernel Manager
One-click installation and tracking for performance kernels like CachyOS and Linux-Zen. The backend automatically updates repository hooks and your bootloader (grub, systemd-boot).

🎬 Graphics Driver & Firmware Control Center
Skip the broken PPAs and terminal chaos. The engine automatically detects your hardware and delivers a flawless, automated graphics stack.

+------------------------------------------------------------+
| [⚡] PROTON PUNCH   |   [DRIVER & FIRMWARE]                |
+------------------------------------------------------------+
|  Detected Hardware: NVIDIA RTX 4070 / AMD Ryzen 7 7800X3D  |
|                                                            |
|  [🟢] NVIDIA Proprietary Driver                             |
|       Current: v580.126                                    |
|       [ Switch to Open-Kernel (DKMS) ] [ Toggle Beta Stream ]|
|                                                            |
|  [🟢] AMD Radeon / Mesa Stack                              |
|       Current: Mesa 26.0.5 (Vulkan 1.3)                    |
|       [ Install Bleeding-Edge Mesa-Git ]                   |
|                                                            |
|  [🟡] Video Acceleration (VA-API / NVDEC)                 |
|       Status: Incomplete hardware decoding codecs detected.|
|       [ Action: Auto-Fix Hardware Codecs ]                 |
+------------------------------------------------------------+
|  [ Action: Check System Firmware (fwupd) ]                  |
+------------------------------------------------------------+
🟢 NVIDIA Suite: Instantly toggle between Stable Production and Beta channels. Autoconfigures /etc/modprobe.d/ for open-source modules and low-latency sync.

🔴 AMD & Mesa Suite: Grab day-one gaming optimizations by linking to bleeding-edge Mesa-Git, and swap between RADV and AMDVLK Vulkan backends on the fly.

🎬 Auto-Fix Codecs: Scans via vainfo/clinfo and patches missing hardware acceleration dependencies (intel-media, nvidia-vaapi) to drop CPU overhead.

🔌 Unified Firmware: Deep fwupd integration to update your motherboard BIOS, SSD controllers, and gaming peripherals right from the dashboard.
