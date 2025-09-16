# Developing Interactive Sandbox in LUMI


This repository provides a minimal, reproducible sandboxed environment for **text-mode web browsing** on **LUMI** using **Lynx** inside a Singularity/Apptainer container.

The goal is a tiny, auditable setup that works on shared HPC nodes where you can’t use Docker.

## What to Expect in This Repo

**Implementation Examples**
- A small `web_browsing.def` (Ubuntu 22.04 + lynx) you can build as a **sandbox** (writable directory) or **SIF** (single file).
- Helper scripts to build images and run Lynx interactively or as a one-liner.


**Guides & Utilities**
- Notes for LUMI module setup (`LUMI/24.03`, `systools`).
- Tips for proxies and non-interactive builds.

**Reproducibility**
- Each script is self-contained and documented.
- Expected outputs or checks are shown below so you can confirm a good build.

---

## Installations (LUMI)

> These examples are written for **LUMI**. If you use Puhti or Mahti, adjust modules/partitions accordingly.

