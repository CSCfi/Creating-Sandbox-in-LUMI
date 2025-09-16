# Developing Interactive Sandbox in LUMI


This repository provides a minimal, reproducible sandboxed environment for **text-mode web browsing** on **LUMI** using **Lynx** inside a Singularity/Apptainer container.

The goal is a tiny, auditable setup that works on shared HPC nodes where you can’t use Docker.

> Note: On LUMI the container runtime is **Apptainer** (the successor to Singularity).
> Commands below use `apptainer`. If you only have `singularity`, the scripts
> will automatically fall back to it.
>

We provide examples and experiments for:

- **[onlineshopping](https://github.com/CSCfi/Creating-Sandbox-in-LUMI/tree/main/onlineshopping)** – doing secure online shopping on any online store
- **[webbrowsing](https://github.com/CSCfi/Creating-Sandbox-in-LUMI/tree/main/webbrowsing)** – safetly browsing webpages

---

## What to Expect in This Repo

**Implementation Examples**
- A small `webbrowsing.def` and `onlineshopping.def` (Ubuntu 22.04 + lynx) you can build as a **sandbox** (writable directory) or **SIF** (single file).
- Helper scripts to build images and run Lynx interactively.


**Guides & Utilities**
- Notes for LUMI module setup (`LUMI/24.03`, `systools`).
- Tips for proxies and non-interactive builds.

**Reproducibility**
- Each script is self-contained and documented.
- Expected outputs or checks are shown below so you can confirm a good build.

---

## Installations (LUMI)

> These examples are written for **LUMI**. If you use Puhti or Mahti, adjust modules/partitions accordingly.

