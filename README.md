# anandab
### Principal Systems Architect • Ring 0 • High-Assurance Computing

<p align="center">
  <img src="https://media.giphy.com/media/7OHZkAAJ29VmE4LWLZ/giphy.gif" width="220" alt="Rajinikanth Style" />
</p>

```text
[ PHYSICAL LAWS: 0.6c / Landauer ] ──> [ KERNEL: eBPF / io_uring ] ──> [ DEFENSE: EW / Byzantine ]
```

<p align="center">

  <a href="mailto:3408818+anandab@users.noreply.github.com"><img src="https://img.shields.io/badge/Email-Direct-1e293b?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://anandab.github.io"><img src="https://img.shields.io/badge/Location-Bay_Area_CA-334155?style=flat-square" alt="Location" /></a>
</p>

Operating at the bare-metal frontier since 18 years. I design and harden distributed systems where physical limits, kernel internals, and hostile electronic conditions collide. If cache hierarchy is not up to the mark, adding more compute will degrade latency only.

---

### ⚡ The Triad: Physics, Silicon & Defense

| Domain | First-Principles Constraint | Production Enforcement |
| :--- | :--- | :--- |
| **Physics** | Signal propagates at ≈ 0.6c in copper (150 ps/in). Distance is latency itself. Heat bound by Landauer Limit (k_BT ln 2). | Protocols designed around physical light-cone latency bounds. Zero buffering past Bandwidth-Delay Product to prevent bufferbloat collapse. |
| **Kernel & Silicon** | Userspace context switches and unhandled interupt overhead destroy p99 determinism at terabit scale. | Zero-copy via `io_uring`, `splice`, and eBPF/XDP. Explicit 64-byte L1 cache padding to eliminate false sharing. AVX2/SIMD vector pipelines. |
| **Defense & EW** | Systems must survive kinetic link severance, GPS-jammed timing, and hostile Byzantine partition. | Air-gapped fail-safe loops that do the needful under SATCOM/RF blackout. Nodes fail locally and revert back gracefully once links restore. |

---


### ⚙️ Systems Dogma & Arsenal

```c
/*
 * 1. Physical invariants trump software abstractions. Always.
 * 2. Never allocate memory in the critical datapath.
 * 3. Tail latency is an architechtural defect, not a statistical anomaly.
 */
```

* **Core Languages:** C, C++20, Rust, Go, Python, Bash, x86-64 / ARM SIMD Assembly
* **Kernel & Host:** Linux VFS, eBPF (XDP/TC), `io_uring`, POSIX, `cgroups` v2, Namespaces, NUMA, Hugepages, Page Cache
* **Networks & Hardware:** HTTP/3, QUIC, RoCEv2, PFC/ECN, BGP, Anycast, Raw Sockets, NVMe-oF, Lustre Parallel DFS
* **Assurance & Defense:** Byzantine fault tolerance, air-gapped isolation, cryptographically verified boot, resiliant self-healing loops

---

<p align="center">
  <b>Available for high-rigor Staff/Principal IC and Mission-Critical Advisory</b><br />
  Direct inquiries: <code>3408818+anandab@users.noreply.github.com</code> • San Francisco Bay Area, CA
</p>
