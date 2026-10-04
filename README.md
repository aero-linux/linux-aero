# 🐧 linux-aero Kernel & Low-Latency Systems Suite

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0b0e,100:00f2fe&height=200&section=header&text=linux--aero%20Kernel&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Low-Latency%20Systems%20Architecture%20%26%20BORE%20Scheduler%20Tuning&descAlignY=62&descAlign=50" width="100%"/>

<br/>

[![Roadmap](https://img.shields.io/badge/Milestone-v1.7_Hyperion-0891b2?style=for-the-badge&logo=linux&logoColor=white)](https://github.com/aero-linux/linux-aero)
[![Scheduler](https://img.shields.io/badge/Scheduler-BORE_%2F_EEVDF-3178C6?style=for-the-badge&logo=gnubash&logoColor=white)](https://github.com/aero-linux/linux-aero)
[![License: GPL-2.0](https://img.shields.io/badge/License-GPL--2.0-4EAA25?style=for-the-badge)](LICENSE)

</div>

---

### 🚀 Overview
The systems repository for the **`linux-aero` custom kernel flavor** and low-latency kernel recipes powering **Aero Linux**. Optimized specifically for interactive desktop responsiveness, sub-millisecond audio DSP, real-time eBPF network telemetry, and zero-stutter frame scheduling under heavy multi-threaded compilation workloads.

### ⚡ Architectural Pillars

1. **BORE (Burst-Oriented Response Enhancer) Scheduler:**
   - Dynamically tracks CPU burstiness to prioritize interactive GUI threads, audio pipelines, and developer IDEs during background `cargo build`, `make -j`, or Docker container builds.
2. **Dynamic In-Memory Compression (zRAM with ZSTD):**
   - Eliminates disk swap thrashing by compressing anonymous memory pages in-RAM at algorithmically optimal latency.
3. **BBRv3 Congestion Control & Network Optimization:**
   - Kernel TCP buffers tuned for minimal bufferbloat and maximal throughput over high-latency developer pipelines.
4. **Low-Latency P-State & Audio DSP:**
   - 1000Hz timer frequency (`CONFIG_HZ_1000=y`), `PREEMPT_DYNAMIC` enabled, and low-latency ALSA / PipeWire parameters.

---

### 📂 Repository Structure

```
├── sysctl.d/
│   └── 99-aero-performance.conf   # Kernel sysctl parameters for memory, vm, and fs
├── scheduler/
│   └── bore-tuning.md             # Burst-oriented scheduling algorithms & benchmarks
├── kernel-config/
│   └── config-aero-edge           # Low-latency custom kernel configuration profile
└── scripts/
    └── apply-sysctl.sh            # One-command system performance applier
```

---

<div align="center">
  <p>Maintained by the <b><a href="https://github.com/aero-linux">Aero Linux Project</a></b> & <b><a href="https://github.com/ronitgupta138">@ronitgupta138</a></b></p>
</div>
