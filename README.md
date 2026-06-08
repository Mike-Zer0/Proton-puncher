Proton Punch

1. Advanced Memory & Swap Optimization
Beyond Profile Sync Daemon, how Linux handles memory pressure dramatically affects system responsiveness:

ZRAM Automation with Custom Compressors: Automate the configuration of ZRAM (RAM-based swap utilizing fast in-kernel compression) using cutting-edge compressors like zstd or lz4. Proton Punch can dynamically calculate the optimal pool size based on the user's total system RAM.

MGLRU (Multi-Gen Least Recently Used) Toggling: Ensure users can easily verify and enable MGLRU via a simple GUI toggle. This modern kernel memory management feature prevents the system from locking up or dragging frame rates down when memory is nearly full.

Transparent Hugepages (THP) Controls: Provide option toggles for THP (always, madvise, or never). While always can boost performance for virtualization and databases, setting it to madvise is often preferred for gaming to prevent erratic latency spikes.

2. Micro-Stutter & Latency Defeating Tweaks
Splitting sysctl Virtual Memory (VM) Tweaks: Add a "Gaming/Low-Latency" profile that drops vm.max_map_count to higher levels (critical for modern Steam Play/Proton games like Hogwarts Legacy or Starfield) and fine-tunes dirty background ratios:

vm.dirty_background_ratio = 5

vm.dirty_ratio = 10
This forces the kernel to flush dirty pages to disk in smaller, more frequent batches, completely preventing the major storage-bound stutters that occur during massive auto-saves.

SELinux / Auditd Gaming Mode Switch: Temporarily suspending or reducing the verbosity of system auditing layers during heavy application execution can claw back minor CPU cycles and lower context-switching overhead.

3. Dedicated Input Lag & Sound Tweaks
Real-time Audio Scheduling (PipeWire/RTKit): Integrate automation that configures RTKit permissions for PipeWire, allowing the audio server to claim real-time thread priority. This eliminates crackling and cuts audio processing latency down to the millisecond level.

USB Polling Rate Tweaks: Provide an interface to safely adjust the module options for mouse and keyboard polling rates (e.g., forcing a rock-solid 1000Hz via usbhid kernel module parameters), giving a competitive edge in fast-paced inputs.

4. Storage & I/O Scheduler Profiles
I/O Scheduler Auto-Matching: Dynamically detect the underlying drive hardware and apply the absolute best scheduler on the fly.

Sets NVMe drives to none or kyber.

Sets SATA SSDs to mq-deadline.

FSTRIM Automation: Include a one-click manual TRIM execution button and a toggle to safely schedule background storage optimization blocks via fstrim.timer.
